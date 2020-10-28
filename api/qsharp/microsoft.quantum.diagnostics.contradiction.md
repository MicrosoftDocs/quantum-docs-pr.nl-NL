---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Functie tegen strijdigheid
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702710"
---
# <a name="contradiction-function"></a><span data-ttu-id="68274-102">Functie tegen strijdigheid</span><span class="sxs-lookup"><span data-stu-id="68274-102">Contradiction function</span></span>

<span data-ttu-id="68274-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="68274-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="68274-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="68274-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="68274-105">Declareert dat een klassieke voor waarde ONWAAR is.</span><span class="sxs-lookup"><span data-stu-id="68274-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="68274-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="68274-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="68274-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="68274-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="68274-108">De voor waarde die moet worden gedeclareerd.</span><span class="sxs-lookup"><span data-stu-id="68274-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="68274-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="68274-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="68274-110">Fout bericht teken reeks die moet worden afgedrukt in het geval dat de klassieke voor waarde waar is.</span><span class="sxs-lookup"><span data-stu-id="68274-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="68274-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="68274-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="68274-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="68274-112">See Also</span></span>

- [<span data-ttu-id="68274-113">Micro soft. Quantum. Diagnostics. fact</span><span class="sxs-lookup"><span data-stu-id="68274-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)