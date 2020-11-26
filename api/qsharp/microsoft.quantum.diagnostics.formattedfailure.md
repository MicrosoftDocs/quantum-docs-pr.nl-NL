---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: De functie FormattedFailure
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: da809c04059d4fd0f0ec92412a3094f5b582fd91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201696"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="a14f8-102">De functie FormattedFailure</span><span class="sxs-lookup"><span data-stu-id="a14f8-102">FormattedFailure function</span></span>

<span data-ttu-id="a14f8-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a14f8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a14f8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a14f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a14f8-105">Interne functie die wordt gebruikt om te mislukken met zinvolle fout berichten.</span><span class="sxs-lookup"><span data-stu-id="a14f8-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="a14f8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a14f8-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="a14f8-107">werkelijk: 'T</span><span class="sxs-lookup"><span data-stu-id="a14f8-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="a14f8-108">verwacht: ' 'T</span><span class="sxs-lookup"><span data-stu-id="a14f8-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="a14f8-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a14f8-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="a14f8-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a14f8-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a14f8-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a14f8-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a14f8-112">T</span><span class="sxs-lookup"><span data-stu-id="a14f8-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="a14f8-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a14f8-113">Remarks</span></span>

<span data-ttu-id="a14f8-114">Deze functie is bedoeld om te worden geëmuleerd door simulatie runtimes, zodat het door sturen van opgemaakte tegen strijdigheden toestaat.</span><span class="sxs-lookup"><span data-stu-id="a14f8-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>