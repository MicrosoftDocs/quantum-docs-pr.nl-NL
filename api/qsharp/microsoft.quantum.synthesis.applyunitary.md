---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Bewerking ApplyUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859163"
---
# <a name="applyunitary-operation"></a><span data-ttu-id="1b31c-102">Bewerking ApplyUnitary</span><span class="sxs-lookup"><span data-stu-id="1b31c-102">ApplyUnitary operation</span></span>

<span data-ttu-id="1b31c-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="1b31c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="1b31c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1b31c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1b31c-105">Past Gate toe die is gedefinieerd door 2 ^ n x 2 ^ n unitary matrix.</span><span class="sxs-lookup"><span data-stu-id="1b31c-105">Applies gate defined by 2^n x 2^n unitary matrix.</span></span>

<span data-ttu-id="1b31c-106">Mislukt als de matrix niet unitary of een verkeerde grootte heeft.</span><span class="sxs-lookup"><span data-stu-id="1b31c-106">Fails if matrix is not unitary, or has wrong size.</span></span>

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1b31c-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="1b31c-107">Input</span></span>

### <a name="unitary--complex"></a><span data-ttu-id="1b31c-108">unitary: [complex](xref:Microsoft.Quantum.Math.Complex)[] []</span><span class="sxs-lookup"><span data-stu-id="1b31c-108">unitary : [Complex](xref:Microsoft.Quantum.Math.Complex)[][]</span></span>

<span data-ttu-id="1b31c-109">2 ^ n x 2 ^ n unitary matrix met een beschrijving van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="1b31c-109">2^n x 2^n unitary matrix describing the operation.</span></span>
<span data-ttu-id="1b31c-110">Als de matrix niet unitary of niet een geschikte grootte heeft, genereert een uitzonde ring.</span><span class="sxs-lookup"><span data-stu-id="1b31c-110">If matrix is not unitary or not of suitable size, throws an exception.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="1b31c-111">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1b31c-111">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1b31c-112">Qubits waarvoor het bewerkings register van de lengte n moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1b31c-112">Qubits to which apply the operation - register of length n.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1b31c-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1b31c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

