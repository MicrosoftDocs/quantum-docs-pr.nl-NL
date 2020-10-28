---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Bewerking MAJ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707205"
---
# <a name="maj-operation"></a>Bewerking MAJ

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Dit past de in-place meerderheids bewerking toe op 3 qubits.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
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

