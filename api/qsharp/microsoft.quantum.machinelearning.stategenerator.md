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
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="3478a-102">Door de gebruiker gedefinieerd StateGenerator-type</span><span class="sxs-lookup"><span data-stu-id="3478a-102">StateGenerator user defined type</span></span>

<span data-ttu-id="3478a-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3478a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="3478a-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3478a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="3478a-105">Hierin wordt een bewerking beschreven waarmee een gegeven invoer wordt voor bereid op een sequentiële classificatie.</span><span class="sxs-lookup"><span data-stu-id="3478a-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="3478a-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="3478a-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="3478a-107">NQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3478a-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3478a-108">Het aantal qubits waarvoor de gecodeerde invoer is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3478a-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="3478a-109">Voorbereiden: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="3478a-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="3478a-110">Een bewerking waarbij de gecodeerde invoer wordt voor bereid op een little-endian-REGI ster van `NQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="3478a-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>