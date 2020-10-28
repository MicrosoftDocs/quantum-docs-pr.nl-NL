---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Bewerking ApplyTransposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 1bd6f9580e09752f1de75927d6bb35417bb1ff21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709192"
---
# <a name="applytransposition-operation"></a>Bewerking ApplyTransposition

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket [](https://nuget.org/packages/)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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

