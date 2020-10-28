---
uid: Microsoft.Quantum.Math.Fraction
title: Door de gebruiker gedefinieerd type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708503"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="2a0df-102">Door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="2a0df-102">Fraction user defined type</span></span>

<span data-ttu-id="2a0df-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2a0df-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2a0df-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a0df-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a0df-105">Vertegenwoordigt een rationeel nummer van het formulier `p/q` .</span><span class="sxs-lookup"><span data-stu-id="2a0df-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="2a0df-106">Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.</span><span class="sxs-lookup"><span data-stu-id="2a0df-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="2a0df-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="2a0df-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="2a0df-108">Teller: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a0df-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a0df-109">De teller van de Fractie.</span><span class="sxs-lookup"><span data-stu-id="2a0df-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="2a0df-110">Noemer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a0df-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a0df-111">Noemer van de Fractie/</span><span class="sxs-lookup"><span data-stu-id="2a0df-111">Denominator of the fraction/</span></span>