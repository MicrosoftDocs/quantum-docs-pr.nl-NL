---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Bewerking AssertMeasurement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 3fbe000202abbd8a206b0c83dfa35f4546ea91cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202444"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="fa8b4-102">Bewerking AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="fa8b4-102">AssertMeasurement operation</span></span>

<span data-ttu-id="fa8b4-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fa8b4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fa8b4-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fa8b4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fa8b4-105">Bevestigingen die de opgegeven qubits in het opgegeven Pauli meten, zullen altijd het gegeven resultaat hebben.</span><span class="sxs-lookup"><span data-stu-id="fa8b4-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fa8b4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fa8b4-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="fa8b4-107">basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="fa8b4-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="fa8b4-108">Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="fa8b4-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="fa8b4-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fa8b4-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fa8b4-110">Een registratie voor het maken van de bevestiging.</span><span class="sxs-lookup"><span data-stu-id="fa8b4-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="fa8b4-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="fa8b4-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="fa8b4-112">Het verwachte resultaat van `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="fa8b4-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="fa8b4-113">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="fa8b4-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="fa8b4-114">Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="fa8b4-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fa8b4-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa8b4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fa8b4-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fa8b4-116">Remarks</span></span>

<span data-ttu-id="fa8b4-117">Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.</span><span class="sxs-lookup"><span data-stu-id="fa8b4-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa8b4-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fa8b4-118">See Also</span></span>

- [<span data-ttu-id="fa8b4-119">Micro soft. Quantum. Diagnostics. AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="fa8b4-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)