---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Bewerking ApplyFermionicSWAP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 0c470705843a6360df0a72374570d86571397e41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218798"
---
# <a name="applyfermionicswap-operation"></a>Bewerking ApplyFermionicSWAP

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee past u de Fermionic-SWAP toe.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
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



## <a name="references"></a>Referenties

- [*Ryan Babbush, Nathan Wiebe, Jarrod McClean, Jeroen McClain, Hartmut neven, Garnet Kin-Lic kanaal*, arXiv: 1706.00023](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. intrinsiek. SWAP](xref:Microsoft.Quantum.Intrinsic.SWAP)