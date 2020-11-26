---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: De functie OptimizedTrotterStepOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: 04b1ea457277e0681596cb564fae3782a2d09db9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229814"
---
# <a name="optimizedtrottersteporacle-function"></a><span data-ttu-id="975f5-102">De functie OptimizedTrotterStepOracle</span><span class="sxs-lookup"><span data-stu-id="975f5-102">OptimizedTrotterStepOracle function</span></span>

<span data-ttu-id="975f5-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="975f5-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="975f5-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="975f5-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="975f5-105">Retourneert een geoptimaliseerde Trotter-stap bewerking en de para meters die nodig zijn om deze uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="975f5-105">Returns optimized Trotter step operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedTrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="975f5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="975f5-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="975f5-107">qSharpData: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="975f5-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="975f5-108">Hamiltonian beschreven door `JordanWignerEncodingData` Format.</span><span class="sxs-lookup"><span data-stu-id="975f5-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="975f5-109">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="975f5-109">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="975f5-110">Stap grootte van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="975f5-110">Step size of Trotter integrator.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="975f5-111">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="975f5-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="975f5-112">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="975f5-112">Order of Trotter integrator.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="975f5-113">Output: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="975f5-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="975f5-114">Een tuple waarbij: `Int` het aantal toegewezen qubits, `Double` is `1.0/trotterStepSize` en de bewerking is de Trotter-stap.</span><span class="sxs-lookup"><span data-stu-id="975f5-114">A tuple where: `Int` is the number of qubits allocated, `Double` is `1.0/trotterStepSize`, and the operation is the Trotter step.</span></span>