---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: De functie FormattedFailure
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 6b1202c8897d67e3089a88a0855c8008b3a8c2ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828278"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="d430e-102">De functie FormattedFailure</span><span class="sxs-lookup"><span data-stu-id="d430e-102">FormattedFailure function</span></span>

<span data-ttu-id="d430e-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d430e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d430e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d430e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d430e-105">Interne functie die wordt gebruikt om te mislukken met zinvolle fout berichten.</span><span class="sxs-lookup"><span data-stu-id="d430e-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="d430e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d430e-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="d430e-107">werkelijk: 'T</span><span class="sxs-lookup"><span data-stu-id="d430e-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="d430e-108">verwacht: ' 'T</span><span class="sxs-lookup"><span data-stu-id="d430e-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="d430e-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d430e-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="d430e-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d430e-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d430e-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d430e-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d430e-112">T</span><span class="sxs-lookup"><span data-stu-id="d430e-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="d430e-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d430e-113">Remarks</span></span>

<span data-ttu-id="d430e-114">Deze functie is bedoeld om te worden geëmuleerd door simulatie runtimes, zodat het door sturen van opgemaakte tegen strijdigheden toestaat.</span><span class="sxs-lookup"><span data-stu-id="d430e-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>