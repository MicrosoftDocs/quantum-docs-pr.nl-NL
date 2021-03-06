---
uid: Microsoft.Quantum.Canon.OperationPowC
title: De functie OperationPowC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 05b0d5b286e16c308d8c3df8fb8fa1ac8c9868ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852337"
---
# <a name="operationpowc-function"></a>De functie OperationPowC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking naar een stroom gegenereerd.
De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.

Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit--is-ctl"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.


### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keren dat $U $ moet worden herhaald.



## <a name="output--t--unit--is-ctl"></a>Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de bewerking die moet worden ingeschakeld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. OperationPow](xref:Microsoft.Quantum.Canon.OperationPow)