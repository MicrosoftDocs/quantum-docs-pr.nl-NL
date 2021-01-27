---
uid: Microsoft.Quantum.Diagnostics.EqualityFactL
title: De functie EqualityFactL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactL
qsharp.summary: Asserts that a classical BigInt variable has the expected value.
ms.openlocfilehash: b7d37b5115c51596c1b3ed93c53a29e9f36b811d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829149"
---
# <a name="equalityfactl-function"></a><span data-ttu-id="b161f-102">De functie EqualityFactL</span><span class="sxs-lookup"><span data-stu-id="b161f-102">EqualityFactL function</span></span>

<span data-ttu-id="b161f-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b161f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b161f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b161f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b161f-105">Bevestiging dat een klassieke BigInt-variabele de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="b161f-105">Asserts that a classical BigInt variable has the expected value.</span></span>

```qsharp
function EqualityFactL (actual : BigInt, expected : BigInt, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="b161f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b161f-106">Input</span></span>

### <a name="actual--bigint"></a><span data-ttu-id="b161f-107">werkelijk: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b161f-107">actual : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b161f-108">Het getal dat moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="b161f-108">The number to be checked.</span></span>


### <a name="expected--bigint"></a><span data-ttu-id="b161f-109">verwacht: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b161f-109">expected : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b161f-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="b161f-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="b161f-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="b161f-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="b161f-112">Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="b161f-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b161f-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b161f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

