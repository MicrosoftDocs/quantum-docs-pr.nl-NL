---
uid: Microsoft.Quantum.Canon.CControlledC
title: De functie CControlledC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: a10c8f0f835fe7cbb8f2d89d521a548169613c0a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840967"
---
# <a name="ccontrolledc-function"></a><span data-ttu-id="9841e-102">De functie CControlledC</span><span class="sxs-lookup"><span data-stu-id="9841e-102">CControlledC function</span></span>

<span data-ttu-id="9841e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9841e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9841e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9841e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9841e-105">Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="9841e-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="9841e-106">Als `false` , gebeurt er niets.</span><span class="sxs-lookup"><span data-stu-id="9841e-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="9841e-107">De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="9841e-107">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="9841e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="9841e-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="9841e-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9841e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9841e-110">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9841e-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-ctl"></a><span data-ttu-id="9841e-111">Output: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9841e-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9841e-112">Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.</span><span class="sxs-lookup"><span data-stu-id="9841e-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9841e-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9841e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9841e-114">T</span><span class="sxs-lookup"><span data-stu-id="9841e-114">'T</span></span>

<span data-ttu-id="9841e-115">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9841e-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9841e-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9841e-116">See Also</span></span>

- [<span data-ttu-id="9841e-117">Micro soft. Quantum. Canon. CControlled</span><span class="sxs-lookup"><span data-stu-id="9841e-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)