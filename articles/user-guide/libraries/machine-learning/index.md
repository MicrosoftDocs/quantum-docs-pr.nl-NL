---
title: Inleiding tot het kwantumpakket voor machine learning | Microsoft Docs
description: Inleiding tot het kwantumpakket voor machine learning
author: QuantumWriter
ms.author: alexeib
ms.date: 12/5/2019
ms.topic: conceptual
uid: microsoft.quantum.machine-learning.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1e36948a216a06d76b99cd451bbfac6f5defd7c8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858781"
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
