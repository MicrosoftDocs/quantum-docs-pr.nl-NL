---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Bewerking ApplyTransposition
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203311"
---
# <a name="applytransposition-operation"></a>Bewerking ApplyTransposition

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt de amplitude in de index vervangen `a` door de amplitude bij de index `b` in de opgegeven status-vector van `register` lengte $n $.  Als `a` gelijk is aan `b` , wordt de status-vector niet gewijzigd.

## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Eerste index (moet een waarde tussen 0 en $2 ^ n-$1) zijn


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

Tweede index (moet een waarde tussen 0 en $2 ^ n-$1) zijn


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een lijst met $n $ qubits waarop de omzetting wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

