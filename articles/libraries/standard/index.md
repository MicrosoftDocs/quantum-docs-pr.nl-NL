---
title: Introductie van de Microsoft Q#-standaardbiliotheken
description: Maak kennis met de Microsoft Q#-standaardbibliotheken die de bewerkingen, functies en gegevenstypen definiëren die worden gebruikt in kwantumprogramma's.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
ms.openlocfilehash: 820ad885e7134aa723116d4c9f853d88210a5514
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907151"
---
# <a name="introduction-to-the-q-standard-libraries"></a><span data-ttu-id="ad005-103">Inleiding in de Q#-standaardbiliotheken</span><span class="sxs-lookup"><span data-stu-id="ad005-103">Introduction to the Q# Standard Libraries</span></span> #

<span data-ttu-id="ad005-104">Q# wordt ondersteund door veel nuttige bewerkingen, functies en door de gebruiker gedefinieerde typen, die samen de Q#-*standaardbibliotheken* vormen.</span><span class="sxs-lookup"><span data-stu-id="ad005-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard libraries*.</span></span>
<span data-ttu-id="ad005-105">Het [NuGet-pakket `Microsoft.Quantum.Development.Kit`](https://www.nuget.org/packages/microsoft.quantum.development.kit), dat tijdens de [installatie en validatie](xref:microsoft.quantum.install) is geïnstalleerd, bevat de Q#-compiler, evenals delen van de standaardbibliotheek die door de doelmachines worden geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="ad005-105">The [`Microsoft.Quantum.Development.Kit` NuGet package](https://www.nuget.org/packages/microsoft.quantum.development.kit) installed during [installation and validation](xref:microsoft.quantum.install) provides the Q# compiler, and parts of the standard library that are implemented by the target machines.</span></span>
<span data-ttu-id="ad005-106">Het [pakket `Microsoft.Quantum.Standard`](https://www.nuget.org/packages/microsoft.quantum.standard) bevat de delen van de Q#-standaardbibliotheken die overdraagbaar zijn tussen de doelmachines.</span><span class="sxs-lookup"><span data-stu-id="ad005-106">The [`Microsoft.Quantum.Standard` package](https://www.nuget.org/packages/microsoft.quantum.standard) provides the portion of the Q# standard libraries that are portable across target machines.</span></span>

<span data-ttu-id="ad005-107">De symbolen die door de Q#-standaardbibliotheken zijn gedefinieerd, worden in de [API-documentatie](xref:microsoft.quantum.standardlibsintro) veel uitgebreider en gedetailleerder beschreven.</span><span class="sxs-lookup"><span data-stu-id="ad005-107">The symbols defined by the Q# standard libraries are defined in much greater and more exhaustive detail in the [API documentation](xref:microsoft.quantum.standardlibsintro).</span></span>

<span data-ttu-id="ad005-108">In de volgende secties beschrijven we de meest relevante functies uit de standaardbibliotheek en geven we enige context voor het gebruik van elke functie in de praktijk.</span><span class="sxs-lookup"><span data-stu-id="ad005-108">In the following sections, we will outline the most salient features of each part of the standard library and provide some context about how each feature might be used in practice.</span></span>
