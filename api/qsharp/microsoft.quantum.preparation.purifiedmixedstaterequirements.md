---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: De functie PurifiedMixedStateRequirements
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229984"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="4327b-102">De functie PurifiedMixedStateRequirements</span><span class="sxs-lookup"><span data-stu-id="4327b-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="4327b-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="4327b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="4327b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4327b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4327b-105">Retourneert het totale aantal qubits dat moet worden toegewezen om de bewerking die wordt geretourneerd door te kunnen Toep assen @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="4327b-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="4327b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4327b-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="4327b-107">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4327b-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4327b-108">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="4327b-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="4327b-109">nCoefficients: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4327b-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4327b-110">Het aantal coëfficiënten dat moet worden opgegeven bij het voorbereiden van een gemengde status.</span><span class="sxs-lookup"><span data-stu-id="4327b-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="4327b-111">Uitvoer: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="4327b-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="4327b-112">Een beschrijving van het aantal qubits dat in totaal is vereist en voor elk van de index-en garbage-registers die worden gebruikt door de @"microsoft.quantum.preparation.purifiedmixedstate" functie.</span><span class="sxs-lookup"><span data-stu-id="4327b-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="4327b-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4327b-113">See Also</span></span>

- [<span data-ttu-id="4327b-114">Micro soft. Quantum. prepare. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="4327b-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)