---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Bewerking MultiplexOperations
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: ad66b39fcfacbe5231ec3b9ba96989d6d5d449c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206099"
---
# <a name="multiplexoperations-operation"></a><span data-ttu-id="1fc80-102">Bewerking MultiplexOperations</span><span class="sxs-lookup"><span data-stu-id="1fc80-102">MultiplexOperations operation</span></span>

<span data-ttu-id="1fc80-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1fc80-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1fc80-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fc80-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fc80-105">Past een matrix van bewerkingen toe die worden beheerd door een matrix van aantal statussen.</span><span class="sxs-lookup"><span data-stu-id="1fc80-105">Applies an array of operations controlled by an array of number states.</span></span>

<span data-ttu-id="1fc80-106">Dat wil zeggen, een unitary-bewerking met vermenigvuldiging Toep assen $U $ waarmee een unitary $V _j $ wordt toegepast wanneer wordt bepaald door $n $-Qubit Number status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="1fc80-106">That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="1fc80-107">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="1fc80-107">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1fc80-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="1fc80-108">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="1fc80-109">unitaries: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL []</span><span class="sxs-lookup"><span data-stu-id="1fc80-109">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="1fc80-110">Matrix van Maxi maal $2 ^ n $ unitary-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="1fc80-110">Array of up to $2^n$ unitary operations.</span></span> <span data-ttu-id="1fc80-111">De $j $ de bewerking wordt geïndexeerd door de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="1fc80-111">The $j$th operation is indexed by the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="1fc80-112">index: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1fc80-112">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1fc80-113">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="1fc80-113">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="1fc80-114">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="1fc80-114">target : 'T</span></span>

<span data-ttu-id="1fc80-115">Generic Qubit-REGI ster dat $V _j $ treedt op.</span><span class="sxs-lookup"><span data-stu-id="1fc80-115">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1fc80-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1fc80-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1fc80-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1fc80-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1fc80-118">T</span><span class="sxs-lookup"><span data-stu-id="1fc80-118">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="1fc80-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1fc80-119">Remarks</span></span>

<span data-ttu-id="1fc80-120">`coefficients` wordt aangevuld met identiteits elementen als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="1fc80-120">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="1fc80-121">Deze implementatie maakt gebruik van $n-$1 hulp qubits.</span><span class="sxs-lookup"><span data-stu-id="1fc80-121">This implementation uses $n - 1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="1fc80-122">Referenties</span><span class="sxs-lookup"><span data-stu-id="1fc80-122">References</span></span>

- <span data-ttu-id="1fc80-123">Naar de eerste Quantum simulatie met Quantum SpeedUp Andrew M. Childs, Dmitri Maslov, Yunseongy, Neil J. Rvende, Yuan su https://arxiv.org/abs/1711.10980</span><span class="sxs-lookup"><span data-stu-id="1fc80-123">Toward the first quantum simulation with quantum speedup Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su https://arxiv.org/abs/1711.10980</span></span>