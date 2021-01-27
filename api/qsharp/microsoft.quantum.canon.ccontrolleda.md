---
uid: Microsoft.Quantum.Canon.CControlledA
title: De functie CControlledA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 823d80182621691f4fa6f42246b3d671f3adfc3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840997"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="e26f2-102">De functie CControlledA</span><span class="sxs-lookup"><span data-stu-id="e26f2-102">CControlledA function</span></span>

<span data-ttu-id="e26f2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e26f2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e26f2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e26f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e26f2-105">Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="e26f2-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="e26f2-106">Als `false` , gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="e26f2-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="e26f2-107">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="e26f2-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="e26f2-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e26f2-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="e26f2-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="e26f2-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e26f2-110">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e26f2-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj"></a><span data-ttu-id="e26f2-111">Output: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="e26f2-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="e26f2-112">Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.</span><span class="sxs-lookup"><span data-stu-id="e26f2-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e26f2-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e26f2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e26f2-114">T</span><span class="sxs-lookup"><span data-stu-id="e26f2-114">'T</span></span>

<span data-ttu-id="e26f2-115">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e26f2-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e26f2-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e26f2-116">See Also</span></span>

- [<span data-ttu-id="e26f2-117">Micro soft. Quantum. Canon. CControlled</span><span class="sxs-lookup"><span data-stu-id="e26f2-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)