---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Bewerking EstimateEnergy
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703088"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="ea6b6-102">Bewerking EstimateEnergy</span><span class="sxs-lookup"><span data-stu-id="ea6b6-102">EstimateEnergy operation</span></span>

<span data-ttu-id="ea6b6-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="ea6b6-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="ea6b6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ea6b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ea6b6-105">Maakt een schatting van de energie van het molecuul door het opsommen van de energie die door de afzonderlijke Jordan-Wignerings voorwaarden wordt bijgedragen.</span><span class="sxs-lookup"><span data-stu-id="ea6b6-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="ea6b6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ea6b6-106">Description</span></span>

<span data-ttu-id="ea6b6-107">Deze bewerking is impliciet afhankelijk van de indexerings Conventie omhoog en omlaag.</span><span class="sxs-lookup"><span data-stu-id="ea6b6-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="ea6b6-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="ea6b6-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="ea6b6-109">jwHamiltonian: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="ea6b6-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="ea6b6-110">De Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="ea6b6-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="ea6b6-111">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea6b6-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ea6b6-112">Het aantal steek proeven dat moet worden gebruikt voor de schatting van de verwachtingen van de term.</span><span class="sxs-lookup"><span data-stu-id="ea6b6-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="ea6b6-113">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ea6b6-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ea6b6-114">De geschatte energie van het molecuul</span><span class="sxs-lookup"><span data-stu-id="ea6b6-114">The estimated energy of the molecule</span></span>