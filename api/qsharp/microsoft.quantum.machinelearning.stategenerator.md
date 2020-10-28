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
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="01238-102">Door de gebruiker gedefinieerd StateGenerator-type</span><span class="sxs-lookup"><span data-stu-id="01238-102">StateGenerator user defined type</span></span>

<span data-ttu-id="01238-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="01238-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="01238-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="01238-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="01238-105">Hierin wordt een bewerking beschreven waarmee een gegeven invoer wordt voor bereid op een sequentiële classificatie.</span><span class="sxs-lookup"><span data-stu-id="01238-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="01238-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="01238-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="01238-107">NQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01238-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01238-108">Het aantal qubits waarvoor de gecodeerde invoer is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="01238-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit-adj--ctl"></a><span data-ttu-id="01238-109">Voorbereiden: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="01238-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="01238-110">Een bewerking waarbij de gecodeerde invoer wordt voor bereid op een little-endian-REGI ster van `NQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="01238-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>