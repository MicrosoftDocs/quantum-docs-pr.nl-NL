---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: De functie MultiplexerFromGenerator
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: b86238debe66747ba23c3b41164813594f80b27c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852554"
---
# <a name="multiplexerfromgenerator-function"></a><span data-ttu-id="11829-102">De functie MultiplexerFromGenerator</span><span class="sxs-lookup"><span data-stu-id="11829-102">MultiplexerFromGenerator function</span></span>

<span data-ttu-id="11829-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11829-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11829-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11829-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11829-105">Retourneert een met vermenigvuldiging beheerde unitary-bewerking $U $ waarmee een unitary $V _j $ wordt toegepast wanneer wordt bepaald door n-Qubit nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="11829-105">Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="11829-106">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="11829-106">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="11829-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="11829-107">Input</span></span>

### <a name="unitarygenerator--intint---qubit--unit--is-adj--ctl"></a><span data-ttu-id="11829-108">unitaryGenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL)</span><span class="sxs-lookup"><span data-stu-id="11829-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="11829-109">Een tuple waarbij het eerste element `Int` het aantal unitaries $N $ is en het tweede element `(Int -> ('T => () is Adj + Ctl))` is een functie die een geheel getal $j $ in $ [0, N-1] $ gebruikt en de bewerking unitary $V _J $ uitvoert.</span><span class="sxs-lookup"><span data-stu-id="11829-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>



## <a name="output--littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="11829-110">Output: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="11829-110">Output : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="11829-111">Een met vermenigvuldiging beheerde unitary-bewerking $U $ waarmee unitaries worden toegepast die worden beschreven door `unitaryGenerator` .</span><span class="sxs-lookup"><span data-stu-id="11829-111">A multiply-controlled unitary operation $U$ that applies unitaries described by `unitaryGenerator`.</span></span>

## <a name="see-also"></a><span data-ttu-id="11829-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="11829-112">See Also</span></span>

- [<span data-ttu-id="11829-113">Micro soft. Quantum. Canon. MultiplexOperationsFromGenerator</span><span class="sxs-lookup"><span data-stu-id="11829-113">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)