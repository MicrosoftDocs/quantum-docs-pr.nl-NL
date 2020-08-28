---
title: De Microsoft Quantum development kit (QDK) installeren
description: De Microsoft Quantum Development Kit installeren voor verschillende omgevingen.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3aafe78d5910027e2836f7dce72c064e75fc4436
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863712"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>De Microsoft Quantum development kit (QDK) installeren

Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering. De QDK bestaat uit:

- Q#-programmeertaal
- Een set bibliotheken voor abstractie van complexe functionaliteit in Q#
- API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren
- Hulpprogramma's om het ontwikkelen te vergemakkelijken

Q#-programma's kunnen worden uitgevoerd als zelfstandige toepassingen met Visual Studio Code of Visual Studio of via Jupyter Notebooks met de IQ# Jupyter-kernel.
Ze kunnen ook worden gekoppeld met een hostprogramma dat is geschreven in een .NET-taal (doorgaans C#) of Python, waardoor u kwantumbewerkingen kunt aanroepen vanuit een klassiek programma.

De werkstromen voor elk van deze configuraties worden beschreven en vergeleken in [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs).

Selecteer de gewenste instellingen als u wilt doorgaan met het installeren van de QDK en het maken van Q#-projecten:

[Ontwikkelen met Q#-toepassingen](xref:microsoft.quantum.install.standalone): kies deze methode als u wilt werken met Q# vanaf het opdrachtprompt. Hiervoor is geen stuurprogramma of hostprogramma vereist, zoals voor de onderstaande opties.

[Ontwikkelen met Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter): kies deze omgeving als u Q#-code wilt uitvoeren in cellen met ingesloten tekst of om interactieve zelfstudies te maken voor kwantumcomputing. 

[Ontwikkelen met Q# en Python](xref:microsoft.quantum.install.python): hiermee kunt u Python en Q# combineren om een Python-hostprogramma te maken dat Q#-bewerkingen aanroept.

[Ontwikkelen met Q# en .NET](xref:microsoft.quantum.install.cs): combineer C#, F# of VB.NET met Q# om een .NET-hostprogramma te maken dat Q#-bewerkingen aanroept.
