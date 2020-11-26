---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: De functie AllEqualityFactI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 92b57f49407d558e5f8d0365c168b7890f1f4981
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223881"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="77d04-102">De functie AllEqualityFactI</span><span class="sxs-lookup"><span data-stu-id="77d04-102">AllEqualityFactI function</span></span>

<span data-ttu-id="77d04-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="77d04-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="77d04-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77d04-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77d04-105">Hierbij wordt bevestigd dat twee matrices van gehele waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="77d04-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="77d04-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="77d04-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="77d04-107">werkelijk: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="77d04-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="77d04-108">De matrix die wordt geproduceerd door een test case.</span><span class="sxs-lookup"><span data-stu-id="77d04-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="77d04-109">verwacht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="77d04-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="77d04-110">De matrix die wordt verwacht van een test geval van belang.</span><span class="sxs-lookup"><span data-stu-id="77d04-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="77d04-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="77d04-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="77d04-112">Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="77d04-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77d04-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77d04-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

