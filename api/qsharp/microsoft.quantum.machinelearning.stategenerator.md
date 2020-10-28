---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Door de gebruiker gedefinieerd StateGenerator-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: e3026dbae7209acd41924c0038a6f9b2c4b41197
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707963"
---
# <a name="stategenerator-user-defined-type"></a>Door de gebruiker gedefinieerd StateGenerator-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Hierin wordt een bewerking beschreven waarmee een gegeven invoer wordt voor bereid op een sequentiële classificatie.

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benoemde items

### <a name="nqubits--int"></a>NQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarvoor de gecodeerde invoer is gedefinieerd.
### <a name="prepare--littleendian--unit-adj--ctl"></a>Voorbereiden: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een bewerking waarbij de gecodeerde invoer wordt voor bereid op een little-endian-REGI ster van `NQubits` qubits.