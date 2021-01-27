---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: De functie OptimizedTrotterStepOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: 523a31564ae5f054fd60161f9981c43d3467f3d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842278"
---
# <a name="optimizedtrottersteporacle-function"></a><span data-ttu-id="fba8e-102">De functie OptimizedTrotterStepOracle</span><span class="sxs-lookup"><span data-stu-id="fba8e-102">OptimizedTrotterStepOracle function</span></span>

<span data-ttu-id="fba8e-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fba8e-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="fba8e-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fba8e-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="fba8e-105">Retourneert een geoptimaliseerde Trotter-stap bewerking en de para meters die nodig zijn om deze uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="fba8e-105">Returns optimized Trotter step operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedTrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="fba8e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fba8e-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="fba8e-107">qSharpData: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="fba8e-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="fba8e-108">Hamiltonian beschreven door `JordanWignerEncodingData` Format.</span><span class="sxs-lookup"><span data-stu-id="fba8e-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="fba8e-109">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fba8e-109">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fba8e-110">Stap grootte van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="fba8e-110">Step size of Trotter integrator.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="fba8e-111">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fba8e-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fba8e-112">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="fba8e-112">Order of Trotter integrator.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="fba8e-113">Output: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="fba8e-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="fba8e-114">Een tuple waarbij: `Int` het aantal toegewezen qubits, `Double` is `1.0/trotterStepSize` en de bewerking is de Trotter-stap.</span><span class="sxs-lookup"><span data-stu-id="fba8e-114">A tuple where: `Int` is the number of qubits allocated, `Double` is `1.0/trotterStepSize`, and the operation is the Trotter step.</span></span>