---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Bewerking ApplyToEachIndexC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 387d7ea24b9251386a71b42a1f51ce70933bf6fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704948"
---
# <a name="applytoeachindexc-operation"></a><span data-ttu-id="b1305-102">Bewerking ApplyToEachIndexC</span><span class="sxs-lookup"><span data-stu-id="b1305-102">ApplyToEachIndexC operation</span></span>

<span data-ttu-id="b1305-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b1305-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b1305-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b1305-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b1305-105">Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.</span><span class="sxs-lookup"><span data-stu-id="b1305-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="b1305-106">De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="b1305-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b1305-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="b1305-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-ctl"></a><span data-ttu-id="b1305-108">singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) =>-CTL van de [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1305-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="b1305-109">Bewerking die moet worden toegepast op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="b1305-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="b1305-110">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="b1305-110">register : 'T[]</span></span>

<span data-ttu-id="b1305-111">Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b1305-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b1305-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1305-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b1305-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="b1305-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b1305-114">T</span><span class="sxs-lookup"><span data-stu-id="b1305-114">'T</span></span>

<span data-ttu-id="b1305-115">Het doel waarop elk van de bewerkingen optreedt.</span><span class="sxs-lookup"><span data-stu-id="b1305-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1305-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b1305-116">See Also</span></span>

- [<span data-ttu-id="b1305-117">Micro soft. Quantum. Canon. ApplyToEachIndex</span><span class="sxs-lookup"><span data-stu-id="b1305-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)