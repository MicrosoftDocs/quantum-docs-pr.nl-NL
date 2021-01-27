---
uid: Microsoft.Quantum.Canon.GrayCode
title: De functie GrayCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: 0a9a19685f0511c44942df7d0bc8d257ad6b18c6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840502"
---
# <a name="graycode-function"></a><span data-ttu-id="66a53-102">De functie GrayCode</span><span class="sxs-lookup"><span data-stu-id="66a53-102">GrayCode function</span></span>

<span data-ttu-id="66a53-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="66a53-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="66a53-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66a53-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66a53-105">Maakt grijze code reeksen</span><span class="sxs-lookup"><span data-stu-id="66a53-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="66a53-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="66a53-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="66a53-107">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="66a53-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="66a53-108">Aantal bits</span><span class="sxs-lookup"><span data-stu-id="66a53-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="66a53-109">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="66a53-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="66a53-110">De matrix van Tuples.</span><span class="sxs-lookup"><span data-stu-id="66a53-110">Array of tuples.</span></span> <span data-ttu-id="66a53-111">De eerste waarde in tuple is een waarde in de tweede waarde van de GrayCode-reeks in tuple is position om de huidige waarde te wijzigen in volgende.</span><span class="sxs-lookup"><span data-stu-id="66a53-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>

## <a name="example"></a><span data-ttu-id="66a53-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="66a53-112">Example</span></span>

```qsharp
GrayCode(2); // [(0, 0),(1, 1),(3, 0),(2, 1)]
```