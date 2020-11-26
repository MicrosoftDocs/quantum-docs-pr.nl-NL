---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Bewerking AssertQubit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: 0e005230427bbd570133712679c51661e7ae6496
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202240"
---
# <a name="assertqubit-operation"></a><span data-ttu-id="9b790-102">Bewerking AssertQubit</span><span class="sxs-lookup"><span data-stu-id="9b790-102">AssertQubit operation</span></span>

<span data-ttu-id="9b790-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9b790-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9b790-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9b790-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9b790-105">Beweringen dat de Qubit `q` zich in de verwachte eigenstate van de Pauli Z-operator bevindt.</span><span class="sxs-lookup"><span data-stu-id="9b790-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.</span></span>

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="9b790-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9b790-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="9b790-107">verwacht: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="9b790-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="9b790-108">In welke staat wordt verwacht dat Qubit zich in: of bevindt `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="9b790-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="9b790-109">v: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9b790-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9b790-110">De Qubit waarvan de status wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="9b790-110">The qubit whose state is asserted.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9b790-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9b790-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9b790-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9b790-112">Remarks</span></span>

<span data-ttu-id="9b790-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Hiermee kunnen wille keurige Qubit-statussen worden bevestigd in plaats van alleen $Z $ eigenstates.</span><span class="sxs-lookup"><span data-stu-id="9b790-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b790-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9b790-114">See Also</span></span>

- [<span data-ttu-id="9b790-115">Micro soft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="9b790-115">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)