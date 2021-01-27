---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: De functie FunctionAsOperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833828"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="2e720-102">De functie FunctionAsOperation</span><span class="sxs-lookup"><span data-stu-id="2e720-102">FunctionAsOperation function</span></span>

<span data-ttu-id="2e720-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="2e720-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="2e720-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e720-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e720-105">Hiermee worden functies geconverteerd naar bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="2e720-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="2e720-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2e720-106">Description</span></span>

<span data-ttu-id="2e720-107">Een bewerking die de functie aanroept, wordt door gegeven aan een functie.</span><span class="sxs-lookup"><span data-stu-id="2e720-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="2e720-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="2e720-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="2e720-109">FN: de uitvoer van invoer ></span><span class="sxs-lookup"><span data-stu-id="2e720-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="2e720-110">Een functie die moet worden geconverteerd naar een bewerking.</span><span class="sxs-lookup"><span data-stu-id="2e720-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="2e720-111">Output: ' input => ' uitvoer</span><span class="sxs-lookup"><span data-stu-id="2e720-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="2e720-112">Een bewerking `op` die `op(input)` identiek is aan `fn(input)` voor alle `input` .</span><span class="sxs-lookup"><span data-stu-id="2e720-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2e720-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2e720-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="2e720-114">' Invoer</span><span class="sxs-lookup"><span data-stu-id="2e720-114">'Input</span></span>

<span data-ttu-id="2e720-115">Invoer type van de functie die moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="2e720-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="2e720-116">' Uitvoer</span><span class="sxs-lookup"><span data-stu-id="2e720-116">'Output</span></span>

<span data-ttu-id="2e720-117">Het uitvoer type van de functie die moet worden geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="2e720-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e720-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2e720-118">Remarks</span></span>

<span data-ttu-id="2e720-119">Dit is vooral nuttig voor het door geven van functies aan functies of bewerkingen waarbij een bewerking als invoer wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="2e720-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>