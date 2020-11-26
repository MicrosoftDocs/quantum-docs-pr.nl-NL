---
uid: Microsoft.Quantum.Canon.Angle
title: Functie Angle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 1d8a9c2c19469e4949f043edd1ba91021fa42e78
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219410"
---
# <a name="angle-function"></a><span data-ttu-id="01332-102">Functie Angle</span><span class="sxs-lookup"><span data-stu-id="01332-102">Angle function</span></span>

<span data-ttu-id="01332-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="01332-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="01332-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="01332-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="01332-105">Retourneert 1, als `index` heeft een oneven aantal enen en-1, als `index` een even aantal enen heeft.</span><span class="sxs-lookup"><span data-stu-id="01332-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="01332-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="01332-106">Description</span></span>

<span data-ttu-id="01332-107">De waarde komt overeen met het teken van de coëfficiënt van het Rademacher-Walsh spectrum van de n-variabele en de functie voor een bepaalde toewijzing die de hoek van de draaiing bepaalt.</span><span class="sxs-lookup"><span data-stu-id="01332-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="01332-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="01332-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="01332-109">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01332-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01332-110">Invoer toewijzing als geheel getal (tussen 0 en 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="01332-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="01332-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01332-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

