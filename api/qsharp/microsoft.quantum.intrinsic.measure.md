---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Meting bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: bf0a606b1bfc8c4762245422450ec26907ec1946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818768"
---
# <a name="measure-operation"></a>Meting bewerking

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Hiermee wordt een gemeen schappelijke meting uitgevoerd van een of meer qubits in de opgegeven Pauli bases.

Het resultaat van de uitvoer wordt gegeven door de distributie: \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \frac12 \braket{\psi \mid | \left (\boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align} waarbij $P _i $ het $i $ TH-element van is `bases` en waar $N = \texttt{length} (\texttt{bases}) $.
Dat wil zeggen dat de meting een `Result` $d $ zo retourneert dat de eigenvalue van het waargenomen meet effect $ (-1) ^ d $ is.

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a>Invoer

### <a name="bases--pauli"></a>basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Het REGI ster van de qubits die moeten worden gemeten.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__

`Zero` Als de $ + $1 eigenvalue wordt waargenomen en `One` als de $-$1 eigenvalue wordt waargenomen.

## <a name="remarks"></a>Opmerkingen

Als de matrix basis en Qubit verschillende lengten hebben, mislukt de bewerking.