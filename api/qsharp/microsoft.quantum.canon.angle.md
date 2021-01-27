---
uid: Microsoft.Quantum.Canon.Angle
title: Functie Angle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 0528f21b2d9c98b6497e28741964e6497d4d0fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842040"
---
# <a name="angle-function"></a><span data-ttu-id="4ca51-102">Functie Angle</span><span class="sxs-lookup"><span data-stu-id="4ca51-102">Angle function</span></span>

<span data-ttu-id="4ca51-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4ca51-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4ca51-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ca51-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ca51-105">Retourneert 1, als `index` heeft een oneven aantal enen en-1, als `index` een even aantal enen heeft.</span><span class="sxs-lookup"><span data-stu-id="4ca51-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="4ca51-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4ca51-106">Description</span></span>

<span data-ttu-id="4ca51-107">De waarde komt overeen met het teken van de coëfficiënt van het Rademacher-Walsh spectrum van de n-variabele en de functie voor een bepaalde toewijzing die de hoek van de draaiing bepaalt.</span><span class="sxs-lookup"><span data-stu-id="4ca51-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="4ca51-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4ca51-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="4ca51-109">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ca51-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4ca51-110">Invoer toewijzing als geheel getal (tussen 0 en 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="4ca51-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="4ca51-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ca51-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

