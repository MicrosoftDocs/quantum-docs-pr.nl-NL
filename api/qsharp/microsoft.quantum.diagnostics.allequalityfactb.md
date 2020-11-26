---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: De functie AllEqualityFactB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 79dcf65956ba9436fb6fdd452f22f35d4852d6f8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213698"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="9ed06-102">De functie AllEqualityFactB</span><span class="sxs-lookup"><span data-stu-id="9ed06-102">AllEqualityFactB function</span></span>

<span data-ttu-id="9ed06-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9ed06-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9ed06-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ed06-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ed06-105">Hierbij wordt bevestigd dat twee matrices van Boole-waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="9ed06-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="9ed06-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9ed06-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="9ed06-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="9ed06-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="9ed06-108">De matrix die wordt geproduceerd door een test case.</span><span class="sxs-lookup"><span data-stu-id="9ed06-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="9ed06-109">verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="9ed06-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="9ed06-110">De matrix die wordt verwacht van een test geval van belang.</span><span class="sxs-lookup"><span data-stu-id="9ed06-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="9ed06-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="9ed06-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="9ed06-112">Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="9ed06-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ed06-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ed06-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

