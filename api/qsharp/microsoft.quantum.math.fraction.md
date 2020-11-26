---
uid: Microsoft.Quantum.Math.Fraction
title: Door de gebruiker gedefinieerd type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210672"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="3f55f-102">Door de gebruiker gedefinieerd type</span><span class="sxs-lookup"><span data-stu-id="3f55f-102">Fraction user defined type</span></span>

<span data-ttu-id="3f55f-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="3f55f-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="3f55f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f55f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f55f-105">Vertegenwoordigt een rationeel nummer van het formulier `p/q` .</span><span class="sxs-lookup"><span data-stu-id="3f55f-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="3f55f-106">Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.</span><span class="sxs-lookup"><span data-stu-id="3f55f-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="3f55f-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="3f55f-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="3f55f-108">Teller: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3f55f-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3f55f-109">De teller van de Fractie.</span><span class="sxs-lookup"><span data-stu-id="3f55f-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="3f55f-110">Noemer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3f55f-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3f55f-111">Noemer van de Fractie/</span><span class="sxs-lookup"><span data-stu-id="3f55f-111">Denominator of the fraction/</span></span>