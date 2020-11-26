---
uid: Microsoft.Quantum.Canon.OperationPow
title: De functie OperationPow
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 808001200d276ca21cc5a70140d5d84d96da3496
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205810"
---
# <a name="operationpow-function"></a>De functie OperationPow

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking naar een stroom gegenereerd.

Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit"></a>op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.


### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keren dat $U $ moet worden herhaald.



## <a name="output--t--unit"></a>Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de bewerking die moet worden ingeschakeld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. OperationPowC](xref:Microsoft.Quantum.Canon.OperationPowC)
- [Micro soft. Quantum. Canon. OperationPowA](xref:Microsoft.Quantum.Canon.OperationPowA)
- [Micro soft. Quantum. Canon. OperationPowCA](xref:Microsoft.Quantum.Canon.OperationPowCA)