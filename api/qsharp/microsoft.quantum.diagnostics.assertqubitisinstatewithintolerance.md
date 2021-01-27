---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Bewerking AssertQubitIsInStateWithinTolerance
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: b40c5c4f731190c8c0d00d33718680e5448bf767
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829789"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a><span data-ttu-id="a769e-102">Bewerking AssertQubitIsInStateWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="a769e-102">AssertQubitIsInStateWithinTolerance operation</span></span>

<span data-ttu-id="a769e-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a769e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a769e-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a769e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a769e-105">Beweringen dat een Qubit de verwachte status heeft.</span><span class="sxs-lookup"><span data-stu-id="a769e-105">Asserts that a qubit in the expected state.</span></span>

<span data-ttu-id="a769e-106">`expected` vertegenwoordigt een complexe vector, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.</span><span class="sxs-lookup"><span data-stu-id="a769e-106">`expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$.</span></span>
<span data-ttu-id="a769e-107">Het eerste element van de Tuples die elk van $a $ vertegenwoordigen, $b $ het reële deel van het complexe getal is, terwijl de tweede het meest imaginaire deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="a769e-107">The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part.</span></span>
<span data-ttu-id="a769e-108">Met het laatste argument wordt de tolerantie gedefinieerd waarmee de bevestiging wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a769e-108">The last argument defines the tolerance with which assertion is made.</span></span>

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="a769e-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="a769e-109">Input</span></span>

### <a name="expected--complexcomplex"></a><span data-ttu-id="a769e-110">verwacht: ([complex](xref:Microsoft.Quantum.Math.Complex),[complex](xref:Microsoft.Quantum.Math.Complex))</span><span class="sxs-lookup"><span data-stu-id="a769e-110">expected : ([Complex](xref:Microsoft.Quantum.Math.Complex),[Complex](xref:Microsoft.Quantum.Math.Complex))</span></span>

<span data-ttu-id="a769e-111">Er werden respectievelijk complexe amplitudes verwacht voor $ \ket {0} $ en $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="a769e-111">Expected complex amplitudes for $\ket{0}$ and $\ket{1}$, respectively.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="a769e-112">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a769e-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a769e-113">Qubit waarvan de status moet worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="a769e-113">Qubit whose state is to be asserted.</span></span> <span data-ttu-id="a769e-114">Houd er rekening mee dat deze Qubit wordt verondersteld te worden gescheiden van andere toegewezen qubits en niet Entangled.</span><span class="sxs-lookup"><span data-stu-id="a769e-114">Note that this qubit is assumed to be separable from other allocated qubits, and not entangled.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="a769e-115">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a769e-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a769e-116">Toevoegings tolerantie waarbij de werkelijke amplitudes mogen afwijken van verwacht.</span><span class="sxs-lookup"><span data-stu-id="a769e-116">Additive tolerance by which actual amplitudes are allowed to deviate from expected.</span></span>
<span data-ttu-id="a769e-117">Zie de opmerkingen hieronder voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a769e-117">See remarks below for details.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a769e-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a769e-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="a769e-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a769e-119">Example</span></span>

```qsharp
using (qubits = Qubit[2]) {
    // Both qubits are initialized as |0〉: a=(1 + 0*i), b=(0 + 0*i)
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[0], 1e-5);
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[1], 1e-5);
    Y(qubits[1]);
    // Y |0〉 = i |1〉: a=(0 + 0*i), b=(0 + 1*i)
    AssertQubitIsInStateWithinTolerance((Complex(0., 0.), Complex(0., 1.)), qubits[1], 1e-5);
}
```

## <a name="remarks"></a><span data-ttu-id="a769e-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a769e-120">Remarks</span></span>

<span data-ttu-id="a769e-121">De volgende Mathematica-code kan worden gebruikt om expressies te controleren voor mi, MX, my, MZ:</span><span class="sxs-lookup"><span data-stu-id="a769e-121">The following Mathematica code can be used to verify expressions for mi, mx, my, mz:</span></span>

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

<span data-ttu-id="a769e-122">De tolerantie is de $L \_ {\infty} $ de afstand tussen de 3 dimensionale reële vector (x ₂, x ₃, x ₄) gedefinieerd door $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ en Real vector (Y ₂, y ₃, y ₄) gedefinieerd door ρ = y ₁ I + Y ₂ x + y ₃ Y + y ₄ Z waarbij ρ de dichtheids matrix is die overeenkomt met de status van het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="a769e-122">The tolerance is the $L\_{\infty}$ distance between 3 dimensional real vector (x₂,x₃,x₄) defined by $\langle\psi|\psi\rangle = x\_1 I + x\_2 X + x\_3 Y + x\_4 Z$ and real vector (y₂,y₃,y₄) defined by ρ = y₁I + y₂X + y₃Y + y₄Z where ρ is the density matrix corresponding to the state of the register.</span></span>
<span data-ttu-id="a769e-123">Dit geldt alleen voor de veronderstelling dat tr (ρ) en tr (| ψ ⟩ ⟨ ψ |) beide 1 zijn (bijvoorbeeld x ₁ = 1/2, y ₁ = 1/2).</span><span class="sxs-lookup"><span data-stu-id="a769e-123">This is only true under the assumption that Tr(ρ) and Tr(|ψ⟩⟨ψ|) are both 1 (e.g. x₁ = 1/2, y₁ = 1/2).</span></span>
<span data-ttu-id="a769e-124">Als dit niet het geval is, beweringt de functie dat l ∞ afstand tussen (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) en (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) kleiner is dan de tolerantie parameter.</span><span class="sxs-lookup"><span data-stu-id="a769e-124">If this is not the case, the function asserts that l∞ distance between (x₂-x₁,x₃-x₁,x₄-x₁,x₄+x₁) and (y₂-y₁,y₃-y₁,y₄-y₁,y₄+y₁) is less than the tolerance parameter.</span></span>