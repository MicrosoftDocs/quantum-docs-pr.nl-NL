---
title: De Microsoft Quantum development kit (QDK) installeren
description: De Microsoft Quantum Development Kit installeren voor verschillende omgevingen.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: ee8d210d67a20cfea3bdc36162efc47f021a6dc6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885460"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>De Microsoft Quantum development kit (QDK) installeren

Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering. De QDK bestaat uit:

- De programmeertaal Q#
- Een set bibliotheken voor abstractie van complexe functionaliteit in Q#
- API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren
- Hulpprogramma's om het ontwikkelen te vergemakkelijken

Q#-programma's kunnen worden uitgevoerd als zelfstandige toepassingen met Visual Studio Code of Visual Studio of via Jupyter Notebooks met de IQ# Jupyter-kernel.
Ze kunnen ook worden gekoppeld met een hostprogramma dat is geschreven in een .NET-taal (doorgaans C#) of Python, waardoor u kwantumbewerkingen kunt aanroepen vanuit een klassiek programma.

De werkstromen voor elk van deze configuraties worden beschreven en vergeleken in [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs).

Selecteer de gewenste instellingen als u wilt doorgaan met het installeren van de QDK en het maken van Q#-projecten:

[Ontwikkelen met Q#-opdrachtregeltoepassing](xref:microsoft.quantum.install.standalone): kies deze methode als u wilt werken met Q# vanaf de opdrachtregel. Hiervoor is geen stuurprogramma of hostprogramma vereist, zoals voor de onderstaande opties.

[Ontwikkelen met Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter): kies deze omgeving als u Q#-code wilt uitvoeren in cellen met ingesloten tekst of om interactieve zelfstudies te maken voor kwantumcomputing. 

[Ontwikkelen met Q# en Python](xref:microsoft.quantum.install.python): hiermee kunt u Python en Q# combineren om een Python-hostprogramma te maken dat Python-bewerkingen aanroept.

[Ontwikkelen met Q# en .NET](xref:microsoft.quantum.install.cs): combineer C#, F# of VB.NET met Q# om een .NET-hostprogramma te maken dat Q#-bewerkingen aanroept.
