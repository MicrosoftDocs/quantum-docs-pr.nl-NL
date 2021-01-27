---
title: Inleiding in de bibliotheek voor kwantumchemie
description: Maak kennis met de Microsoft-bibliotheek voor kwantumchemie en ontdek hoe deze wordt gebruikt om elektronische structuurproblemen op kwantumcomputers te simuleren.
author: QuantumWriter
ms.author: ageller
ms.date: 12/11/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3fa606600db1641b9f8b86ccefebb7681f181b92
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847488"
---
# <a name="introduction-to-the-quantum-chemistry-library"></a>Inleiding in de bibliotheek voor kwantumchemie

De simulatie van fysische systemen speelt al lange tijd een centrale rol in kwantumcomputing.  Dit komt omdat algemeen wordt aangenomen dat kwantumdynamica zich lastig laat simuleren op kwantumcomputers, aangezien de complexiteit van het simuleren van een systeem exponentieel toeneemt met de omvang van dat systeem.  Het simuleren van problemen in de chemie en materiaalkunde blijft misschien wel de meest in het oog springende toepassing van quantumcomputing. Hiermee kunnen we namelijk mechanismen van chemische reacties onderzoeken die anders ver buiten ons meet- en simulatiebereik zouden liggen.  Het zou ons ook in staat stellen tot simulatie van gerelateerde elektronische materialen, zoals hogetemperatuur-supergeleiders. De lijst met toepassingen op dit gebied is eindeloos.

Met deze documentatie willen we een beknopte inleiding geven in het simuleren van elektronische structuurproblemen op kwantumcomputers. Zo krijgt de lezer meer inzicht in de rol die veel aspecten uit de bibliotheek voor hamiltoniaanse simulatie spelen op dit gebied.  We beginnen met een korte inleiding in de kwantummechanica en bespreken vervolgens hoe elektronische systemen daarin worden gemodelleerd.  Daarna bespreken we hoe dergelijke kwantumdynamica kan worden geëmuleerd met behulp van een kwantumcomputer.  Vervolgens zullen we twee methoden bespreken voor het compileren van kwantumdynamica tot reeksen van elementaire poorten: Suzuki-Trotter decomposities en qubitization.
