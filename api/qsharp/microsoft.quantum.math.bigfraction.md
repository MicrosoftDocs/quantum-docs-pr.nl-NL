---
uid: Microsoft.Quantum.Math.BigFraction
title: Door de gebruiker gedefinieerd BigFraction-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708311"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="5337a-102">Door de gebruiker gedefinieerd BigFraction-type</span><span class="sxs-lookup"><span data-stu-id="5337a-102">BigFraction user defined type</span></span>

<span data-ttu-id="5337a-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5337a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5337a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5337a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5337a-105">Vertegenwoordigt een rationeel nummer van het formulier `p/q` .</span><span class="sxs-lookup"><span data-stu-id="5337a-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="5337a-106">Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.</span><span class="sxs-lookup"><span data-stu-id="5337a-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="5337a-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="5337a-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="5337a-108">Teller: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5337a-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5337a-109">De teller van de Fractie.</span><span class="sxs-lookup"><span data-stu-id="5337a-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="5337a-110">Noemer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5337a-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5337a-111">Noemer van de Fractie/</span><span class="sxs-lookup"><span data-stu-id="5337a-111">Denominator of the fraction/</span></span>