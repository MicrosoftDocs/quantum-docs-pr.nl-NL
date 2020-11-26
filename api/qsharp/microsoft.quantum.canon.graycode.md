---
uid: Microsoft.Quantum.Canon.GrayCode
title: De functie GrayCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206881"
---
# <a name="graycode-function"></a><span data-ttu-id="84e64-102">De functie GrayCode</span><span class="sxs-lookup"><span data-stu-id="84e64-102">GrayCode function</span></span>

<span data-ttu-id="84e64-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="84e64-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="84e64-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84e64-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84e64-105">Maakt grijze code reeksen</span><span class="sxs-lookup"><span data-stu-id="84e64-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="84e64-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="84e64-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="84e64-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="84e64-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="84e64-108">Aantal bits</span><span class="sxs-lookup"><span data-stu-id="84e64-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="84e64-109">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="84e64-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="84e64-110">De matrix van Tuples.</span><span class="sxs-lookup"><span data-stu-id="84e64-110">Array of tuples.</span></span> <span data-ttu-id="84e64-111">De eerste waarde in tuple is een waarde in de tweede waarde van de GrayCode-reeks in tuple is position om de huidige waarde te wijzigen in volgende.</span><span class="sxs-lookup"><span data-stu-id="84e64-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>