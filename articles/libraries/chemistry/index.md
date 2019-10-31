---
title: Inleiding in het kwantumchemiepakket | Microsoft Docs
description: Inleiding in het kwantumchemiepakket
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.intro
ms.openlocfilehash: e5a9dd70874f1ae0baf4b781346278195a980a7e
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "72960427"
---
# <a name="introduction-to-the-quantum-chemistry-library"></a>Inleiding in de bibliotheek voor kwantumchemie

De simulatie van fysische systemen speelt al lange tijd een centrale rol in kwantumcomputing.  Dit komt omdat algemeen wordt aangenomen dat kwantumdynamica zich lastig laat simuleren op kwantumcomputers, aangezien de complexiteit van het simuleren van een systeem exponentieel toeneemt met de omvang van dat systeem.  Het simuleren van problemen in de chemie en materiaalkunde blijft misschien wel de meest in het oog springende toepassing van quantumcomputing. Hiermee kunnen we namelijk mechanismen van chemische reacties onderzoeken die anders ver buiten ons meet- en simulatiebereik zouden liggen.  Het zou ons ook in staat stellen tot simulatie van gerelateerde elektronische materialen, zoals hogetemperatuur-supergeleiders. De lijst met toepassingen op dit gebied is eindeloos.

Met deze documentatie willen we een beknopte inleiding geven in het simuleren van elektronische structuurproblemen op kwantumcomputers. Zo krijgt de lezer meer inzicht in de rol die veel aspecten uit de bibliotheek voor hamiltoniaanse simulatie spelen op dit gebied.  We beginnen met een korte inleiding in de kwantummechanica en bespreken vervolgens hoe elektronische systemen daarin worden gemodelleerd.  Daarna bespreken we hoe dergelijke kwantumdynamica kan worden geëmuleerd met behulp van een kwantumcomputer.  Vervolgens zullen we twee methoden bespreken voor het compileren van kwantumdynamica tot reeksen van elementaire poorten: Suzuki-Trotter decomposities en qubitization.
