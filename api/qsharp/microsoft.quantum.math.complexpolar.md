---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Door de gebruiker gedefinieerd ComplexPolar-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 174e75b82a3ee740cd4d07e5bcd091de65bbc6b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847348"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="7f08b-102">Door de gebruiker gedefinieerd ComplexPolar-type</span><span class="sxs-lookup"><span data-stu-id="7f08b-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="7f08b-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7f08b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7f08b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7f08b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7f08b-105">Vertegenwoordigt een complex getal in polaire vorm.</span><span class="sxs-lookup"><span data-stu-id="7f08b-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="7f08b-106">De polaire weer gave van een complex getal is $c = r e ^ {i t} $.</span><span class="sxs-lookup"><span data-stu-id="7f08b-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="7f08b-107">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="7f08b-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="7f08b-108">Grootte: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7f08b-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7f08b-109">De absolute waarde $r \ge $0 van $c $.</span><span class="sxs-lookup"><span data-stu-id="7f08b-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="7f08b-110">Argument: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7f08b-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7f08b-111">De fase $t \in \mathbb R $ van $c $.</span><span class="sxs-lookup"><span data-stu-id="7f08b-111">The phase $t \in \mathbb R$ of $c$.</span></span>