---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: De functie AllEqualityFactB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 100aacccbfd5b45ac9f859cd89424b0ed4007f72
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702800"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="c4e4a-102">De functie AllEqualityFactB</span><span class="sxs-lookup"><span data-stu-id="c4e4a-102">AllEqualityFactB function</span></span>

<span data-ttu-id="c4e4a-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c4e4a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c4e4a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4e4a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4e4a-105">Hierbij wordt bevestigd dat twee matrices van Boole-waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="c4e4a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c4e4a-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="c4e4a-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c4e4a-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c4e4a-108">De matrix die wordt geproduceerd door een test case.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="c4e4a-109">verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c4e4a-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c4e4a-110">De matrix die wordt verwacht van een test geval van belang.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="c4e4a-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c4e4a-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c4e4a-112">Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4e4a-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4e4a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

