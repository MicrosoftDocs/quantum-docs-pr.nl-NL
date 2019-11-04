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
# <a name="classical-mathematical-functions"></a>Klassieke wiskundige functies #

Deze functies worden voornamelijk gebruikt om te werken met de Q # ingebouwde gegevens typen `Int`, `Double`en `Range`.

De <xref:microsoft.quantum.intrinsic.random> bewerking heeft hand tekening `(Double[] => Int)`.
Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int`.
De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index. n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.
Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.