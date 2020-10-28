---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: De functie FunctionAsOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702986"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="d5fc5-102">De functie FunctionAsOperation</span><span class="sxs-lookup"><span data-stu-id="d5fc5-102">FunctionAsOperation function</span></span>

<span data-ttu-id="d5fc5-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="d5fc5-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="d5fc5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5fc5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d5fc5-105">Hiermee worden functies geconverteerd naar bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="d5fc5-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="d5fc5-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d5fc5-106">Description</span></span>

<span data-ttu-id="d5fc5-107">Een bewerking die de functie aanroept, wordt door gegeven aan een functie.</span><span class="sxs-lookup"><span data-stu-id="d5fc5-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="d5fc5-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d5fc5-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="d5fc5-109">FN: de uitvoer van invoer ></span><span class="sxs-lookup"><span data-stu-id="d5fc5-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="d5fc5-110">Een functie die moet worden geconverteerd naar een bewerking.</span><span class="sxs-lookup"><span data-stu-id="d5fc5-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="d5fc5-111">Output: ' input => ' uitvoer</span><span class="sxs-lookup"><span data-stu-id="d5fc5-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="d5fc5-112">Een bewerking `op` die `op(input)` identiek is aan `fn(input)` voor alle `input` .</span><span class="sxs-lookup"><span data-stu-id="d5fc5-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d5fc5-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d5fc5-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="d5fc5-114">' Invoer</span><span class="sxs-lookup"><span data-stu-id="d5fc5-114">'Input</span></span>

<span data-ttu-id="d5fc5-115">Invoer type van de functie die moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="d5fc5-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="d5fc5-116">' Uitvoer</span><span class="sxs-lookup"><span data-stu-id="d5fc5-116">'Output</span></span>

<span data-ttu-id="d5fc5-117">Het uitvoer type van de functie die moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="d5fc5-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5fc5-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d5fc5-118">Remarks</span></span>

<span data-ttu-id="d5fc5-119">Dit is vooral nuttig voor het door geven van functies aan functies of bewerkingen waarbij een bewerking als invoer wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="d5fc5-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>