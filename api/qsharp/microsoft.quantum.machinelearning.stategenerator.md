---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Door de gebruiker gedefinieerd StateGenerator-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: 5c9643f5c917ff3cb25fa8c046856b03cc287edd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211556"
---
# <a name="stategenerator-user-defined-type"></a>Door de gebruiker gedefinieerd StateGenerator-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Hierin wordt een bewerking beschreven waarmee een gegeven invoer wordt voor bereid op een sequentiële classificatie.

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benoemde items

### <a name="nqubits--int"></a>NQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarvoor de gecodeerde invoer is gedefinieerd.
### <a name="prepare--littleendian--unit--is-adj--ctl"></a>Voorbereiden: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking waarbij de gecodeerde invoer wordt voor bereid op een little-endian-REGI ster van `NQubits` qubits.