---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: De functie StatePreparationPositiveCoefficients
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855849"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="9de2f-102">De functie StatePreparationPositiveCoefficients</span><span class="sxs-lookup"><span data-stu-id="9de2f-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="9de2f-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="9de2f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="9de2f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9de2f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="9de2f-105">StatePreparationPositiveCoefficients is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="9de2f-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="9de2f-106">Gebruik <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="9de2f-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="9de2f-107">Retourneert een bewerking die de opgegeven Quantum status voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="9de2f-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="9de2f-108">De geretourneerde bewerking $U $ een wille keurige Quantum status $ \ket{\psi} $ voorbereidt met positieve coëfficiënten $ \ alpha_j \ge $0 van de $n $-Qubit reken kundige status $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="9de2f-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="9de2f-109">De actie van U op een nieuw toegewezen REGI ster wordt gegeven door $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="9de2f-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="9de2f-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9de2f-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9de2f-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="9de2f-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="9de2f-112">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9de2f-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9de2f-113">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="9de2f-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="9de2f-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="9de2f-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="9de2f-115">Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="9de2f-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9de2f-116">Een status-Prepare unitary-bewerking $U $.</span><span class="sxs-lookup"><span data-stu-id="9de2f-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="9de2f-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9de2f-117">Example</span></span>

<span data-ttu-id="9de2f-118">Het volgende code fragment bereidt de Quantum status $ \ket{\psi} = \ wortel {1/8} \ Ket {0} + \ SQRT {7/8} \ Ket {2} $ voor in de Qubit-registratie `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="9de2f-118">The following snippet prepares the quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="9de2f-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9de2f-119">Remarks</span></span>

<span data-ttu-id="9de2f-120">Negatieve invoer coëfficiënten $ \ alpha_j < $0 worden beschouwd als positief met de waarde $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="9de2f-120">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="9de2f-121">`coefficients` wordt aangevuld met elementen $ \ alpha_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="9de2f-121">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>