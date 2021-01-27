---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Bewerking ReflectAboutInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: 4d451c4e8e002f86c892b394f58ea2d7e9dd6a48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842983"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="4a37b-102">Bewerking ReflectAboutInteger</span><span class="sxs-lookup"><span data-stu-id="4a37b-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="4a37b-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="4a37b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="4a37b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a37b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a37b-105">Weerspiegelt een Quantum register over een gegeven klassiek geheel getal.</span><span class="sxs-lookup"><span data-stu-id="4a37b-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4a37b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4a37b-106">Description</span></span>

<span data-ttu-id="4a37b-107">Gezien een Quantum register in eerste instantie in de staat $ \ sum_i \ alpha_i \ket{i} $, waarbij elke $ \ket{i} $ een basis status is van een geheel getal $i $, weerspiegelt de status van de kassa over de basis status voor een bepaald geheel getal $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $</span><span class="sxs-lookup"><span data-stu-id="4a37b-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="4a37b-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4a37b-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="4a37b-109">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a37b-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a37b-110">Het klassieke geheel getal waarmee de basis status wordt geïndexeerd die moet worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="4a37b-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="4a37b-111">reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4a37b-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="4a37b-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a37b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4a37b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4a37b-113">Remarks</span></span>

<span data-ttu-id="4a37b-114">Deze bewerking wordt in-place geïmplementeerd zonder uitdrukkelijke toewijzing van aanvullende hulp qubits.</span><span class="sxs-lookup"><span data-stu-id="4a37b-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>