---
uid: Microsoft.Quantum.Diagnostics.EqualityFactC
title: De functie EqualityFactC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactC
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 4c7256f9a8c84b4e105b1cbff6b18d6dd99cc441
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702674"
---
# <a name="equalityfactc-function"></a><span data-ttu-id="e8c8c-102">De functie EqualityFactC</span><span class="sxs-lookup"><span data-stu-id="e8c8c-102">EqualityFactC function</span></span>

<span data-ttu-id="e8c8c-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e8c8c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e8c8c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8c8c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8c8c-105">Er wordt bevestigd dat een complex getal de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="e8c8c-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="e8c8c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e8c8c-106">Input</span></span>

### <a name="actual--complex"></a><span data-ttu-id="e8c8c-107">werkelijk: [complex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="e8c8c-107">actual : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="e8c8c-108">De waarde die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="e8c8c-108">The value to be checked.</span></span>


### <a name="expected--complex"></a><span data-ttu-id="e8c8c-109">verwacht: [complex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="e8c8c-109">expected : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="e8c8c-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="e8c8c-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="e8c8c-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e8c8c-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e8c8c-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="e8c8c-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8c8c-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8c8c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

