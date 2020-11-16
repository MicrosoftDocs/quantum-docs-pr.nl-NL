---
title: 'Wiskunde in de Q# standaard bibliotheken'
description: 'Meer informatie over de klassieke wiskundige functies in de Q# standaard bibliotheken die worden gebruikt met de ingebouwde gegevens typen.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 6de1574341d67c569cd2f040ec533e263fdd386e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692050"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="80288-103">Klassieke wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="80288-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="80288-104">Deze functies worden voornamelijk gebruikt voor het gebruik van de Q# ingebouwde gegevens typen `Int` , `Double` en `Range` .</span><span class="sxs-lookup"><span data-stu-id="80288-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="80288-105">De <xref:Microsoft.Quantum.Intrinsic.Random> bewerking heeft hand tekening `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="80288-105">The <xref:Microsoft.Quantum.Intrinsic.Random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="80288-106">Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int` .</span><span class="sxs-lookup"><span data-stu-id="80288-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="80288-107">De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index.</span><span class="sxs-lookup"><span data-stu-id="80288-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="80288-108">n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="80288-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="80288-109">Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.</span><span class="sxs-lookup"><span data-stu-id="80288-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
