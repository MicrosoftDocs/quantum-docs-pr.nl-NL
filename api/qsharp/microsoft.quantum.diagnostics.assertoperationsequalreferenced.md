---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Bewerking AssertOperationsEqualReferenced
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: a3e8791321b4f2ca1885dffeb92c7b13e5491a32
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702747"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="46e0b-102">Bewerking AssertOperationsEqualReferenced</span><span class="sxs-lookup"><span data-stu-id="46e0b-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="46e0b-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="46e0b-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="46e0b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46e0b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46e0b-105">Als er twee bewerkingen worden uitgevoerd, worden er voor alle invoer statussen aangenomen dat ze identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="46e0b-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="46e0b-106">Deze bevestiging wordt geïmplementeerd met behulp van de Choi – Jamiołkowski isomorphism om de bewering te beperken tot een van de Qubit-status verklaringen op twee Entangled-registers.</span><span class="sxs-lookup"><span data-stu-id="46e0b-106">This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers.</span></span>
<span data-ttu-id="46e0b-107">Deze bewerking heeft dus slechts één aanroep nodig voor elke bewerking die wordt getest, maar vereist twee keer zoveel qubits die moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="46e0b-107">Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated.</span></span>
<span data-ttu-id="46e0b-108">Deze bevestiging kan worden gebruikt om ervoor te zorgen dat een geoptimaliseerde versie van een bewerking identiek is aan de Naïve-implementatie, of dat een bewerking die op een bereik van niet-Quantum gegevens reageert, overeenkomt met de bekende gevallen.</span><span class="sxs-lookup"><span data-stu-id="46e0b-108">This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.</span></span>

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="46e0b-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="46e0b-109">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="46e0b-110">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46e0b-110">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46e0b-111">Aantal qubits dat aan elke bewerking moet worden door gegeven.</span><span class="sxs-lookup"><span data-stu-id="46e0b-111">Number of qubits to pass to each operation.</span></span>


### <a name="actual--qubit--unit"></a><span data-ttu-id="46e0b-112">werkelijk: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46e0b-112">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="46e0b-113">Te testen bewerking.</span><span class="sxs-lookup"><span data-stu-id="46e0b-113">Operation to be tested.</span></span>


### <a name="expected--qubit--unit-adj"></a><span data-ttu-id="46e0b-114">verwacht: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="46e0b-114">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="46e0b-115">Bewerking die het verwachte gedrag voor de bewerking tijdens de test definieert.</span><span class="sxs-lookup"><span data-stu-id="46e0b-115">Operation defining the expected behavior for the operation under test.</span></span>



## <a name="output--unit"></a><span data-ttu-id="46e0b-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46e0b-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="46e0b-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="46e0b-117">Remarks</span></span>

<span data-ttu-id="46e0b-118">Voor deze bewerking moet de bewerking worden gemodelleerd om het verwachte gedrag te adjointable, zodat de inverse alleen kan worden uitgevoerd op het doel register.</span><span class="sxs-lookup"><span data-stu-id="46e0b-118">This operation requires that the operation modeling the expected behavior is adjointable, so that the inverse can be performed on the target register alone.</span></span>
<span data-ttu-id="46e0b-119">Formeel, een kan een getransponeerde-bewerking opgeven, waardoor deze vereiste wordt versoepeld, maar de getransponeerde bewerking is niet in het algemeen fysiek te realiseren voor wille keurige Quantum bewerkingen, en is hier dus niet opgenomen als een optie.</span><span class="sxs-lookup"><span data-stu-id="46e0b-119">Formally, one can specify a transpose operation, which relaxes this requirement, but the transpose operation is not in general physically realizable for arbitrary quantum operations and thus is not included here as an option.</span></span>