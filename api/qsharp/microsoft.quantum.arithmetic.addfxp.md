---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Bewerking AddFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: cf1f1379b7e1c32aefb0fccb55f4d13c95c78d8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707661"
---
# <a name="addfxp-operation"></a><span data-ttu-id="81117-102">Bewerking AddFxP</span><span class="sxs-lookup"><span data-stu-id="81117-102">AddFxP operation</span></span>

<span data-ttu-id="81117-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="81117-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="81117-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81117-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81117-105">Telt twee vaste-komma nummers op die zijn opgeslagen in Quantum registers.</span><span class="sxs-lookup"><span data-stu-id="81117-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="description"></a><span data-ttu-id="81117-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="81117-106">Description</span></span>

<span data-ttu-id="81117-107">In de Staten $ \ket{f_1} $ en $ \ket{f_2} $, voert de bewerking $ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $ uit op twee vaste-punt registreren.</span><span class="sxs-lookup"><span data-stu-id="81117-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="81117-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="81117-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="81117-109">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="81117-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="81117-110">Eerste getal met vaste komma</span><span class="sxs-lookup"><span data-stu-id="81117-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="81117-111">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="81117-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="81117-112">Het tweede getal met vaste komma wordt bijgewerkt met de som van de twee invoer waarden.</span><span class="sxs-lookup"><span data-stu-id="81117-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="81117-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81117-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="81117-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="81117-114">Remarks</span></span>

<span data-ttu-id="81117-115">De huidige implementatie vereist dat de twee vaste-komma waarden dezelfde punt positie hebben ten opzichte van de minst significante bit, d.w.z. $n _i $ en $p _i $ gelijk moet zijn.</span><span class="sxs-lookup"><span data-stu-id="81117-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>