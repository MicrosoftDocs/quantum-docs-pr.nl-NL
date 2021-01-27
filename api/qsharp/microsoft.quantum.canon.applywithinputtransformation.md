---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Bewerking ApplyWithInputTransformation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: d4589acbe9f9dc6c6ab665582ed663dbc193edbb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850381"
---
# <a name="applywithinputtransformation-operation"></a>Bewerking ApplyWithInputTransformation

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een bewerking waarbij een invoer wordt geaccepteerd, wordt met een functie die een uitvoer die compatibel is met die bewerking, en een invoer naar die functie, de bewerking toegepast met behulp van de functie om de invoer te transformeren naar een formulier dat wordt verwacht door de bewerking.

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a>Invoer

### <a name="fn--u---t"></a>FN: ' U-> '

Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.


### <a name="op--t--unit"></a>op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit) 

De bewerking die moet worden toegepast.


### <a name="input--u"></a>invoer: ' U

Een invoer voor de functie.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="u"></a>' U



## <a name="example"></a>Voorbeeld

De volgende aanroep gebruikt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" om een bewerking die is ontworpen voor invoer, toe @"Microsoft.Quantum.Arithmetic.BigEndian" te passen op een invoer van het type @"Microsoft.Quantum.Arithmetic.LittleEndian" :

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyWithInputTransformationA](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [Micro soft. Quantum. Canon. ApplyWithInputTransformationC](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [Micro soft. Quantum. Canon. ApplyWithInputTransformationCA](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [Micro soft. Quantum. Canon. TransformedOperation](xref:Microsoft.Quantum.Canon.TransformedOperation)