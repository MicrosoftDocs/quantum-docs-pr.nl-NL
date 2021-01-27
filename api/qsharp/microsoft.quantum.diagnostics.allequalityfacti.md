---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: De functie AllEqualityFactI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: a7043b9c670f79e270180c583fef56b70c1a3bcb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830894"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="cd750-102">De functie AllEqualityFactI</span><span class="sxs-lookup"><span data-stu-id="cd750-102">AllEqualityFactI function</span></span>

<span data-ttu-id="cd750-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="cd750-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="cd750-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd750-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd750-105">Hierbij wordt bevestigd dat twee matrices van gehele waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="cd750-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="cd750-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd750-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="cd750-107">werkelijk: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cd750-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cd750-108">De matrix die wordt geproduceerd door een test case.</span><span class="sxs-lookup"><span data-stu-id="cd750-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="cd750-109">verwacht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cd750-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cd750-110">De matrix die wordt verwacht van een test geval van belang.</span><span class="sxs-lookup"><span data-stu-id="cd750-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="cd750-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="cd750-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="cd750-112">Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="cd750-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cd750-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd750-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

