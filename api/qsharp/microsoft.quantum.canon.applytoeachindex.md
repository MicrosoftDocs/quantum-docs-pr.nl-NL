---
uid: Microsoft.Quantum.Canon.ApplyToEachIndex
title: Bewerking ApplyToEachIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndex
qsharp.summary: Applies a single-qubit operation to each indexed element in a register.
ms.openlocfilehash: 8b34dc24580a3df7ae2c13ef87a6fa10c7afd3f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844595"
---
# <a name="applytoeachindex-operation"></a><span data-ttu-id="08477-102">Bewerking ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="08477-102">ApplyToEachIndex operation</span></span>

<span data-ttu-id="08477-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="08477-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="08477-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08477-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08477-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="08477-105">Applies a single-qubit operation to each indexed element in a register.</span></span>

```qsharp
operation ApplyToEachIndex<'T> (singleElementOperation : ((Int, 'T) => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="08477-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="08477-106">Input</span></span>

### <a name="singleelementoperation--intt--unit"></a><span data-ttu-id="08477-107">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08477-107">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="08477-108">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="08477-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="08477-109">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="08477-109">register : 'T[]</span></span>

<span data-ttu-id="08477-110">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="08477-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="08477-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="08477-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="08477-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="08477-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="08477-113">T</span><span class="sxs-lookup"><span data-stu-id="08477-113">'T</span></span>

<span data-ttu-id="08477-114">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="08477-114">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="08477-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="08477-115">See Also</span></span>

- [<span data-ttu-id="08477-116">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="08477-116">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)
- [<span data-ttu-id="08477-117">Micro soft. Quantum. Canon. ApplyToEachIndexA</span><span class="sxs-lookup"><span data-stu-id="08477-117">Microsoft.Quantum.Canon.ApplyToEachIndexA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexA)
- [<span data-ttu-id="08477-118">Micro soft. Quantum. Canon. ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="08477-118">Microsoft.Quantum.Canon.ApplyToEachIndexC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexC)
- [<span data-ttu-id="08477-119">Micro soft. Quantum. Canon. ApplyToEachIndexCA</span><span class="sxs-lookup"><span data-stu-id="08477-119">Microsoft.Quantum.Canon.ApplyToEachIndexCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndexCA)