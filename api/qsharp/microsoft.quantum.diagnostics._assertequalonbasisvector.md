---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: d8f2195f75de49918032053dc8d1fa4fb4eba840
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213766"
---
# <a name="_assertequalonbasisvector-operation"></a><span data-ttu-id="c879d-102">_assertEqualOnBasisVector bewerking</span><span class="sxs-lookup"><span data-stu-id="c879d-102">_assertEqualOnBasisVector operation</span></span>

<span data-ttu-id="c879d-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c879d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c879d-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c879d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c879d-105">Hiermee wordt gecontroleerd of het resultaat van het Toep assen van twee bewerkingen `givenU` en `expectedU` de basis status hetzelfde is.</span><span class="sxs-lookup"><span data-stu-id="c879d-105">Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same.</span></span> <span data-ttu-id="c879d-106">De basis status wordt beschreven met de `basis` para meter.</span><span class="sxs-lookup"><span data-stu-id="c879d-106">The basis state is described by `basis` parameter.</span></span>
<span data-ttu-id="c879d-107">Zie <xref:microsoft.quantum.extensions.fliptobasis> functie voor meer informatie over deze beschrijving.</span><span class="sxs-lookup"><span data-stu-id="c879d-107">See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.</span></span>

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="c879d-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c879d-108">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="c879d-109">soort_jaar: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c879d-109">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c879d-110">Basis status opgegeven door een basis status-ID van één Qubit (0 <= id <= 3) voor elk van $n $ qubits.</span><span class="sxs-lookup"><span data-stu-id="c879d-110">Basis state specified by a single-qubit basis state ID (0 <= id <= 3) for each of $n$ qubits.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="c879d-111">givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c879d-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c879d-112">Bewerking op $n $ qubits moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="c879d-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="c879d-113">expectedU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="c879d-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c879d-114">Verwijzings bewerking op $n $ qubits dat givenU moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c879d-114">Reference operation on $n$ qubits that givenU is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c879d-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c879d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

