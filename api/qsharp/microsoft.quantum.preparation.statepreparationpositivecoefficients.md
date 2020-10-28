---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: De functie StatePreparationPositiveCoefficients
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708178"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="89c78-102">De functie StatePreparationPositiveCoefficients</span><span class="sxs-lookup"><span data-stu-id="89c78-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="89c78-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="89c78-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="89c78-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89c78-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89c78-105">Retourneert een bewerking die de opgegeven Quantum status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="89c78-105">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="89c78-106">De geretourneerde bewerking $U $ een wille keurige Quantum status $ \ket{\psi} $ voorbereidt met positieve coëfficiënten $ \ alpha_j \ge $0 van de $n $-Qubit reken kundige status $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="89c78-106">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="89c78-107">De actie van U op een nieuw toegewezen REGI ster wordt gegeven door $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="89c78-107">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="89c78-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="89c78-108">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="89c78-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="89c78-109">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="89c78-110">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="89c78-110">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="89c78-111">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="89c78-111">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="89c78-112">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="89c78-112">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit-adj--ctl"></a><span data-ttu-id="89c78-113">Output: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="89c78-113">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="89c78-114">Een status-Prepare unitary-bewerking $U $.</span><span class="sxs-lookup"><span data-stu-id="89c78-114">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c78-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="89c78-115">Remarks</span></span>

<span data-ttu-id="89c78-116">Negatieve invoer coëfficiënten $ \ alpha_j < $0 worden beschouwd als positief met de waarde $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="89c78-116">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="89c78-117">`coefficients` wordt aangevuld met elementen $ \ alpha_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="89c78-117">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>