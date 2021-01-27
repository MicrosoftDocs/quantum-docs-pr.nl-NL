---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: De functie EqualityFactCP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: a207ba1c4d08ec58095f5db34ee32c7341002920
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829175"
---
# <a name="equalityfactcp-function"></a><span data-ttu-id="99ee8-102">De functie EqualityFactCP</span><span class="sxs-lookup"><span data-stu-id="99ee8-102">EqualityFactCP function</span></span>

<span data-ttu-id="99ee8-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="99ee8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="99ee8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="99ee8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="99ee8-105">Er wordt bevestigd dat een complex getal de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="99ee8-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="99ee8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="99ee8-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="99ee8-107">werkelijk: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="99ee8-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="99ee8-108">De waarde die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="99ee8-108">The value to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="99ee8-109">verwacht: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="99ee8-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="99ee8-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="99ee8-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="99ee8-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="99ee8-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="99ee8-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="99ee8-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="99ee8-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99ee8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

