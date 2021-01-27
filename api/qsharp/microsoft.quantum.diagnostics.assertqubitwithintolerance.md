---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Bewerking AssertQubitWithinTolerance
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 7f57fc7a29d3eb86dc94cb24230d52b37eb6971d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853435"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="48bb0-102">Bewerking AssertQubitWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="48bb0-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="48bb0-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="48bb0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="48bb0-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="48bb0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="48bb0-105">Beweringen dat de Qubit `q` zich in de verwachte eigenstate van de Pauli Z-operator bevindt, tot een gegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="48bb0-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="48bb0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="48bb0-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="48bb0-107">verwacht: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="48bb0-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="48bb0-108">In welke staat wordt verwacht dat Qubit zich in: of bevindt `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="48bb0-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="48bb0-109">v: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="48bb0-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="48bb0-110">De Qubit waarvan de status wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="48bb0-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="48bb0-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48bb0-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="48bb0-112">Tolerantie voor de kans op een meting van de Qubit die het verwachte resultaat retourneert.</span><span class="sxs-lookup"><span data-stu-id="48bb0-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="48bb0-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="48bb0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="48bb0-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="48bb0-114">Remarks</span></span>

<span data-ttu-id="48bb0-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Hiermee kunnen wille keurige Qubit-statussen worden bevestigd in plaats van alleen $Z $ eigenstates.</span><span class="sxs-lookup"><span data-stu-id="48bb0-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="48bb0-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="48bb0-116">See Also</span></span>

- [<span data-ttu-id="48bb0-117">Micro soft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="48bb0-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)