---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Bewerking AssertMeasurement
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 8f5113f1d6b8e4f104af10ca330e244e95793418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853509"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="2db79-102">Bewerking AssertMeasurement</span><span class="sxs-lookup"><span data-stu-id="2db79-102">AssertMeasurement operation</span></span>

<span data-ttu-id="2db79-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2db79-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2db79-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2db79-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2db79-105">Bevestigingen die de opgegeven qubits in het opgegeven Pauli meten, zullen altijd het gegeven resultaat hebben.</span><span class="sxs-lookup"><span data-stu-id="2db79-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2db79-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2db79-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="2db79-107">basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="2db79-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="2db79-108">Een meet effect om de kans van, uitgedrukt in een multi-Qubit Pauli-operator, te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="2db79-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="2db79-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2db79-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2db79-110">Een registratie voor het maken van de bevestiging.</span><span class="sxs-lookup"><span data-stu-id="2db79-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="2db79-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="2db79-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="2db79-112">Het verwachte resultaat van `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="2db79-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="2db79-113">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="2db79-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="2db79-114">Een bericht dat moet worden gerapporteerd als de bevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="2db79-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2db79-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2db79-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2db79-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2db79-116">Remarks</span></span>

<span data-ttu-id="2db79-117">Houd er rekening mee dat de adjoint en de gecontroleerde versies van deze bewerking de voor waarde niet controleren.</span><span class="sxs-lookup"><span data-stu-id="2db79-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="2db79-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2db79-118">See Also</span></span>

- [<span data-ttu-id="2db79-119">Micro soft. Quantum. Diagnostics. AssertMeasurementProbability</span><span class="sxs-lookup"><span data-stu-id="2db79-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)