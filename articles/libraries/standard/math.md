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
# <a name="classical-mathematical-functions"></a>Klassieke wiskundige functies #

Deze functies worden voornamelijk gebruikt om te werken met de Q # ingebouwde gegevens typen `Int`, `Double`en `Range`.

De <xref:microsoft.quantum.intrinsic.random> bewerking heeft hand tekening `(Double[] => Int)`.
Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int`.
De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index. n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.
Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.
