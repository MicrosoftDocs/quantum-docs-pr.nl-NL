---
uid: Microsoft.Quantum.Canon.CControlled
title: De functie CControlled
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: f4d91471eae859b7018c9e7ea0c1c853619c484d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841016"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="15205-102">De functie CControlled</span><span class="sxs-lookup"><span data-stu-id="15205-102">CControlled function</span></span>

<span data-ttu-id="15205-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="15205-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="15205-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15205-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15205-105">Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="15205-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="15205-106">Als `false` , gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="15205-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="15205-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="15205-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="15205-108">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="15205-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="15205-109">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="15205-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="15205-110">Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="15205-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="15205-111">Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.</span><span class="sxs-lookup"><span data-stu-id="15205-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="15205-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="15205-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="15205-113">T</span><span class="sxs-lookup"><span data-stu-id="15205-113">'T</span></span>

<span data-ttu-id="15205-114">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="15205-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="15205-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="15205-115">See Also</span></span>

- [<span data-ttu-id="15205-116">Micro soft. Quantum. Canon. CControlledC</span><span class="sxs-lookup"><span data-stu-id="15205-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="15205-117">Micro soft. Quantum. Canon. CControlledA</span><span class="sxs-lookup"><span data-stu-id="15205-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="15205-118">Micro soft. Quantum. Canon. CControlledCA</span><span class="sxs-lookup"><span data-stu-id="15205-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)