---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateD
title: Bewerking ApproximatelyPrepareArbitraryStateD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: 822efe08e66c43b7a3128d100e3e58a8c2ce3c2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193587"
---
# <a name="approximatelypreparearbitrarystated-operation"></a>Bewerking ApproximatelyPrepareArbitraryStateD

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een set coëfficiënten en een versleuteld Quantum REGI ster van little endian, wordt een staat voor het REGI ster die is beschreven door de gegeven coëfficiënten, voor een bepaalde aanpassings tolerantie voor bereid.

```qsharp
operation ApproximatelyPrepareArbitraryStateD (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt een wille keurige Quantum status $ \ket{\psi} $ voor bereid met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0 \cdots 0} $.
Met name de actie van deze bewerking kan worden gesimuleerd door de unitary-trans formatie $U $ die op de status alles-nullen werkt als

$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.
\end{align} $ $

## <a name="input"></a>Invoer

### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De aanpassings tolerantie die moet worden gebruikt bij het voorbereiden van de gegeven status.


### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van Maxi maal $2 ^ n $ reële coëfficiënten. De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Qubit registreert coderings nummer statussen in de indeling little endian. Dit wordt verwacht te worden geïnitialiseerd in de status van de berekening $ \ket{0...0} $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $. `coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.

## <a name="references"></a>Referenties

- Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176