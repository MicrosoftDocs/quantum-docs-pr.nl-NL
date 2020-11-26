---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: De functie EqualityFactCP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 39b55e17302f9d2e5049169e9c1a74e53a8b1115
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201849"
---
# <a name="equalityfactcp-function"></a><span data-ttu-id="6a303-102">De functie EqualityFactCP</span><span class="sxs-lookup"><span data-stu-id="6a303-102">EqualityFactCP function</span></span>

<span data-ttu-id="6a303-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6a303-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6a303-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a303-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a303-105">Er wordt bevestigd dat een complex getal de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="6a303-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="6a303-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6a303-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="6a303-107">werkelijk: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="6a303-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="6a303-108">De waarde die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="6a303-108">The value to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="6a303-109">verwacht: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="6a303-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="6a303-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="6a303-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="6a303-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="6a303-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="6a303-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="6a303-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6a303-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6a303-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

