---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Door de gebruiker gedefinieerd ComplexPolar-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701330"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="6b6b4-102">Door de gebruiker gedefinieerd ComplexPolar-type</span><span class="sxs-lookup"><span data-stu-id="6b6b4-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="6b6b4-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="6b6b4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="6b6b4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6b6b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6b6b4-105">Vertegenwoordigt een complex getal in polaire vorm.</span><span class="sxs-lookup"><span data-stu-id="6b6b4-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="6b6b4-106">De polaire weer gave van een complex getal is $c = r e ^ {i t} $.</span><span class="sxs-lookup"><span data-stu-id="6b6b4-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="6b6b4-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="6b6b4-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="6b6b4-108">Grootte: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6b6b4-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6b6b4-109">De absolute waarde $r \ge $0 van $c $.</span><span class="sxs-lookup"><span data-stu-id="6b6b4-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="6b6b4-110">Argument: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6b6b4-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6b6b4-111">De fase $t \in \mathbb R $ van $c $.</span><span class="sxs-lookup"><span data-stu-id="6b6b4-111">The phase $t \in \mathbb R$ of $c$.</span></span>