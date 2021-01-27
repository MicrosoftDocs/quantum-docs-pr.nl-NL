---
title: Inleiding tot Q#-standaardbibliotheken van Microsoft
description: Maak kennis met de Microsoft Q#-standaardbibliotheken waarin de bewerkingen, functies en gegevenstypen worden gedefinieerd die in kwantumprogramma's worden gebruikt.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 58e271fefba84e45c5558eeee066bc37c22bf63b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858306"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a>Inleiding tot de Q#-standaardbibliotheken

Q# wordt ondersteund door veel nuttige bewerkingen, functies en door de gebruiker gedefinieerde typen, die samen de Q# *-standaardbibliotheken* vormen.
Het [NuGet-pakket `Microsoft.Quantum.Development.Kit`](https://www.nuget.org/packages/microsoft.quantum.development.kit), dat tijdens de [installatie en validatie](xref:microsoft.quantum.install) is geïnstalleerd, bevat de Q#-compiler, evenals delen van de standaardbibliotheek die door de doelmachines worden geïmplementeerd.
Het [`Microsoft.Quantum.Standard`-pakket](https://www.nuget.org/packages/microsoft.quantum.standard) bevat de delen van de Q#-standaardbibliotheken die overdraagbaar zijn tussen de doelmachines.

De symbolen die door de Q#-standaardbibliotheken zijn gedefinieerd, worden in de [API-documentatie](xref:microsoft.quantum.apiref-intro) veel uitgebreider en gedetailleerder beschreven.

In de volgende secties beschrijven we de meest relevante functies uit de standaardbibliotheek en geven we enige context voor het gebruik van elke functie in de praktijk.
