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
# <a name="statepreparationpositivecoefficients-function"></a>De functie StatePreparationPositiveCoefficients

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket [](https://nuget.org/packages/)


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



## <a name="output--littleendian--unit-adj--ctl"></a>Output: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een status-Prepare unitary-bewerking $U $.

## <a name="remarks"></a>Opmerkingen

Negatieve invoer coëfficiënten $ \ alpha_j < $0 worden beschouwd als positief met de waarde $ | \ alpha_j | $. `coefficients` wordt aangevuld met elementen $ \ alpha_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.