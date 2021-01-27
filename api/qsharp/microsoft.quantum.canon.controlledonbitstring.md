---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: De functie ControlledOnBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 176170cc972ca67b812b84f79cf97ba5418be9b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840808"
---
# <a name="controlledonbitstring-function"></a>De functie ControlledOnBitString

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een unitary-bewerking die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven bitmasker.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>Beschrijving

De uitvoer van deze functie is een bewerking die kan worden weer gegeven met een unitary-trans formatie $U $, waarmee \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} waarbij $V $ een unitary-trans formatie is die de actie van de `oracle` bewerking vertegenwoordigt.

## <a name="input"></a>Invoer

### <a name="bits--bool"></a>bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De unitary-bewerking die moet worden toegepast op het doel register.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL

Een unitary-bewerking die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met het bitmasker `bits` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="example"></a>Voorbeeld

De volgende code fragmenten zijn gelijk:

```qsharp
(ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
```

en

```qsharp
within {
    ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
} apply {
    Controlled oracle(controlRegister, targetRegister);
}
```

Met de volgende code wordt een status $ \frac {1} {2} (\ket {00} -\ket {01} + \ket {10} + \ket {11} ) voor bereid.

```qsharp
using (register = Qubit[2]) {
    ApplyToEach(H, register);
    (ControlledOnBitString([false], Z))(register[0..0], register[1]);
}
```

## <a name="remarks"></a>Opmerkingen

Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).
Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.

Op basis van een Boole `bits` -matrix en een unitary `oracle` -bewerking is de uitvoer van deze functie een bewerking die de volgende stappen uitvoert:

* een bewerking Toep assen `X` op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` ;
* Toep assen `Controlled oracle` op het besturings element en de doel registers;
* pas een `X` bewerking toe op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` opnieuw om het controle register te retour neren naar de oorspronkelijke staat.

De uitvoer van de `Controlled` functor is een speciaal geval `ControlledOnBitString` waar `bits` is gelijk aan `[true, ..., true]` .