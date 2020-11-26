---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Opgesomde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221416"
---
# <a name="enumerated-function"></a><span data-ttu-id="2c01b-102">Opgesomde functie</span><span class="sxs-lookup"><span data-stu-id="2c01b-102">Enumerated function</span></span>

<span data-ttu-id="2c01b-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2c01b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2c01b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c01b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c01b-105">Op basis van een matrix retourneert een nieuwe matrix met elementen van de oorspronkelijke matrix, samen met de indices van elk element.</span><span class="sxs-lookup"><span data-stu-id="2c01b-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="2c01b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2c01b-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="2c01b-107">matrix: ' TEle []</span><span class="sxs-lookup"><span data-stu-id="2c01b-107">array : 'TElement[]</span></span>

<span data-ttu-id="2c01b-108">Een matrix waarvan de elementen moeten worden geïnventariseerd.</span><span class="sxs-lookup"><span data-stu-id="2c01b-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="2c01b-109">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int), ' tele) []</span><span class="sxs-lookup"><span data-stu-id="2c01b-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="2c01b-110">Een nieuwe matrix met elementen van de oorspronkelijke matrix samen met de indices.</span><span class="sxs-lookup"><span data-stu-id="2c01b-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2c01b-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2c01b-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="2c01b-112">-TEle</span><span class="sxs-lookup"><span data-stu-id="2c01b-112">'TElement</span></span>

<span data-ttu-id="2c01b-113">Het type elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="2c01b-113">The type of elements of the array.</span></span>