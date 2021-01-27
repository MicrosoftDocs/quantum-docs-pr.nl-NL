---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Bewerking ApplyMajorityInPlace
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 10b512392b2098663c09b2e07a09c4025da90706
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843733"
---
# <a name="applymajorityinplace-operation"></a>Bewerking ApplyMajorityInPlace

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de Qubit-hoofd bewerking in-place toegepast op een REGI ster van qubits.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt de functie in de hoofd positie op 3 qubits berekend.

Als we output Qubit als $z $ en invoer qubits als $x $ en $y $ aanduiden, voert de bewerking de volgende trans formatie uit: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.

## <a name="input"></a>Invoer

### <a name="output--qubit"></a>uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eerste invoer Qubit. Houd er rekening mee dat de uitvoer op locatie wordt berekend en opgeslagen in deze Qubit.


### <a name="input--qubit"></a>invoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Tweede en derde invoer qubits.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

