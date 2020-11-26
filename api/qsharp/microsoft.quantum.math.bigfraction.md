---
uid: Microsoft.Quantum.Math.BigFraction
title: Door de gebruiker gedefinieerd BigFraction-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1c9b9e350c4fa3664b2c66da05149005b1170ec3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211080"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="0e573-102">Door de gebruiker gedefinieerd BigFraction-type</span><span class="sxs-lookup"><span data-stu-id="0e573-102">BigFraction user defined type</span></span>

<span data-ttu-id="0e573-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="0e573-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="0e573-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0e573-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0e573-105">Vertegenwoordigt een rationeel nummer van het formulier `p/q` .</span><span class="sxs-lookup"><span data-stu-id="0e573-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="0e573-106">Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.</span><span class="sxs-lookup"><span data-stu-id="0e573-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="0e573-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="0e573-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="0e573-108">Teller: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0e573-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0e573-109">De teller van de Fractie.</span><span class="sxs-lookup"><span data-stu-id="0e573-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="0e573-110">Noemer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0e573-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0e573-111">Noemer van de Fractie/</span><span class="sxs-lookup"><span data-stu-id="0e573-111">Denominator of the fraction/</span></span>