---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Bewerking ApplyTransposition
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855570"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="c1757-102">Bewerking ApplyTransposition</span><span class="sxs-lookup"><span data-stu-id="c1757-102">ApplyTransposition operation</span></span>

<span data-ttu-id="c1757-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c1757-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c1757-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c1757-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c1757-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c1757-105">Description</span></span>

<span data-ttu-id="c1757-106">Met deze bewerking wordt de amplitude in de index vervangen `a` door de amplitude bij de index `b` in de opgegeven status-vector van `register` lengte $n $.</span><span class="sxs-lookup"><span data-stu-id="c1757-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="c1757-107">Als `a` gelijk is aan `b` , wordt de status-vector niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="c1757-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="c1757-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="c1757-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="c1757-109">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c1757-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c1757-110">Eerste index (moet een waarde tussen 0 en $2 ^ n-$1) zijn</span><span class="sxs-lookup"><span data-stu-id="c1757-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="c1757-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c1757-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c1757-112">Tweede index (moet een waarde tussen 0 en $2 ^ n-$1) zijn</span><span class="sxs-lookup"><span data-stu-id="c1757-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="c1757-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c1757-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c1757-114">Een lijst met $n $ qubits waarop de omzetting wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c1757-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c1757-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1757-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="c1757-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c1757-116">Example</span></span>

<span data-ttu-id="c1757-117">Bereid een uniforme superpositie voor in aantal statussen $ | 1 \ rangle $, $ | 2 \ rangle $ en $ | 3 \ rangle $ op 2 qubits.</span><span class="sxs-lookup"><span data-stu-id="c1757-117">Prepare a uniform superposition of number states $|1\rangle$, $|2\rangle$, and $|3\rangle$ on 2 qubits.</span></span>

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```