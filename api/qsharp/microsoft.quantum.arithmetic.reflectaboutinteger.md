---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Bewerking ReflectAboutInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706340"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="8ca68-102">Bewerking ReflectAboutInteger</span><span class="sxs-lookup"><span data-stu-id="8ca68-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="8ca68-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8ca68-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8ca68-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8ca68-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8ca68-105">Weerspiegelt een Quantum register over een gegeven klassiek geheel getal.</span><span class="sxs-lookup"><span data-stu-id="8ca68-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="8ca68-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8ca68-106">Description</span></span>

<span data-ttu-id="8ca68-107">Gezien een Quantum register in eerste instantie in de staat $ \ sum_i \ alpha_i \ket{i} $, waarbij elke $ \ket{i} $ een basis status is van een geheel getal $i $, weerspiegelt de status van de kassa over de basis status voor een bepaald geheel getal $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $</span><span class="sxs-lookup"><span data-stu-id="8ca68-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="8ca68-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="8ca68-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="8ca68-109">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8ca68-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8ca68-110">Het klassieke geheel getal waarmee de basis status wordt geïndexeerd die moet worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="8ca68-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="8ca68-111">reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8ca68-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="8ca68-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8ca68-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8ca68-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8ca68-113">Remarks</span></span>

<span data-ttu-id="8ca68-114">Deze bewerking wordt in-place geïmplementeerd zonder uitdrukkelijke toewijzing van aanvullende hulp qubits.</span><span class="sxs-lookup"><span data-stu-id="8ca68-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>