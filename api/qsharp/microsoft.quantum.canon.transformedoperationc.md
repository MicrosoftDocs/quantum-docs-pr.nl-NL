---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: De functie TransformedOperationC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 9475c5a1cc3b7e14c56c301749311a72e15f71e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852033"
---
# <a name="transformedoperationc-function"></a>De functie TransformedOperationC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="fn--u---t"></a>FN: ' U-> '

Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.


### <a name="op--t--unit--is-ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

De bewerking die moet worden getransformeerd.



## <a name="output--u--unit--is-ctl"></a>Uitvoer: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="u"></a>' U



## <a name="example"></a>Voorbeeld

Met de volgende aanroep wordt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" een bewerking die is ontworpen voor invoer, omgezet @"Microsoft.Quantum.Arithmetic.BigEndian" in een bewerking die invoer van het type accepteert @"Microsoft.Quantum.Arithmetic.LittleEndian" :

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. TransformedOperation](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [Micro soft. Quantum. Canon. TransformedOperationA](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [Micro soft. Quantum. Canon. TransformedOperationCA](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Micro soft. Quantum. Canon. ApplyWithInputTransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Micro soft. Quantum. Canon. samengesteld](xref:Microsoft.Quantum.Canon.Composed)