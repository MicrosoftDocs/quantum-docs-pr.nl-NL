---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Bewerking ApplyToEachA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9485c6549ed4e1a6fb3abdfa3f85ba35579d8b0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704973"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="f6f39-102">Bewerking ApplyToEachA</span><span class="sxs-lookup"><span data-stu-id="f6f39-102">ApplyToEachA operation</span></span>

<span data-ttu-id="f6f39-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f6f39-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f6f39-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6f39-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6f39-105">Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="f6f39-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="f6f39-106">De aanpassings functie `A` geeft aan dat de bewerking met één Qubit adjointable is.</span><span class="sxs-lookup"><span data-stu-id="f6f39-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f6f39-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f6f39-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj"></a><span data-ttu-id="f6f39-108">singleElementOperation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="f6f39-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f6f39-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="f6f39-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="f6f39-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="f6f39-110">register : 'T[]</span></span>

<span data-ttu-id="f6f39-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f6f39-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f6f39-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f6f39-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f6f39-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f6f39-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f6f39-114">T</span><span class="sxs-lookup"><span data-stu-id="f6f39-114">'T</span></span>

<span data-ttu-id="f6f39-115">Het doel waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="f6f39-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6f39-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f6f39-116">See Also</span></span>

- [<span data-ttu-id="f6f39-117">Micro soft. Quantum. Canon. ApplyToEach</span><span class="sxs-lookup"><span data-stu-id="f6f39-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)