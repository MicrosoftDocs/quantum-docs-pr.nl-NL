---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: De functie EqualityFactB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: a87d6690e701eb1530be3134d24884a8c19357e9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201917"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="3a4fd-102">De functie EqualityFactB</span><span class="sxs-lookup"><span data-stu-id="3a4fd-102">EqualityFactB function</span></span>

<span data-ttu-id="3a4fd-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="3a4fd-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="3a4fd-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a4fd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a4fd-105">Bevestiging dat een klassieke Boole-variabele de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="3a4fd-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="3a4fd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3a4fd-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="3a4fd-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3a4fd-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3a4fd-108">De variabele die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="3a4fd-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="3a4fd-109">verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3a4fd-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3a4fd-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="3a4fd-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="3a4fd-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="3a4fd-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="3a4fd-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="3a4fd-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3a4fd-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3a4fd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

