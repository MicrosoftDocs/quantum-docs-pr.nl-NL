---
title: Wiskunde in de Q# standaard bibliotheken
description: Meer informatie over de klassieke wiskundige functies in de Q# standaard bibliotheken die worden gebruikt met de ingebouwde gegevens typen.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: a2e2656f42213c8ae9e984f63f3ebf4058520532
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854002"
---
# <a name="classical-mathematical-functions"></a>Klassieke wiskundige functies #

Deze functies worden voornamelijk gebruikt voor het gebruik van de Q# ingebouwde gegevens typen `Int` , `Double` en `Range` .

De <xref:Microsoft.Quantum.Intrinsic.Random> bewerking heeft hand tekening `(Double[] => Int)` .
Er wordt een matrix van dubbele waarde gebruikt als invoer en retourneert een wille keurig geselecteerde index in de matrix als een `Int` .
De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index. n matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.
Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.
