---
uid: Microsoft.Quantum.Canon.DelayedC
title: De functie DelayedC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: d8036397559b1587b806f701d89e892eea2da8f9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207005"
---
# <a name="delayedc-function"></a><span data-ttu-id="809cf-102">De functie DelayedC</span><span class="sxs-lookup"><span data-stu-id="809cf-102">DelayedC function</span></span>

<span data-ttu-id="809cf-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="809cf-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="809cf-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="809cf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="809cf-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="809cf-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="809cf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="809cf-106">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="809cf-107">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="809cf-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="809cf-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="809cf-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="809cf-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="809cf-109">arg : 'T</span></span>

<span data-ttu-id="809cf-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="809cf-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-ctl"></a><span data-ttu-id="809cf-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="809cf-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="809cf-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="809cf-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="809cf-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="809cf-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="809cf-114">T</span><span class="sxs-lookup"><span data-stu-id="809cf-114">'T</span></span>

<span data-ttu-id="809cf-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="809cf-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="809cf-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="809cf-116">See Also</span></span>

- [<span data-ttu-id="809cf-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="809cf-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="809cf-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="809cf-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)