---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Door de gebruiker gedefinieerd ComplexPolar-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: a4f3a7b6ffa73271d7ac9674d8c718f6f09c0291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210978"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="17b09-102">Door de gebruiker gedefinieerd ComplexPolar-type</span><span class="sxs-lookup"><span data-stu-id="17b09-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="17b09-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="17b09-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="17b09-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="17b09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="17b09-105">Vertegenwoordigt een complex getal in polaire vorm.</span><span class="sxs-lookup"><span data-stu-id="17b09-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="17b09-106">De polaire weer gave van een complex getal is $c = r e ^ {i t} $.</span><span class="sxs-lookup"><span data-stu-id="17b09-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="17b09-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="17b09-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="17b09-108">Grootte: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="17b09-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="17b09-109">De absolute waarde $r \ge $0 van $c $.</span><span class="sxs-lookup"><span data-stu-id="17b09-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="17b09-110">Argument: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="17b09-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="17b09-111">De fase $t \in \mathbb R $ van $c $.</span><span class="sxs-lookup"><span data-stu-id="17b09-111">The phase $t \in \mathbb R$ of $c$.</span></span>