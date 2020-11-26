---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: De functie QuantumROM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229882"
---
# <a name="quantumrom-function"></a>De functie QuantumROM

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> QuantumROM is afgeschaft. Gebruik <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> in plaats daarvan.

Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven.

Op basis van een lijst met $N $ coëfficiënten $ \ alpha_j $ wordt een unitary $U $ geretourneerd die gebruikmaakt van de Quantum-ROM-techniek voor het voorbereiden van een benadering $ \tilde\rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ van de zuivering van de dichtheids matrix $ \rho = \ sum_ {j = 0} ^ {N-1} \frac{ {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $. In deze benadering is de fout $ \epsilon $ zo dat $ | p_j-\frac{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ en $ \| \tilde\rho-\rho \| \le \epsilon $. Met andere woorden, $ $ \begin{align} U\ket {0} ^ {\lceil\ log_2 N\rceil} \ Ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\Text{garbage} _J}.
\end{align} $ $

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a>Invoer

### <a name="targeterror--double"></a>targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)

De doel fout $ \epsilon $.


### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van $N $-coëfficiënten waarmee de kans op basis status wordt opgegeven.
Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a>Output: (([int](xref:microsoft.quantum.lang-ref.int)[, int)](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit) is ADJ en CTL)

## <a name="first-parameter"></a>Eerste para meter

Een tuple `(x,(y,z))` waarbij `x = y + z` het totale aantal toegewezen qubits is, `y` het aantal qubits voor het `LittleEndian` REGI ster en `z` het aantal garbage qubits.

## <a name="second-parameter"></a>Tweede para meter

De One-norm $ \ sum_j | \ alpha_j | $ van de coëfficiënt matrix.

## <a name="third-parameter"></a>Derde para meter

De unitary $U $.

## <a name="references"></a>Referenties

- Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662