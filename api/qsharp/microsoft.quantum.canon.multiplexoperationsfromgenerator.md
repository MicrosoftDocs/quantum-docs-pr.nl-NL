---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: Bewerking MultiplexOperationsFromGenerator
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 59afa9d9a34fe74206118680940d243ed8b2496e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852497"
---
# <a name="multiplexoperationsfromgenerator-operation"></a><span data-ttu-id="47085-102">Bewerking MultiplexOperationsFromGenerator</span><span class="sxs-lookup"><span data-stu-id="47085-102">MultiplexOperationsFromGenerator operation</span></span>

<span data-ttu-id="47085-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="47085-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="47085-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="47085-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="47085-105">Past een met vermenigvuldiging beheerde unitary-bewerking toe $U $ waarmee een unitary $V _j $ wordt toegepast wanneer de waarde wordt bepaald door n-Qubit Number status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="47085-105">Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="47085-106">$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="47085-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="47085-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="47085-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit--is-adj--ctl"></a><span data-ttu-id="47085-108">unitaryGenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL)</span><span class="sxs-lookup"><span data-stu-id="47085-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="47085-109">Een tuple waarbij het eerste element `Int` het aantal unitaries $N $ is en het tweede element `(Int -> ('T => () is Adj + Ctl))` is een functie die een geheel getal $j $ in $ [0, N-1] $ gebruikt en de bewerking unitary $V _J $ uitvoert.</span><span class="sxs-lookup"><span data-stu-id="47085-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="47085-110">index: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="47085-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="47085-111">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="47085-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="47085-112">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="47085-112">target : 'T</span></span>

<span data-ttu-id="47085-113">Generic Qubit-REGI ster dat $V _j $ treedt op.</span><span class="sxs-lookup"><span data-stu-id="47085-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="47085-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47085-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="47085-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="47085-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47085-116">T</span><span class="sxs-lookup"><span data-stu-id="47085-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="47085-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="47085-117">Remarks</span></span>

<span data-ttu-id="47085-118">`coefficients` wordt aangevuld met identiteits elementen als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="47085-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="47085-119">Deze implementatie maakt gebruik van $n-$1 hulp qubits.</span><span class="sxs-lookup"><span data-stu-id="47085-119">This implementation uses $n-1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="47085-120">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="47085-120">References</span></span>

- [<span data-ttu-id="47085-121">*Andrew M. Childs, Dmitri Maslov, Yunseongy, Neil J. rvende, Yuan su*, arXiv: 1711.10980</span><span class="sxs-lookup"><span data-stu-id="47085-121"> *Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su*, arXiv:1711.10980</span></span>](https://arxiv.org/abs/1711.10980)