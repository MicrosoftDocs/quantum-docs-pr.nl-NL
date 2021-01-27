---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationC
title: Bewerking ApplyWithInputTransformationC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationC
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: d877fedbc0caa1a9ebc87d80cbce9ab54ca20d88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850358"
---
# <a name="applywithinputtransformationc-operation"></a><span data-ttu-id="df22e-102">Bewerking ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="df22e-102">ApplyWithInputTransformationC operation</span></span>

<span data-ttu-id="df22e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="df22e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="df22e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df22e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df22e-105">Op basis van een bewerking waarbij een invoer wordt geaccepteerd, wordt met een functie die een uitvoer die compatibel is met die bewerking, en een invoer naar die functie, de bewerking toegepast met behulp van de functie om de invoer te transformeren naar een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="df22e-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl), input : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="df22e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="df22e-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="df22e-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="df22e-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="df22e-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="df22e-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="df22e-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="df22e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="df22e-110">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="df22e-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="df22e-111">invoer: ' U</span><span class="sxs-lookup"><span data-stu-id="df22e-111">input : 'U</span></span>

<span data-ttu-id="df22e-112">Een invoer voor de functie.</span><span class="sxs-lookup"><span data-stu-id="df22e-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df22e-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df22e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="df22e-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="df22e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df22e-115">T</span><span class="sxs-lookup"><span data-stu-id="df22e-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="df22e-116">' U</span><span class="sxs-lookup"><span data-stu-id="df22e-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="df22e-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="df22e-117">Example</span></span>

<span data-ttu-id="df22e-118">De volgende aanroep gebruikt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" om een bewerking die is ontworpen voor invoer, toe @"Microsoft.Quantum.Arithmetic.BigEndian" te passen op een invoer van het type @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="df22e-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="df22e-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="df22e-119">See Also</span></span>

- [<span data-ttu-id="df22e-120">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="df22e-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="df22e-121">Micro soft. Quantum. Canon. ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="df22e-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="df22e-122">Micro soft. Quantum. Canon. ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="df22e-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="df22e-123">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="df22e-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)