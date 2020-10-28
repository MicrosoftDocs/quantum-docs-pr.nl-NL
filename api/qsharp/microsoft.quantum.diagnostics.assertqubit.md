---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Bewerking AssertQubit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702741"
---
# <a name="assertqubit-operation"></a><span data-ttu-id="417d8-102">Bewerking AssertQubit</span><span class="sxs-lookup"><span data-stu-id="417d8-102">AssertQubit operation</span></span>

<span data-ttu-id="417d8-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="417d8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="417d8-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="417d8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="417d8-105">Beweringen dat de Qubit `q` zich in de verwachte eigenstate van de Pauli Z-operator bevindt.</span><span class="sxs-lookup"><span data-stu-id="417d8-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.</span></span>

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="417d8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="417d8-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="417d8-107">verwacht: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="417d8-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="417d8-108">In welke staat wordt verwacht dat Qubit zich in: of bevindt `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="417d8-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="417d8-109">v: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="417d8-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="417d8-110">De Qubit waarvan de status wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="417d8-110">The qubit whose state is asserted.</span></span>



## <a name="output--unit"></a><span data-ttu-id="417d8-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="417d8-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="417d8-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="417d8-112">Remarks</span></span>

<span data-ttu-id="417d8-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Hiermee kunnen wille keurige Qubit-statussen worden bevestigd in plaats van alleen $Z $ eigenstates.</span><span class="sxs-lookup"><span data-stu-id="417d8-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="417d8-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="417d8-114">See Also</span></span>

- [<span data-ttu-id="417d8-115">Micro soft. Quantum. Diagnostics. AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="417d8-115">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)