---
title: Wiskunde in de Q# standaard bibliotheken
description: Meer informatie over de klassieke wiskundige functies in de Q# standaard bibliotheken die worden gebruikt met de ingebouwde gegevens typen.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4a3747eaa2c91e482ded3af1279a0e40d922bfb3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868420"
---
# <a name="classical-mathematical-functions"></a>Klassieke wiskundige functies #

Deze functies worden voornamelijk gebruikt voor het gebruik van de Q# ingebouwde gegevens typen `Int` , `Double` en `Range` .

De <xref:microsoft.quantum.intrinsic.random> bewerking heeft hand tekening `(Double[] => Int)` .
Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int` .
De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index. n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.
Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.
