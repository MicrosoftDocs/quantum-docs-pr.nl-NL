---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Bewerking ApplyTransposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 1bd6f9580e09752f1de75927d6bb35417bb1ff21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709192"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="660fd-102">Bewerking ApplyTransposition</span><span class="sxs-lookup"><span data-stu-id="660fd-102">ApplyTransposition operation</span></span>

<span data-ttu-id="660fd-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="660fd-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="660fd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="660fd-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="660fd-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="660fd-105">Description</span></span>

<span data-ttu-id="660fd-106">Met deze bewerking wordt de amplitude in de index vervangen `a` door de amplitude bij de index `b` in de opgegeven status-vector van `register` lengte $n $.</span><span class="sxs-lookup"><span data-stu-id="660fd-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="660fd-107">Als `a` gelijk is aan `b` , wordt de status-vector niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="660fd-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="660fd-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="660fd-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="660fd-109">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="660fd-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="660fd-110">Eerste index (moet een waarde tussen 0 en $2 ^ n-$1) zijn</span><span class="sxs-lookup"><span data-stu-id="660fd-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="660fd-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="660fd-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="660fd-112">Tweede index (moet een waarde tussen 0 en $2 ^ n-$1) zijn</span><span class="sxs-lookup"><span data-stu-id="660fd-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="660fd-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="660fd-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="660fd-114">Een lijst met $n $ qubits waarop de omzetting wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="660fd-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="660fd-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="660fd-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

