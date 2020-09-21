---
title: Wiskunde in de Q# standaard bibliotheken
description: Meer informatie over de klassieke wiskundige functies in de Q# standaard bibliotheken die worden gebruikt met de ingebouwde gegevens typen.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 55b1ef70eed1eb47ab0c6b30e2b8203c38c9a67a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833602"
---
# <a name="classical-mathematical-functions"></a>Klassieke wiskundige functies #

Deze functies worden voornamelijk gebruikt voor het gebruik van de Q# ingebouwde gegevens typen `Int` , `Double` en `Range` .

De <xref:microsoft.quantum.intrinsic.random> bewerking heeft hand tekening `(Double[] => Int)` .
Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int` .
De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index. n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.
Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.
