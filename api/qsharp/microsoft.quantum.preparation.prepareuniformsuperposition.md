---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Bewerking PrepareUniformSuperposition
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230086"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="74b24-102">Bewerking PrepareUniformSuperposition</span><span class="sxs-lookup"><span data-stu-id="74b24-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="74b24-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="74b24-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="74b24-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="74b24-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="74b24-105">Hiermee maakt u een uniforme superpositie op status die 0 t/m-codeert `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="74b24-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="74b24-106">Dat wil zeggen dat deze unitary $U $ een uniforme superpositie maakt boven alle nummer Staten $0 $ tot $M-$1, op basis van een invoer status $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="74b24-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="74b24-107">Met andere woorden, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.</span><span class="sxs-lookup"><span data-stu-id="74b24-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="74b24-108">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="74b24-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="74b24-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="74b24-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="74b24-110">nIndices: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="74b24-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="74b24-111">Het gewenste aantal statussen $M $ in de uniforme superpositie.</span><span class="sxs-lookup"><span data-stu-id="74b24-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="74b24-112">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="74b24-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="74b24-113">Het Qubit-REGI ster waarin de nummer Staten worden opgeslagen in de `LittleEndian` indeling.</span><span class="sxs-lookup"><span data-stu-id="74b24-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="74b24-114">In dit REGI ster moet het getal $M-$1 worden opgeslagen en wordt ervan uitgegaan dat het is geïnitialiseerd in de status $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="74b24-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74b24-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74b24-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="74b24-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="74b24-116">Remarks</span></span>

<span data-ttu-id="74b24-117">De bewerking is adjointable, maar vereist dat `indexRegister` zich in een uniforme superpositie bevindt `nIndices` in de eerste basis status in dat geval.</span><span class="sxs-lookup"><span data-stu-id="74b24-117">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>