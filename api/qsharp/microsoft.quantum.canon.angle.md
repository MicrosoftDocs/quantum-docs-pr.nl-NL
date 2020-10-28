---
uid: Microsoft.Quantum.Canon.Angle
title: Functie Angle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705524"
---
# <a name="angle-function"></a><span data-ttu-id="80f36-102">Functie Angle</span><span class="sxs-lookup"><span data-stu-id="80f36-102">Angle function</span></span>

<span data-ttu-id="80f36-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="80f36-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="80f36-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80f36-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80f36-105">Retourneert 1, als `index` heeft een oneven aantal enen en-1, als `index` een even aantal enen heeft.</span><span class="sxs-lookup"><span data-stu-id="80f36-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="80f36-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="80f36-106">Description</span></span>

<span data-ttu-id="80f36-107">De waarde komt overeen met het teken van de coëfficiënt van het Rademacher-Walsh spectrum van de n-variabele en de functie voor een bepaalde toewijzing die de hoek van de draaiing bepaalt.</span><span class="sxs-lookup"><span data-stu-id="80f36-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="80f36-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="80f36-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="80f36-109">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="80f36-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="80f36-110">Invoer toewijzing als geheel getal (tussen 0 en 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="80f36-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="80f36-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="80f36-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

