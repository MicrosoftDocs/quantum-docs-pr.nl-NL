---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: De functie OperationPowCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703911"
---
# <a name="operationpowca-function"></a>De functie OperationPowCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bewerking naar een stroom gegenereerd.
De aanpassings functie `A` geeft aan dat de bewerking kan worden bestuurd en adjointable.

Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit-ctl--adj"></a>op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) + correctie

Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.


### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keren dat $U $ moet worden herhaald.



## <a name="output--t--unit-ctl--adj"></a>Output: 'T [=> CTL](xref:microsoft.quantum.lang-ref.unit) en correctie

Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de bewerking die moet worden ingeschakeld.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. OperationPow](xref:Microsoft.Quantum.Canon.OperationPow)