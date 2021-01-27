---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: De functie EqualityFactB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: cb1d4c471c528d2d3c08c92619fafd532a88c8f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829209"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="f002c-102">De functie EqualityFactB</span><span class="sxs-lookup"><span data-stu-id="f002c-102">EqualityFactB function</span></span>

<span data-ttu-id="f002c-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f002c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f002c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f002c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f002c-105">Bevestiging dat een klassieke Boole-variabele de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="f002c-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="f002c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f002c-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="f002c-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f002c-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f002c-108">De variabele die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="f002c-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="f002c-109">verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f002c-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f002c-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="f002c-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="f002c-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f002c-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="f002c-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="f002c-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f002c-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f002c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

