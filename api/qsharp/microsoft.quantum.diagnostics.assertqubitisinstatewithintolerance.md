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
# <a name="assertqubitisinstatewithintolerance-operation"></a>Bewerking AssertQubitIsInStateWithinTolerance

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Beweringen dat een Qubit de verwachte status heeft.

`expected` vertegenwoordigt een complexe vector, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.
Het eerste element van de Tuples die elk van $a $ vertegenwoordigen, $b $ het reële deel van het complexe getal is, terwijl de tweede het meest imaginaire deel uitmaakt.
Met het laatste argument wordt de tolerantie gedefinieerd waarmee de bevestiging wordt gemaakt.

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Invoer

### <a name="expected--complexcomplex"></a>verwacht: ([complex](xref:Microsoft.Quantum.Math.Complex),[complex](xref:Microsoft.Quantum.Math.Complex))

Er werden respectievelijk complexe amplitudes verwacht voor $ \ket {0} $ en $ \ket {1} $.


### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit waarvan de status moet worden bevestigd. Houd er rekening mee dat deze Qubit wordt verondersteld te worden gescheiden van andere toegewezen qubits en niet Entangled.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Toevoegings tolerantie waarbij de werkelijke amplitudes mogen afwijken van verwacht.
Zie de opmerkingen hieronder voor meer informatie.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

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

## <a name="remarks"></a>Opmerkingen

De volgende Mathematica-code kan worden gebruikt om expressies te controleren voor mi, MX, my, MZ:

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

De tolerantie is de $L \_ {\infty} $ de afstand tussen de 3 dimensionale reële vector (x ₂, x ₃, x ₄) gedefinieerd door $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ en Real vector (Y ₂, y ₃, y ₄) gedefinieerd door ρ = y ₁ I + Y ₂ x + y ₃ Y + y ₄ Z waarbij ρ de dichtheids matrix is die overeenkomt met de status van het REGI ster.
Dit geldt alleen voor de veronderstelling dat tr (ρ) en tr (| ψ ⟩ ⟨ ψ |) beide 1 zijn (bijvoorbeeld x ₁ = 1/2, y ₁ = 1/2).
Als dit niet het geval is, beweringt de functie dat l ∞ afstand tussen (x ₂-x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) en (y ₂-y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) kleiner is dan de tolerantie parameter.