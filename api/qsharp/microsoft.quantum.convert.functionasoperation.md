---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: De functie FunctionAsOperation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 10703818242cf6b3853f08a45bfb9094f397f6c2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224374"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="ceece-102">De functie FunctionAsOperation</span><span class="sxs-lookup"><span data-stu-id="ceece-102">FunctionAsOperation function</span></span>

<span data-ttu-id="ceece-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="ceece-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="ceece-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ceece-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ceece-105">Hiermee worden functies geconverteerd naar bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ceece-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="ceece-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ceece-106">Description</span></span>

<span data-ttu-id="ceece-107">Een bewerking die de functie aanroept, wordt door gegeven aan een functie.</span><span class="sxs-lookup"><span data-stu-id="ceece-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="ceece-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="ceece-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="ceece-109">FN: de uitvoer van invoer ></span><span class="sxs-lookup"><span data-stu-id="ceece-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="ceece-110">Een functie die moet worden geconverteerd naar een bewerking.</span><span class="sxs-lookup"><span data-stu-id="ceece-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="ceece-111">Output: ' input => ' uitvoer</span><span class="sxs-lookup"><span data-stu-id="ceece-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="ceece-112">Een bewerking `op` die `op(input)` identiek is aan `fn(input)` voor alle `input` .</span><span class="sxs-lookup"><span data-stu-id="ceece-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ceece-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ceece-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="ceece-114">' Invoer</span><span class="sxs-lookup"><span data-stu-id="ceece-114">'Input</span></span>

<span data-ttu-id="ceece-115">Invoer type van de functie die moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="ceece-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="ceece-116">' Uitvoer</span><span class="sxs-lookup"><span data-stu-id="ceece-116">'Output</span></span>

<span data-ttu-id="ceece-117">Het uitvoer type van de functie die moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="ceece-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceece-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ceece-118">Remarks</span></span>

<span data-ttu-id="ceece-119">Dit is vooral nuttig voor het door geven van functies aan functies of bewerkingen waarbij een bewerking als invoer wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="ceece-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>