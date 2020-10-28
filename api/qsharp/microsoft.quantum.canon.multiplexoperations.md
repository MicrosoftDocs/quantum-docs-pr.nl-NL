---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Bewerking MultiplexOperations
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 267c9c2858090ebe024fd387938e8bd2f8c76867
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703982"
---
# <a name="multiplexoperations-operation"></a>Bewerking MultiplexOperations

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Past een matrix van bewerkingen toe die worden beheerd door een matrix van aantal statussen.

Dat wil zeggen, een unitary-bewerking met vermenigvuldiging Toep assen $U $ waarmee een unitary $V _j $ wordt toegepast wanneer wordt bepaald door $n $-Qubit Number status $ \ket{j} $.

$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a>Invoer

### <a name="unitaries--t--unit-adj--ctl"></a>unitaries: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []

Matrix van Maxi maal $2 ^ n $ unitary-bewerkingen. De $j $ de bewerking wordt geïndexeerd door de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.


### <a name="index--littleendian"></a>index: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.


### <a name="target--t"></a>doel: 'T

Generic Qubit-REGI ster dat $V _j $ treedt op.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

`coefficients` wordt aangevuld met identiteits elementen als er minder dan $2 ^ n $ is opgegeven. Deze implementatie maakt gebruik van $n-$1 hulp qubits.

## <a name="references"></a>Naslaginformatie

- Naar de eerste Quantum simulatie met Quantum SpeedUp Andrew M. Childs, Dmitri Maslov, Yunseongy, Neil J. Rvende, Yuan su https://arxiv.org/abs/1711.10980