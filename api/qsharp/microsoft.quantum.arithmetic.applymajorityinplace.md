---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Bewerking ApplyMajorityInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 3664ffe96cd1db8cf5e8898387fe7f2d45b4ea98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707596"
---
# <a name="applymajorityinplace-operation"></a>Bewerking ApplyMajorityInPlace

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Hiermee wordt de Qubit-hoofd bewerking in-place toegepast op een REGI ster van qubits.

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit
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

