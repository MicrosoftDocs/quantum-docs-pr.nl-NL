---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Bewerking MAJ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846551"
---
# <a name="maj-operation"></a>Bewerking MAJ

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dit past de in-place meerderheids bewerking toe op 3 qubits.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als we de status van de doel-Qubit als $ \ket{z} $ aanduiden en de invoer status van de invoer qubits als $ \ket{x} $ en $ \ket{y} $, voert deze bewerking de volgende trans formatie uit: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.

## <a name="input"></a>Invoer

### <a name="input0--qubit"></a>input0: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De eerste invoer Qubit.


### <a name="input1--qubit"></a>input1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De tweede invoer Qubit.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een Qubit waarop de functie meerderheid wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

