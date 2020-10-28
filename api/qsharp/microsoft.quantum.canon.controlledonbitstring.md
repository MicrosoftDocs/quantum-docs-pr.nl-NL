---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: De functie ControlledOnBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: ca5a6e116eff187060f7a160e42836b170f0362d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704325"
---
# <a name="controlledonbitstring-function"></a>De functie ControlledOnBitString

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Retourneert een unitary-bewerking die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven bitmasker.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>Beschrijving

De uitvoer van deze functie is een bewerking die kan worden weer gegeven met een unitary-trans formatie $U $, waarmee \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} waarbij $V $ een unitary-trans formatie is die de actie van de `oracle` bewerking vertegenwoordigt.

## <a name="input"></a>Invoer

### <a name="bits--bool"></a>bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

De unitary-bewerking die moet worden toegepast op het doel register.



## <a name="output--qubitt--unit-adj--ctl"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een unitary-bewerking die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met het bitmasker `bits` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).
Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.

Op basis van een Boole `bits` -matrix en een unitary `oracle` -bewerking is de uitvoer van deze functie een bewerking die de volgende stappen uitvoert:

* een bewerking Toep assen `X` op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` ;
* Toep assen `Controlled oracle` op het besturings element en de doel registers;
* pas een `X` bewerking toe op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` opnieuw om het controle register te retour neren naar de oorspronkelijke staat.

De uitvoer van de `Controlled` functor is een speciaal geval `ControlledOnBitString` waar `bits` is gelijk aan `[true, ..., true]` .