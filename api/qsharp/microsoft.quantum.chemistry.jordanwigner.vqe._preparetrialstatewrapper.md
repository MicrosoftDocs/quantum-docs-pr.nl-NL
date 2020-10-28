---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: bfd7b9ce8e8b2c8f322d676c640f8c2488655516
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703094"
---
# <a name="_preparetrialstatewrapper-operation"></a><span data-ttu-id="33f98-102">_prepareTrialStateWrapper bewerking</span><span class="sxs-lookup"><span data-stu-id="33f98-102">_prepareTrialStateWrapper operation</span></span>

<span data-ttu-id="33f98-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="33f98-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="33f98-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33f98-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33f98-105">Persoonlijke wrapper rond PrepareTrialState om deze compatibel te maken met EstimateFrequencyA door een adjoint te definiëren.</span><span class="sxs-lookup"><span data-stu-id="33f98-105">Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint.</span></span>
<span data-ttu-id="33f98-106">EstimateFrequencyA heeft ingebouwde emulatie functie bij het richten op de QuantumSimulator, waardoor de uitvoering kan worden versneld.</span><span class="sxs-lookup"><span data-stu-id="33f98-106">EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.</span></span>

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="33f98-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="33f98-107">Input</span></span>

### <a name="inputstate--intjordanwignerinputstate"></a><span data-ttu-id="33f98-108">inputState: ([int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span><span class="sxs-lookup"><span data-stu-id="33f98-108">inputState : ([Int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span></span>

<span data-ttu-id="33f98-109">De Jordan-Wigner invoer die vereist is voor het uitvoeren van PrepareTrialState.</span><span class="sxs-lookup"><span data-stu-id="33f98-109">The Jordan-Wigner input required for PrepareTrialState to run.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="33f98-110">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33f98-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33f98-111">Een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="33f98-111">A qubit register.</span></span>



## <a name="output--unit"></a><span data-ttu-id="33f98-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33f98-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

