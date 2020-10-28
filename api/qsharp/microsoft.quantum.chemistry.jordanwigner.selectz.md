---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Bewerking SelectZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 171bbe28ce8f10ca4b213a94b23f8c049546e3bf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703106"
---
# <a name="selectz-operation"></a>Bewerking SelectZ

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Een unitary $U $ waarmee de Pauli $Z $-Gate wordt toegepast op een qubits $p $, voorwaarded op een index status $ \ket{p} $. Dat wil zeggen, $ $ \begin{align} U\ket {p} \ Ket {\ psi} = \ket{p}Z \_ p\ket {\ psi} \end{align} $ $

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="indexregister--littleendian"></a>indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

De status $ \ket{p} $ van dit REGI ster bepaalt de Qubit waarop $Z $ wordt toegepast.


### <a name="targetregister--qubit"></a>targetRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Het REGI ster van qubits waarop de Pauli-Opera tors worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

