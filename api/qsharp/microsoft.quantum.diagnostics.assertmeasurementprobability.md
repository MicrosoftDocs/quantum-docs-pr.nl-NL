---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Bewerking AssertMeasurementProbability
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 032b9224ad728f0637596668c2928a889deeba55
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202359"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="bab81-102">Bewerking AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="bab81-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="bab81-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="bab81-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="bab81-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bab81-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bab81-105">Bevestigingen die de opgegeven qubits in het gegeven Pauli meten, hebben het gegeven resultaat met de opgegeven kans, binnen een bepaalde tolerantie.</span><span class="sxs-lookup"><span data-stu-id="bab81-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bab81-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bab81-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="bab81-107">basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="bab81-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="bab81-108">Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="bab81-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="bab81-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bab81-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bab81-110">Een registratie voor het maken van de bevestiging.</span><span class="sxs-lookup"><span data-stu-id="bab81-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="bab81-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="bab81-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="bab81-112">Een verwacht resultaat van `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="bab81-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="bab81-113">Probe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bab81-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bab81-114">De kans dat het gegeven resultaat wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="bab81-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="bab81-115">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="bab81-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="bab81-116">Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="bab81-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="bab81-117">tol: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bab81-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="bab81-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bab81-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bab81-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="bab81-119">Remarks</span></span>

<span data-ttu-id="bab81-120">Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.</span><span class="sxs-lookup"><span data-stu-id="bab81-120">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="bab81-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bab81-121">See Also</span></span>

- [<span data-ttu-id="bab81-122">Micro soft. Quantum. Diagnostics. AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="bab81-122">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)