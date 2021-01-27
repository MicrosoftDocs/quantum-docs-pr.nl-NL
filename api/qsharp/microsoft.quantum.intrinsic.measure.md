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
# <a name="measure-operation"></a><span data-ttu-id="08d4e-102">Meting bewerking</span><span class="sxs-lookup"><span data-stu-id="08d4e-102">Measure operation</span></span>

<span data-ttu-id="08d4e-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="08d4e-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="08d4e-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="08d4e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="08d4e-105">Hiermee wordt een gemeen schappelijke meting uitgevoerd van een of meer qubits in de opgegeven Pauli bases.</span><span class="sxs-lookup"><span data-stu-id="08d4e-105">Performs a joint measurement of one or more qubits in the specified Pauli bases.</span></span>

<span data-ttu-id="08d4e-106">Het resultaat van de uitvoer wordt gegeven door de distributie: \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \frac12 \braket{\psi \mid | \left (\boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align} waarbij $P _i $ het $i $ TH-element van is `bases` en waar $N = \texttt{length} (\texttt{bases}) $.</span><span class="sxs-lookup"><span data-stu-id="08d4e-106">The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$.</span></span>
<span data-ttu-id="08d4e-107">Dat wil zeggen dat de meting een `Result` $d $ zo retourneert dat de eigenvalue van het waargenomen meet effect $ (-1) ^ d $ is.</span><span class="sxs-lookup"><span data-stu-id="08d4e-107">That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.</span></span>

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="08d4e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="08d4e-108">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="08d4e-109">basees: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="08d4e-109">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="08d4e-110">Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.</span><span class="sxs-lookup"><span data-stu-id="08d4e-110">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="08d4e-111">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="08d4e-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="08d4e-112">Het REGI ster van de qubits die moeten worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="08d4e-112">Register of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="08d4e-113">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="08d4e-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="08d4e-114">`Zero` Als de $ + $1 eigenvalue wordt waargenomen en `One` als de $-$1 eigenvalue wordt waargenomen.</span><span class="sxs-lookup"><span data-stu-id="08d4e-114">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d4e-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="08d4e-115">Remarks</span></span>

<span data-ttu-id="08d4e-116">Als de matrix basis en Qubit verschillende lengten hebben, mislukt de bewerking.</span><span class="sxs-lookup"><span data-stu-id="08d4e-116">If the basis array and qubit array are different lengths, then the operation will fail.</span></span>