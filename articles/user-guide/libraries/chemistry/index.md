---
title: Inleiding in de bibliotheek voor kwantumchemie
description: Maak kennis met de Microsoft-bibliotheek voor kwantumchemie en ontdek hoe deze wordt gebruikt om elektronische structuurproblemen op kwantumcomputers te simuleren.
author: QuantumWriter
ms.author: ageller
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15439a34933bd561dc011acf48e669abeb031e33
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835788"
---
# <a name="introduction-to-the-quantum-chemistry-library"></a>Inleiding in de bibliotheek voor kwantumchemie

De simulatie van fysische systemen speelt al lange tijd een centrale rol in kwantumcomputing.  Dit komt omdat algemeen wordt aangenomen dat kwantumdynamica zich lastig laat simuleren op kwantumcomputers, aangezien de complexiteit van het simuleren van een systeem exponentieel toeneemt met de omvang van dat systeem.  Het simuleren van problemen in de chemie en materiaalkunde blijft misschien wel de meest in het oog springende toepassing van quantumcomputing. Hiermee kunnen we namelijk mechanismen van chemische reacties onderzoeken die anders ver buiten ons meet- en simulatiebereik zouden liggen.  Het zou ons ook in staat stellen tot simulatie van gerelateerde elektronische materialen, zoals hogetemperatuur-supergeleiders. De lijst met toepassingen op dit gebied is eindeloos.

Met deze documentatie willen we een beknopte inleiding geven in het simuleren van elektronische structuurproblemen op kwantumcomputers. Zo krijgt de lezer meer inzicht in de rol die veel aspecten uit de bibliotheek voor hamiltoniaanse simulatie spelen op dit gebied.  We beginnen met een korte inleiding in de kwantummechanica en bespreken vervolgens hoe elektronische systemen daarin worden gemodelleerd.  Daarna bespreken we hoe dergelijke kwantumdynamica kan worden geëmuleerd met behulp van een kwantumcomputer.  Vervolgens zullen we twee methoden bespreken voor het compileren van kwantumdynamica tot reeksen van elementaire poorten: Suzuki-Trotter decomposities en qubitization.
