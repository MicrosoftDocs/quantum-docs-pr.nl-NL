---
title: 'Wiskunde in de standaard bibliotheken Q #'
description: 'Meer informatie over de klassieke wiskundige functies in de Q # standaard-bibliotheken die worden gebruikt met de ingebouwde gegevens typen.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906148"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="862fb-103">Klassieke wiskundige functies</span><span class="sxs-lookup"><span data-stu-id="862fb-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="862fb-104">Deze functies worden voornamelijk gebruikt om te werken met de Q # ingebouwde gegevens typen `Int`, `Double`en `Range`.</span><span class="sxs-lookup"><span data-stu-id="862fb-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="862fb-105">De <xref:microsoft.quantum.intrinsic.random> bewerking heeft hand tekening `(Double[] => Int)`.</span><span class="sxs-lookup"><span data-stu-id="862fb-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="862fb-106">Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int`.</span><span class="sxs-lookup"><span data-stu-id="862fb-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="862fb-107">De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index.</span><span class="sxs-lookup"><span data-stu-id="862fb-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="862fb-108">n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="862fb-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="862fb-109">Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.</span><span class="sxs-lookup"><span data-stu-id="862fb-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
