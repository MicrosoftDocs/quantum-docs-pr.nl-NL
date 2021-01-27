---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: De functie StatePreparationComplexCoefficients
ms.date: 1/23/2021 12:00:00 AM
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
ms.openlocfilehash: c16df0fe075b15cff745a6b7d5b79aac39c14d09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856139"
---
# <a name="statepreparationcomplexcoefficients-function"></a>De functie StatePreparationComplexCoefficients

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> StatePreparationComplexCoefficients is afgeschaft. Gebruik <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> in plaats daarvan.

Retourneert een bewerking die een specifieke Quantum status voorbereidt.

De geretourneerde bewerking $U $ een wille keurige Quantum status $ \ket{\psi} $ voorbereidt met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0...0} $.

De actie van U op een nieuw toegewezen REGI ster wordt gegeven door $ $ \begin{align} U\ket {0... 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.
\end{align} $ $

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="coefficients--complexpolar"></a>coëfficiënten: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]

Matrix van Maxi maal $2 ^ n $ complexe coëfficiënten die worden weer gegeven door hun absolute waarde en fase $ (r_j, t_j) $. De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een status-Prepare unitary-bewerking $U $.

## <a name="example"></a>Voorbeeld

In het volgende code fragment wordt de Quantum status $ \ket{\psi} = e ^ {i 0.1} \ SQRT {1/8} \ Ket {0} + \ SQRT {7/8} \ Ket {2} $ in de Qubit-registratie voor bereid `qubitsLE` .

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let phases = [0.1, 0.0, 0.0, 0.0];
mutable complexNumbers = new ComplexPolar[4];
for (idx in 0..3) {
    set complexNumbers[idx] = ComplexPolar(amplitudes[idx], phases[idx]);
}
let op = StatePreparationComplexCoefficients(complexNumbers);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a>Opmerkingen

Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $. `coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.