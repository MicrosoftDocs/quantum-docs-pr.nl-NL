---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: De functie EqualityFactB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: d3163281772bda392fbdd61ad58543e22022a600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702669"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="d454d-102">De functie EqualityFactB</span><span class="sxs-lookup"><span data-stu-id="d454d-102">EqualityFactB function</span></span>

<span data-ttu-id="d454d-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d454d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d454d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d454d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d454d-105">Bevestiging dat een klassieke Boole-variabele de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="d454d-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="d454d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d454d-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="d454d-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d454d-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d454d-108">De variabele die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d454d-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="d454d-109">verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d454d-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d454d-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="d454d-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="d454d-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d454d-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="d454d-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="d454d-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d454d-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d454d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
