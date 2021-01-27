---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: De functie AllEqualityFactB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 725291e8b5d12683ad580d5938dadd561831e88e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853544"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="60e19-102">De functie AllEqualityFactB</span><span class="sxs-lookup"><span data-stu-id="60e19-102">AllEqualityFactB function</span></span>

<span data-ttu-id="60e19-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="60e19-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="60e19-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="60e19-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="60e19-105">Hierbij wordt bevestigd dat twee matrices van Boole-waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="60e19-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="60e19-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="60e19-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="60e19-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="60e19-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="60e19-108">De matrix die wordt geproduceerd door een test case.</span><span class="sxs-lookup"><span data-stu-id="60e19-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="60e19-109">verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="60e19-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="60e19-110">De matrix die wordt verwacht van een test geval van belang.</span><span class="sxs-lookup"><span data-stu-id="60e19-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="60e19-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="60e19-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="60e19-112">Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="60e19-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="60e19-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="60e19-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

