---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Bewerking AssertQubitIsInStateWithinTolerance
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: 5d34bdac53870326dacb5a11c27c857793c3f420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702740"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a><span data-ttu-id="ca7b5-102">Bewerking AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="ca7b5-102">AssertQubitIsInStateWithinTolerance operation</span></span>

<span data-ttu-id="ca7b5-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="ca7b5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="ca7b5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca7b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ca7b5-105">Beweringen dat een Qubit de verwachte status heeft.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-105">Asserts that a qubit in the expected state.</span></span>

<span data-ttu-id="ca7b5-106">`expected` vertegenwoordigt een complexe vector, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-106">`expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$.</span></span>
<span data-ttu-id="ca7b5-107">Het eerste element van de Tuples die elk van $a $ vertegenwoordigen, $b $ het reële deel van het complexe getal is, terwijl de tweede het meest imaginaire deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-107">The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part.</span></span>
<span data-ttu-id="ca7b5-108">Met het laatste argument wordt de tolerantie gedefinieerd waarmee de bevestiging wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-108">The last argument defines the tolerance with which assertion is made.</span></span>

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="ca7b5-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="ca7b5-109">Input</span></span>

### <a name="expected--complexcomplex"></a><span data-ttu-id="ca7b5-110">verwacht: ([complex](xref:Microsoft.Quantum.Math.Complex),[complex](xref:Microsoft.Quantum.Math.Complex))</span><span class="sxs-lookup"><span data-stu-id="ca7b5-110">expected : ([Complex](xref:Microsoft.Quantum.Math.Complex),[Complex](xref:Microsoft.Quantum.Math.Complex))</span></span>

<span data-ttu-id="ca7b5-111">Er werden respectievelijk complexe amplitudes verwacht voor $ \ket {0} $ en $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-111">Expected complex amplitudes for $\ket{0}$ and $\ket{1}$, respectively.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="ca7b5-112">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ca7b5-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ca7b5-113">Qubit waarvan de status moet worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-113">Qubit whose state is to be asserted.</span></span> <span data-ttu-id="ca7b5-114">Houd er rekening mee dat deze Qubit wordt verondersteld te worden gescheiden van andere toegewezen qubits en niet Entangled.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-114">Note that this qubit is assumed to be separable from other allocated qubits, and not entangled.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="ca7b5-115">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ca7b5-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ca7b5-116">Toevoegings tolerantie waarbij de werkelijke amplitudes mogen afwijken van verwacht.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-116">Additive tolerance by which actual amplitudes are allowed to deviate from expected.</span></span>
<span data-ttu-id="ca7b5-117">Zie de opmerkingen hieronder voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-117">See remarks below for details.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ca7b5-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca7b5-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ca7b5-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ca7b5-119">Remarks</span></span>

<span data-ttu-id="ca7b5-120">De volgende Mathematica-code kan worden gebruikt om expressies te controleren voor mi, MX, my, MZ:</span><span class="sxs-lookup"><span data-stu-id="ca7b5-120">The following Mathematica code can be used to verify expressions for mi, mx, my, mz:</span></span>

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

<span data-ttu-id="ca7b5-121">De tolerantie is de $L \_ {\infty} $ de afstand tussen de 3 dimensionale reële vector (x ₂, x ₃, x ₄) gedefinieerd door $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ en Real vector (Y ₂, y ₃, y ₄) gedefinieerd door ρ = y ₁ I + Y ₂ x + y ₃ Y + y ₄ Z waarbij ρ de dichtheids matrix is die overeenkomt met de status van het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-121">The tolerance is the $L\_{\infty}$ distance between 3 dimensional real vector (x₂,x₃,x₄) defined by $\langle\psi|\psi\rangle = x\_1 I + x\_2 X + x\_3 Y + x\_4 Z$ and real vector (y₂,y₃,y₄) defined by ρ = y₁I + y₂X + y₃Y + y₄Z where ρ is the density matrix corresponding to the state of the register.</span></span>
<span data-ttu-id="ca7b5-122">Dit geldt alleen voor de veronderstelling dat tr (ρ) en tr (| ψ ⟩ ⟨ ψ |) beide 1 zijn (bijvoorbeeld x ₁ = 1/2, y ₁ = 1/2).</span><span class="sxs-lookup"><span data-stu-id="ca7b5-122">This is only true under the assumption that Tr(ρ) and Tr(|ψ⟩⟨ψ|) are both 1 (e.g. x₁ = 1/2, y₁ = 1/2).</span></span>
<span data-ttu-id="ca7b5-123">Als dit niet het geval is, beweringt de functie dat l ∞ afstand tussen (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) en (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) kleiner is dan de tolerantie parameter.</span><span class="sxs-lookup"><span data-stu-id="ca7b5-123">If this is not the case, the function asserts that l∞ distance between (x₂-x₁,x₃-x₁,x₄-x₁,x₄+x₁) and (y₂-y₁,y₃-y₁,y₄-y₁,y₄+y₁) is less than the tolerance parameter.</span></span>