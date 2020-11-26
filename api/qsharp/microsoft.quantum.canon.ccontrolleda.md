---
uid: Microsoft.Quantum.Canon.CControlledA
title: De functie CControlledA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: cb72ca5b3dab99b9ee8a994ba9fde46e0eae5594
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207510"
---
# <a name="ccontrolleda-function"></a><span data-ttu-id="a4f60-102">De functie CControlledA</span><span class="sxs-lookup"><span data-stu-id="a4f60-102">CControlledA function</span></span>

<span data-ttu-id="a4f60-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a4f60-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a4f60-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4f60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4f60-105">Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="a4f60-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="a4f60-106">Als `false` , gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="a4f60-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="a4f60-107">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="a4f60-107">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="a4f60-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="a4f60-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="a4f60-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="a4f60-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a4f60-110">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a4f60-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj"></a><span data-ttu-id="a4f60-111">Output: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="a4f60-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a4f60-112">Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.</span><span class="sxs-lookup"><span data-stu-id="a4f60-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a4f60-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a4f60-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a4f60-114">T</span><span class="sxs-lookup"><span data-stu-id="a4f60-114">'T</span></span>

<span data-ttu-id="a4f60-115">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a4f60-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4f60-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a4f60-116">See Also</span></span>

- [<span data-ttu-id="a4f60-117">Micro soft. Quantum. Canon. CControlled</span><span class="sxs-lookup"><span data-stu-id="a4f60-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)