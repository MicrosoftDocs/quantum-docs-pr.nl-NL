---
uid: Microsoft.Quantum.Convert.Call
title: Aanroep bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 92c159cef878fb587b0ed514fd6660dd19527cab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214208"
---
# <a name="call-operation"></a><span data-ttu-id="15b3b-102">Aanroep bewerking</span><span class="sxs-lookup"><span data-stu-id="15b3b-102">Call operation</span></span>

<span data-ttu-id="15b3b-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="15b3b-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="15b3b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15b3b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15b3b-105">Roept een functie aan met een opgegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="15b3b-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="15b3b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="15b3b-106">Description</span></span>

<span data-ttu-id="15b3b-107">Op basis van een functie en een invoer voor die functie roept u de functie op en wordt de uitvoer geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="15b3b-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="15b3b-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="15b3b-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="15b3b-109">FN: de uitvoer van invoer ></span><span class="sxs-lookup"><span data-stu-id="15b3b-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="15b3b-110">Een functie die moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="15b3b-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="15b3b-111">invoer: ' invoer</span><span class="sxs-lookup"><span data-stu-id="15b3b-111">input : 'Input</span></span>

<span data-ttu-id="15b3b-112">De invoer die moet worden door gegeven aan de functie.</span><span class="sxs-lookup"><span data-stu-id="15b3b-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="15b3b-113">Uitvoer: uitvoer</span><span class="sxs-lookup"><span data-stu-id="15b3b-113">Output : 'Output</span></span>

<span data-ttu-id="15b3b-114">Het resultaat van het aanroepen van `fn` .</span><span class="sxs-lookup"><span data-stu-id="15b3b-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="15b3b-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="15b3b-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="15b3b-116">' Invoer</span><span class="sxs-lookup"><span data-stu-id="15b3b-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="15b3b-117">' Uitvoer</span><span class="sxs-lookup"><span data-stu-id="15b3b-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="15b3b-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="15b3b-118">Remarks</span></span>

<span data-ttu-id="15b3b-119">Deze bewerking is vooral nuttig voor het afdwingen van een functie die wordt aangeroepen op een specifieke locatie binnen een bewerking of voor het aanroepen van een functie waarbij een bewerking wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="15b3b-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>