---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: De functie AllEqualityFactI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 9ccd212010ae557de5ca4ab2a38d4724c5c29aa8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702795"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="fdfe2-102">De functie AllEqualityFactI</span><span class="sxs-lookup"><span data-stu-id="fdfe2-102">AllEqualityFactI function</span></span>

<span data-ttu-id="fdfe2-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fdfe2-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fdfe2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fdfe2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fdfe2-105">Hierbij wordt bevestigd dat twee matrices van gehele waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="fdfe2-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="fdfe2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fdfe2-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="fdfe2-107">werkelijk: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fdfe2-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fdfe2-108">De matrix die wordt geproduceerd door een test case.</span><span class="sxs-lookup"><span data-stu-id="fdfe2-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="fdfe2-109">verwacht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fdfe2-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fdfe2-110">De matrix die wordt verwacht van een test geval van belang.</span><span class="sxs-lookup"><span data-stu-id="fdfe2-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="fdfe2-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="fdfe2-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="fdfe2-112">Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="fdfe2-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fdfe2-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fdfe2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

