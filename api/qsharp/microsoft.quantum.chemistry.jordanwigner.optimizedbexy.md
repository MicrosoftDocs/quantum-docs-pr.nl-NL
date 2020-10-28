---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Bewerking OptimizedBEXY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 359d347fc57be46200a218646911a7a400b4a96d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703155"
---
# <a name="optimizedbexy-operation"></a>Bewerking OptimizedBEXY

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Een unitary $U $ die de teken reeks Pauli toepast op $ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 $ op qubits $0.. p $ op index $z \in \{ 0, 1 \} $ en $p $. Dat wil zeggen, $ $ \begin{align} U\ket {z} \ Ket {p} \ Ket {\ psi} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 \ket{\psi} \end{align} $ $

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="paulibasis--qubit"></a>pauliBasis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Als deze Qubit de status $ \ket {0} $ heeft, wordt $X $ toegepast. Wanneer de status is ingesteld op $ \ket {1} $, wordt $Y $ toegepast.


### <a name="indexregister--littleendian"></a>indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

De status $ \ket{p} $ van dit REGI ster bepaalt de Qubit waarop $X $ of $Y $ wordt toegepast.


### <a name="targetregister--qubit"></a>targetRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Het REGI ster van qubits waarop de Pauli-Opera tors worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

- Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662