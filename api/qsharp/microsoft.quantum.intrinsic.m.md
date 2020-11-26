---
uid: Microsoft.Quantum.Intrinsic.M
title: M-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: ced3a617a7299e169c7a58a1cd0f83f656b2f0b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212338"
---
# <a name="m-operation"></a><span data-ttu-id="a1c3b-102">M-bewerking</span><span class="sxs-lookup"><span data-stu-id="a1c3b-102">M operation</span></span>

<span data-ttu-id="a1c3b-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a1c3b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a1c3b-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a1c3b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a1c3b-105">Hiermee wordt een meting uitgevoerd van één Qubit in de Pauli $Z $ basis.</span><span class="sxs-lookup"><span data-stu-id="a1c3b-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="a1c3b-106">Het resultaat van de uitvoer wordt gegeven door de distributie \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span><span class="sxs-lookup"><span data-stu-id="a1c3b-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="a1c3b-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="a1c3b-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="a1c3b-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="a1c3b-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="a1c3b-109">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a1c3b-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a1c3b-110">Qubit te meten.</span><span class="sxs-lookup"><span data-stu-id="a1c3b-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a1c3b-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a1c3b-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="a1c3b-112">`Zero` Als de $ + $1 eigenvalue wordt waargenomen en `One` als de $-$1 eigenvalue wordt waargenomen.</span><span class="sxs-lookup"><span data-stu-id="a1c3b-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1c3b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a1c3b-113">Remarks</span></span>

<span data-ttu-id="a1c3b-114">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="a1c3b-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```