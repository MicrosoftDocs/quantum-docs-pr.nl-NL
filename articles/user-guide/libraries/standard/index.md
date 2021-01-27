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
# <a name="introduction-to-the-no-locq-standard-libraries"></a><span data-ttu-id="3bc90-103">Inleiding tot de Q#-standaardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="3bc90-103">Introduction to the Q# Standard Libraries</span></span>

<span data-ttu-id="3bc90-104">Q# wordt ondersteund door veel nuttige bewerkingen, functies en door de gebruiker gedefinieerde typen, die samen de Q# *-standaardbibliotheken* vormen.</span><span class="sxs-lookup"><span data-stu-id="3bc90-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard libraries*.</span></span>
<span data-ttu-id="3bc90-105">Het [NuGet-pakket `Microsoft.Quantum.Development.Kit`](https://www.nuget.org/packages/microsoft.quantum.development.kit), dat tijdens de [installatie en validatie](xref:microsoft.quantum.install) is geïnstalleerd, bevat de Q#-compiler, evenals delen van de standaardbibliotheek die door de doelmachines worden geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="3bc90-105">The [`Microsoft.Quantum.Development.Kit` NuGet package](https://www.nuget.org/packages/microsoft.quantum.development.kit) installed during [installation and validation](xref:microsoft.quantum.install) provides the Q# compiler, and parts of the standard library that are implemented by the target machines.</span></span>
<span data-ttu-id="3bc90-106">Het [`Microsoft.Quantum.Standard`-pakket](https://www.nuget.org/packages/microsoft.quantum.standard) bevat de delen van de Q#-standaardbibliotheken die overdraagbaar zijn tussen de doelmachines.</span><span class="sxs-lookup"><span data-stu-id="3bc90-106">The [`Microsoft.Quantum.Standard` package](https://www.nuget.org/packages/microsoft.quantum.standard) provides the portion of the Q# standard libraries that are portable across target machines.</span></span>

<span data-ttu-id="3bc90-107">De symbolen die door de Q#-standaardbibliotheken zijn gedefinieerd, worden in de [API-documentatie](xref:microsoft.quantum.apiref-intro) veel uitgebreider en gedetailleerder beschreven.</span><span class="sxs-lookup"><span data-stu-id="3bc90-107">The symbols defined by the Q# standard libraries are defined in much greater and more exhaustive detail in the [API documentation](xref:microsoft.quantum.apiref-intro).</span></span>

<span data-ttu-id="3bc90-108">In de volgende secties beschrijven we de meest relevante functies uit de standaardbibliotheek en geven we enige context voor het gebruik van elke functie in de praktijk.</span><span class="sxs-lookup"><span data-stu-id="3bc90-108">In the following sections, we will outline the most salient features of each part of the standard library and provide some context about how each feature might be used in practice.</span></span>
