---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Door de gebruiker gedefinieerd StateGenerator-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854880"
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