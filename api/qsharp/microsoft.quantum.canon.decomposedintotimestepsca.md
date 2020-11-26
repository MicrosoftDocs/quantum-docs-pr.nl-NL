---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: De functie DecomposedIntoTimeStepsCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: aa5f09f2e1fde878b523b4efc20b86c26ac738ff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216537"
---
# <a name="decomposedintotimestepsca-function"></a>De functie DecomposedIntoTimeStepsCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een bewerking die de Trotter – Suzuki integrator implementeert voor een bepaalde bewerking.

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="nsteps--int"></a>nSteps: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.


### <a name="op--intdoublet--unit--is-adj--ctl"></a>op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking die een index-invoer (type `Int` ) en een tijd invoer (type `Double` ) voor de ontleding accepteert.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Hiermee selecteert u de volg orde van de Trotter – Suzuki integrator die moet worden gebruikt.
Order 1 en zelfs orders 2, 4, 6,... worden momenteel ondersteund.



## <a name="output--doublet--unit--is-adj--ctl"></a>Output: ([Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Retourneert een unitary-implementatie van de Trotter – Suzuki integrator, waarbij de eerste para meter `Double` de grootte van de integratie stap is en de tweede para meter is gericht op het doel.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .

## <a name="remarks"></a>Opmerkingen

Als `order` deze functie wordt aangeroepen met gelijk aan `1` , wordt een bewerking geretourneerd die kan worden gesimuleerd door de laagste Trotter – Suzuki integrator $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}, \end{align} $ $ waar we de notatie van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139) hebben gevolgd en $ \lambda $ de ontwikkelings tijd zijn (vertegenwoordigd door de eerste invoer van de geretourneerde bewerking), en laat $ \{ H_j \} _ {j = 1} ^ {m} $ zijn de set van (schuine Hermitian) dynamische generators die worden `op(j, lambda, _)` gesimuleerd door de unitary-operator $e ^ {H_j \lambda} $.

Op dezelfde manier `order` retourneert een van `2` de tweede volg orde symmetrisch Trotter – Suzuki integrator $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.
\end{align} $ $

Hogere even waarden van `order` worden geïmplementeerd met de recursieve constructie van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).

## <a name="references"></a>Referenties

- [*D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders*](https://arxiv.org/abs/quant-ph/0508139)