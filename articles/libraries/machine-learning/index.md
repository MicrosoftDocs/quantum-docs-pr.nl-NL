---
title: Inleiding tot het kwantumpakket voor machine learning | Microsoft Docs
description: Inleiding tot het kwantumpakket voor machine learning
author: QuantumWriter
ms.author: alexeib@microsoft.com
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
ms.openlocfilehash: 7f22d5d3212890abc764f88693937b534466170f
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907848"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a>Inleiding tot de kwantumbibliotheek voor machine learning

De kwantumbibliotheek voor machine learning is een API, geschreven in Q#, waarmee u hybride kwantum/klassieke machine learning-experimenten kunt uitvoeren. De bibliotheek biedt u de volgende mogelijkheden:

- Uw eigen gegevens laden om te classificeren met kwantumsimulators

- Voorbeelden en zelfstudies gebruiken om kennis te maken met kwantum machine learning

U kunt beperkte prestaties verwachten in vergelijking met de huidige klassieke machine learning-frameworks (houd er rekening mee dat alles wordt uitgevoerd bovenop de technisch veeleisende simulatie van een kwantumapparaat).

Het doel van dit document is:

- Een beknopte inleiding bieden voor machine learning-hulpmiddelen (geschreven in Q\#) voor hybride kwantum/klassieke machine learning.
- Een inleiding bieden voor machine learning-concepten en dan vooral voor hoe deze kwantumcircuit-georiënteerde classificaties realiseren (ook wel sequentiële kwantumclassificaties genoemd).
- Een aantal zelfstudies bieden over de basisbeginselen, zodat u aan de slag kunt met de hulpprogram ma's in de bibliotheek.
- Bespreek de trainings- en validatiemethoden voor deze classificaties en hoe deze worden omgezet in specifieke Q\#-bewerkingen die de bibliotheek mogelijk maakt.

Het in deze bibliotheek geïmplementeerde model is gebaseerd op het kwantum-klassieke trainingsschema dat wordt beschreven in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)
