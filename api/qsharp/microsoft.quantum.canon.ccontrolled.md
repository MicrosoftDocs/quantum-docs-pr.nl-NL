---
uid: Microsoft.Quantum.Canon.CControlled
title: De functie CControlled
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: a155b00806b17258b3f87629659bc7d786e4e11d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704412"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="37104-102">De functie CControlled</span><span class="sxs-lookup"><span data-stu-id="37104-102">CControlled function</span></span>

<span data-ttu-id="37104-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="37104-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="37104-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="37104-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="37104-105">Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="37104-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="37104-106">Als `false` , gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="37104-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="37104-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="37104-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="37104-108">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37104-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="37104-109">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="37104-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="37104-110">Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37104-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="37104-111">Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.</span><span class="sxs-lookup"><span data-stu-id="37104-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="37104-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="37104-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37104-113">T</span><span class="sxs-lookup"><span data-stu-id="37104-113">'T</span></span>

<span data-ttu-id="37104-114">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="37104-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="37104-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="37104-115">See Also</span></span>

- [<span data-ttu-id="37104-116">Micro soft. Quantum. Canon. CControlledC</span><span class="sxs-lookup"><span data-stu-id="37104-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="37104-117">Micro soft. Quantum. Canon. CControlledA</span><span class="sxs-lookup"><span data-stu-id="37104-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="37104-118">Micro soft. Quantum. Canon. CControlledCA</span><span class="sxs-lookup"><span data-stu-id="37104-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)