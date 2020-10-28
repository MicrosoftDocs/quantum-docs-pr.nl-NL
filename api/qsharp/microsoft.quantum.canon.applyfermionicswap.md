---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Bewerking ApplyFermionicSWAP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 25dd91b200700d1474cf27bf1d0fa71d57f2e09b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705380"
---
# <a name="applyfermionicswap-operation"></a>Bewerking ApplyFermionicSWAP

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee past u de Fermionic-SWAP toe.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="description"></a>Beschrijving

Hiermee wordt de qubits vervangen tijdens het Toep assen van een globale fase van-1 als beide qubits 1 zijn. Hiermee behoudt u anti-symmetrization van banen.
Zie  voor meer informatie.

Deze bewerking wordt vertegenwoordigd door de unitary-operator \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.
\end{align}

## <a name="input"></a>Invoer

### <a name="qubit1--qubit"></a>qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De eerste Qubit die moet worden omgewisseld.


### <a name="qubit2--qubit"></a>qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Het tweede Qubit dat moet worden omgewisseld.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

- [*Ryan Babbush, Nathan Wiebe, Jarrod McClean, Jeroen McClain, Hartmut neven, Garnet Kin-Lic kanaal* , arXiv: 1706.00023](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. intrinsiek. SWAP](xref:Microsoft.Quantum.Intrinsic.SWAP)