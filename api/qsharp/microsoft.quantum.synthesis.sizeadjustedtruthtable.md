---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: De functie SizeAdjustedTruthTable
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 3480f022df7a289594b003f201d16d8bf7c29d7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709282"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="03322-102">De functie SizeAdjustedTruthTable</span><span class="sxs-lookup"><span data-stu-id="03322-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="03322-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="03322-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="03322-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03322-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03322-105">Hiermee wordt de waarheids tabel van een matrix met Booleaanse waarden aangepast op basis van het aantal variabelen</span><span class="sxs-lookup"><span data-stu-id="03322-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="03322-106">Een nieuwe matrix wordt geretourneerd met een lengte `2^numVars` , waardoor de grootte kan worden uitgebreid `table` met `false` vermeldingen of worden afgekapt op `2^numVars` elementen.</span><span class="sxs-lookup"><span data-stu-id="03322-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="03322-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="03322-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="03322-108">tabel: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="03322-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="03322-109">Waarheids tabel als een matrix met waarheids waarden</span><span class="sxs-lookup"><span data-stu-id="03322-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="03322-110">numVars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="03322-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="03322-111">Aantal variabelen</span><span class="sxs-lookup"><span data-stu-id="03322-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="03322-112">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="03322-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="03322-113">Tabel met gecorrigeerde grootte</span><span class="sxs-lookup"><span data-stu-id="03322-113">Size adjusted truth table</span></span>