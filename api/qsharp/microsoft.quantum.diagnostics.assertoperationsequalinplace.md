---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Bewerking AssertOperationsEqualInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 9b17bac9d95baf5a542604892c64130bf35d7f69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202427"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="4c02f-102">Bewerking AssertOperationsEqualInPlace</span><span class="sxs-lookup"><span data-stu-id="4c02f-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="4c02f-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="4c02f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="4c02f-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4c02f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4c02f-105">Als er twee bewerkingen worden uitgevoerd, worden er voor alle invoer statussen aangenomen dat ze identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="4c02f-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="4c02f-106">Deze bevestiging wordt geïmplementeerd door de actie te controleren van de bewerkingen in alle provincies van het formulier $V _0 \otimes... \otimes V_ {n-1} $, waarbij $V _k $ een van de statussen $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ en $ \ket{i} $ (+ 1 Eigenstate van Pauli Y-operator) is.</span><span class="sxs-lookup"><span data-stu-id="4c02f-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="4c02f-107">Deze verklaring maakt gebruik van $n $ qubits en vereist dat meerdere aanroepen van de bewerkingen worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="4c02f-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="4c02f-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4c02f-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="4c02f-109">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4c02f-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4c02f-110">Het aantal qubits-$n $ waarop de bewerkingen `givenU` zijn `expectedU` toegepast en waarop wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4c02f-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="4c02f-111">givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c02f-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4c02f-112">Bewerking op $n $ qubits moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="4c02f-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="4c02f-113">expectedU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="4c02f-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4c02f-114">Verwijzings bewerking op $n $ qubits die moet `givenU` worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="4c02f-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4c02f-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4c02f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="4c02f-116">Referenties</span><span class="sxs-lookup"><span data-stu-id="4c02f-116">References</span></span>

<span data-ttu-id="4c02f-117">De basis van de Staten $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ en $ \ket{i} $ is de Chuang-Nielsen basis, zoals beschreven in [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).</span><span class="sxs-lookup"><span data-stu-id="4c02f-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c02f-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4c02f-118">See Also</span></span>

- [<span data-ttu-id="4c02f-119">Micro soft. Quantum. Diagnostics. AssertOperationsEqualReferenced</span><span class="sxs-lookup"><span data-stu-id="4c02f-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)