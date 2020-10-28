---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Gecodeerde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 6b9d21969ee90f3928b65a1c97a5b0f15157e381
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709168"
---
# <a name="encoded-function"></a><span data-ttu-id="493d0-102">Gecodeerde functie</span><span class="sxs-lookup"><span data-stu-id="493d0-102">Encoded function</span></span>

<span data-ttu-id="493d0-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="493d0-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="493d0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="493d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="493d0-105">Een waarheids tabel coderen in {1,-1} code ring</span><span class="sxs-lookup"><span data-stu-id="493d0-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="493d0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="493d0-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="493d0-107">tabel: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="493d0-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="493d0-108">Waarheids tabel als een matrix met waarheids waarden</span><span class="sxs-lookup"><span data-stu-id="493d0-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="493d0-109">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="493d0-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="493d0-110">Tabel met waarheid als matrix van {1,-1} gehele getallen</span><span class="sxs-lookup"><span data-stu-id="493d0-110">Truth table as array of {1,-1} integers</span></span>