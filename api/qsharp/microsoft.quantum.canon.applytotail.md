---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Bewerking ApplyToTail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850442"
---
# <a name="applytotail-operation"></a>Bewerking ApplyToTail

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking toegepast op het laatste element van een matrix.

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>Beschrijving

Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .

## <a name="input"></a>Invoer

### <a name="op--t--unit"></a>op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking die moet worden toegepast.


### <a name="targets--t"></a>doelen: ' []

Een matrix met doelen waarop de laatste wordt toegepast `op` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die moet worden toegepast.

## <a name="example"></a>Voorbeeld

De volgende Q #-fragmenten zijn gelijk:

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToTailA](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [Micro soft. Quantum. Canon. ApplyToTailC](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [Micro soft. Quantum. Canon. ApplyToTailCA](xref:Microsoft.Quantum.Canon.ApplyToTailCA)