---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: De functie TransformedOperationCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840126"
---
# <a name="transformedoperationca-function"></a>De functie TransformedOperationCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="fn--u---t"></a>FN: ' U-> '

Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.


### <a name="op--t--unit--is-adj--ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De bewerking die moet worden getransformeerd.



## <a name="output--u--unit--is-adj--ctl"></a>Output: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

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