---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorImpl
title: _JordanWignerClusterOperatorImpl bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: d8301934beedf715c533e00f32a50e76c11875f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851623"
---
# <a name="_jordanwignerclusteroperatorimpl-operation"></a><span data-ttu-id="5fce7-102">_JordanWignerClusterOperatorImpl bewerking</span><span class="sxs-lookup"><span data-stu-id="5fce7-102">_JordanWignerClusterOperatorImpl operation</span></span>

<span data-ttu-id="5fce7-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="5fce7-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="5fce7-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="5fce7-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="5fce7-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JordanWigner basis.</span><span class="sxs-lookup"><span data-stu-id="5fce7-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

<span data-ttu-id="5fce7-106">Zie [model lering van dynamische Generator](../libraries/data-structures#dynamical-generator-modeling) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5fce7-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation _JordanWignerClusterOperatorImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5fce7-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5fce7-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="5fce7-108">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="5fce7-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="5fce7-109">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JordanWigner.</span><span class="sxs-lookup"><span data-stu-id="5fce7-109">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="5fce7-110">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fce7-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fce7-111">Dummy variabele die overeenkomt met de hand tekening van simulatie algoritmen.</span><span class="sxs-lookup"><span data-stu-id="5fce7-111">Dummy variable to match signature of simulation algorithms.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5fce7-112">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5fce7-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5fce7-113">Registratie van de actie op basis van tijd-ontwikkelings operator.</span><span class="sxs-lookup"><span data-stu-id="5fce7-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fce7-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fce7-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

