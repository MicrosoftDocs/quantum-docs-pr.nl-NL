---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: De functie StatePreparationPositiveCoefficients
ms.date: 11/25/2020 12:00:00 AM
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
ms.openlocfilehash: 8f1fd7d77531996faf566adb78f452929d6cbd50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193247"
---
# <a name="statepreparationpositivecoefficients-function"></a>De functie StatePreparationPositiveCoefficients

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> StatePreparationPositiveCoefficients is afgeschaft. Gebruik <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> in plaats daarvan.

Retourneert een bewerking die de opgegeven Quantum status voorbereidt.

De geretourneerde bewerking $U $ een wille keurige Quantum status $ \ket{\psi} $ voorbereidt met positieve coëfficiënten $ \ alpha_j \ge $0 van de $n $-Qubit reken kundige status $ \ket{0...0} $.

De actie van U op een nieuw toegewezen REGI ster wordt gegeven door $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.
\end{align} $ $

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ alpha_j $. De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een status-Prepare unitary-bewerking $U $.

## <a name="remarks"></a>Opmerkingen

Negatieve invoer coëfficiënten $ \ alpha_j < $0 worden beschouwd als positief met de waarde $ | \ alpha_j | $. `coefficients` wordt aangevuld met elementen $ \ alpha_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.