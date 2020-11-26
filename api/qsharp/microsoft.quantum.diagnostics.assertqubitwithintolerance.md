---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Bewerking AssertQubitWithinTolerance
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 56b7f93f33ae18146c1fb13d404fc1d119eee72e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202189"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="cae5f-102">Bewerking AssertQubitWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="cae5f-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="cae5f-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="cae5f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="cae5f-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cae5f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="cae5f-105">Beweringen dat de Qubit `q` zich in de verwachte eigenstate van de Pauli Z-operator bevindt, tot een gegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="cae5f-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="cae5f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cae5f-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="cae5f-107">verwacht: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="cae5f-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="cae5f-108">In welke staat wordt verwacht dat Qubit zich in: of bevindt `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="cae5f-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="cae5f-109">v: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cae5f-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cae5f-110">De Qubit waarvan de status wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="cae5f-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="cae5f-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cae5f-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cae5f-112">Tolerantie voor de kans op een meting van de Qubit die het verwachte resultaat retourneert.</span><span class="sxs-lookup"><span data-stu-id="cae5f-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cae5f-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cae5f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cae5f-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cae5f-114">Remarks</span></span>

<span data-ttu-id="cae5f-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Hiermee kunnen wille keurige Qubit-statussen worden bevestigd in plaats van alleen $Z $ eigenstates.</span><span class="sxs-lookup"><span data-stu-id="cae5f-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="cae5f-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cae5f-116">See Also</span></span>

- [<span data-ttu-id="cae5f-117">Micro soft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="cae5f-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)