---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Bewerking AssertMeasurement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702782"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="848ea-102">Bewerking AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="848ea-102">AssertMeasurement operation</span></span>

<span data-ttu-id="848ea-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="848ea-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="848ea-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="848ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="848ea-105">Bevestigingen die de opgegeven qubits in het opgegeven Pauli meten, zullen altijd het gegeven resultaat hebben.</span><span class="sxs-lookup"><span data-stu-id="848ea-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="848ea-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="848ea-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="848ea-107">basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="848ea-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="848ea-108">Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="848ea-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="848ea-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="848ea-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="848ea-110">Een registratie voor het maken van de bevestiging.</span><span class="sxs-lookup"><span data-stu-id="848ea-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="848ea-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="848ea-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="848ea-112">Het verwachte resultaat van `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="848ea-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="848ea-113">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="848ea-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="848ea-114">Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="848ea-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="848ea-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="848ea-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="848ea-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="848ea-116">Remarks</span></span>

<span data-ttu-id="848ea-117">Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.</span><span class="sxs-lookup"><span data-stu-id="848ea-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="848ea-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="848ea-118">See Also</span></span>

- [<span data-ttu-id="848ea-119">Micro soft. Quantum. Diagnostics. AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="848ea-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)