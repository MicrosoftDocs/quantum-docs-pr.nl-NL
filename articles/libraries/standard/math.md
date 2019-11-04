---
title: 'Q # standaard-bibliotheken-wiskunde hulp | Microsoft Docs'
description: 'Q # standaard bibliotheken-wiskunde'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 7ac9d321f59f7cc95ad8939a4cf7c36e0c5e0491
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184454"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="e364e-103">Klassieke wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="e364e-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="e364e-104">Deze functies worden voornamelijk gebruikt om te werken met de Q # ingebouwde gegevens typen `Int`, `Double`en `Range`.</span><span class="sxs-lookup"><span data-stu-id="e364e-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="e364e-105">De <xref:microsoft.quantum.intrinsic.random> bewerking heeft hand tekening `(Double[] => Int)`.</span><span class="sxs-lookup"><span data-stu-id="e364e-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="e364e-106">Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int`.</span><span class="sxs-lookup"><span data-stu-id="e364e-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="e364e-107">De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index.</span><span class="sxs-lookup"><span data-stu-id="e364e-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="e364e-108">n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e364e-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="e364e-109">Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.</span><span class="sxs-lookup"><span data-stu-id="e364e-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>