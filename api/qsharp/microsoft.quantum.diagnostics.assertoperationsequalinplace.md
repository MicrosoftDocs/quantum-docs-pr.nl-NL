---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Bewerking AssertOperationsEqualInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702753"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="c1de7-102">Bewerking AssertOperationsEqualInPlace</span><span class="sxs-lookup"><span data-stu-id="c1de7-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="c1de7-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c1de7-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c1de7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1de7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1de7-105">Als er twee bewerkingen worden uitgevoerd, worden er voor alle invoer statussen aangenomen dat ze identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="c1de7-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="c1de7-106">Deze bevestiging wordt geïmplementeerd door de actie te controleren van de bewerkingen in alle provincies van het formulier $V _0 \otimes... \otimes V_ {n-1} $, waarbij $V _k $ een van de statussen $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ en $ \ket{i} $ (+ 1 Eigenstate van Pauli Y-operator) is.</span><span class="sxs-lookup"><span data-stu-id="c1de7-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="c1de7-107">Deze verklaring maakt gebruik van $n $ qubits en vereist dat meerdere aanroepen van de bewerkingen worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c1de7-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="c1de7-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c1de7-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="c1de7-109">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c1de7-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c1de7-110">Het aantal qubits-$n $ waarop de bewerkingen `givenU` zijn `expectedU` toegepast en waarop wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1de7-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="c1de7-111">givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1de7-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c1de7-112">Bewerking op $n $ qubits moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="c1de7-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="c1de7-113">expectedU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="c1de7-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c1de7-114">Verwijzings bewerking op $n $ qubits die moet `givenU` worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c1de7-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c1de7-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1de7-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="c1de7-116">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="c1de7-116">References</span></span>

<span data-ttu-id="c1de7-117">De basis van de Staten $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ en $ \ket{i} $ is de Chuang-Nielsen basis, zoals beschreven in [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).</span><span class="sxs-lookup"><span data-stu-id="c1de7-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1de7-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c1de7-118">See Also</span></span>

- [<span data-ttu-id="c1de7-119">Micro soft. Quantum. Diagnostics. AssertOperationsEqualReferenced</span><span class="sxs-lookup"><span data-stu-id="c1de7-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)