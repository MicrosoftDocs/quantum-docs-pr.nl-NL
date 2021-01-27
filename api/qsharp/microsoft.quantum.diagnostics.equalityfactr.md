---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: De functie EqualityFactR
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 86d2ddff79f0bca7badd95a2fe2156c558fa7f86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853334"
---
# <a name="equalityfactr-function"></a><span data-ttu-id="b87ec-102">De functie EqualityFactR</span><span class="sxs-lookup"><span data-stu-id="b87ec-102">EqualityFactR function</span></span>

<span data-ttu-id="b87ec-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b87ec-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b87ec-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b87ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b87ec-105">Bevestiging dat een klassieke resultaat variabele de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="b87ec-105">Asserts that a classical Result variable has the expected value.</span></span>

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="b87ec-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b87ec-106">Input</span></span>

### <a name="actual--__invalidresult__"></a><span data-ttu-id="b87ec-107">werkelijk: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="b87ec-107">actual : __invalid<Result>__</span></span>

<span data-ttu-id="b87ec-108">De variabele die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="b87ec-108">The variable to be checked.</span></span>


### <a name="expected--__invalidresult__"></a><span data-ttu-id="b87ec-109">verwacht: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="b87ec-109">expected : __invalid<Result>__</span></span>

<span data-ttu-id="b87ec-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="b87ec-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="b87ec-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="b87ec-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="b87ec-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="b87ec-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b87ec-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b87ec-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

