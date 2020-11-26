---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: De functie StatePreparationComplexCoefficients
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: 1d0efa7b83d2e8e75c4b293866f3929f357ec44b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210366"
---
# <a name="statepreparationcomplexcoefficients-function"></a><span data-ttu-id="67f31-102">De functie StatePreparationComplexCoefficients</span><span class="sxs-lookup"><span data-stu-id="67f31-102">StatePreparationComplexCoefficients function</span></span>

<span data-ttu-id="67f31-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="67f31-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="67f31-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="67f31-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="67f31-105">StatePreparationComplexCoefficients is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="67f31-105">StatePreparationComplexCoefficients has been deprecated.</span></span> <span data-ttu-id="67f31-106">Gebruik <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="67f31-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="67f31-107">Retourneert een bewerking die een specifieke Quantum status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="67f31-107">Returns an operation that prepares a specific quantum state.</span></span>

<span data-ttu-id="67f31-108">De geretourneerde bewerking $U $ een wille keurige Quantum status $ \ket{\psi} $ voorbereidt met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="67f31-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="67f31-109">De actie van U op een nieuw toegewezen REGI ster wordt gegeven door $ $ \begin{align} U\ket {0... 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="67f31-109">The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}.</span></span>
<span data-ttu-id="67f31-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="67f31-110">\end{align} $$</span></span>

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="67f31-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="67f31-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="67f31-112">coëfficiënten: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="67f31-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="67f31-113">Matrix van Maxi maal $2 ^ n $ complexe coëfficiënten die worden weer gegeven door hun absolute waarde en fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="67f31-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="67f31-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="67f31-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="67f31-115">Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="67f31-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="67f31-116">Een status-Prepare unitary-bewerking $U $.</span><span class="sxs-lookup"><span data-stu-id="67f31-116">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f31-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="67f31-117">Remarks</span></span>

<span data-ttu-id="67f31-118">Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="67f31-118">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="67f31-119">`coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="67f31-119">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>