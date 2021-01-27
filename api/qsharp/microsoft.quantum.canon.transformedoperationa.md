---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: De functie TransformedOperationA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: fac0fb6e03dc515892783fb4a5fa9cfc274550b8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840148"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="743c9-102">De functie TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="743c9-102">TransformedOperationA function</span></span>

<span data-ttu-id="743c9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="743c9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="743c9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="743c9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="743c9-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="743c9-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="743c9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="743c9-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="743c9-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="743c9-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="743c9-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="743c9-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="743c9-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="743c9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="743c9-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="743c9-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj"></a><span data-ttu-id="743c9-111">Uitvoer: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="743c9-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="743c9-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="743c9-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="743c9-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="743c9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="743c9-114">T</span><span class="sxs-lookup"><span data-stu-id="743c9-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="743c9-115">' U</span><span class="sxs-lookup"><span data-stu-id="743c9-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="743c9-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="743c9-116">Example</span></span>

<span data-ttu-id="743c9-117">Met de volgende aanroep wordt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" een bewerking die is ontworpen voor invoer, omgezet @"Microsoft.Quantum.Arithmetic.BigEndian" in een bewerking die invoer van het type accepteert @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="743c9-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="743c9-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="743c9-118">See Also</span></span>

- [<span data-ttu-id="743c9-119">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="743c9-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="743c9-120">Micro soft. Quantum. Canon. TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="743c9-120">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="743c9-121">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="743c9-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="743c9-122">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="743c9-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="743c9-123">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="743c9-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)