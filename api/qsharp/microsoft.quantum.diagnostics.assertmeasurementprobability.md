---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Bewerking AssertMeasurementProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830826"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="54aee-102">Bewerking AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="54aee-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="54aee-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="54aee-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="54aee-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="54aee-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="54aee-105">Bevestigingen die de opgegeven qubits in het gegeven Pauli meten, hebben het gegeven resultaat met de opgegeven kans, binnen een bepaalde tolerantie.</span><span class="sxs-lookup"><span data-stu-id="54aee-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="54aee-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="54aee-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="54aee-107">basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="54aee-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="54aee-108">Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="54aee-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="54aee-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="54aee-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="54aee-110">Een registratie voor het maken van de bevestiging.</span><span class="sxs-lookup"><span data-stu-id="54aee-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="54aee-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="54aee-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="54aee-112">Een verwacht resultaat van `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="54aee-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="54aee-113">Probe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="54aee-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="54aee-114">De kans dat het gegeven resultaat wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="54aee-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="54aee-115">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="54aee-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="54aee-116">Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="54aee-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="54aee-117">tol: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="54aee-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="54aee-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="54aee-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="54aee-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="54aee-119">Example</span></span>

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a><span data-ttu-id="54aee-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="54aee-120">Remarks</span></span>

<span data-ttu-id="54aee-121">Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.</span><span class="sxs-lookup"><span data-stu-id="54aee-121">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="54aee-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="54aee-122">See Also</span></span>

- [<span data-ttu-id="54aee-123">Micro soft. Quantum. Diagnostics. AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="54aee-123">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)