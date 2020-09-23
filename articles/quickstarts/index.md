---
title: De Microsoft Quantum Development Kit (QDK) instellen
description: Meer informatie over hoe u de Microsoft Quantum Development Kit installeert voor verschillende omgevingen.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834479"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a>De Microsoft Quantum Development Kit (QDK) instellen

Meer informatie over hoe u de Microsoft Quantum Development Kit (QDK) instelt voor uw omgeving, zodat u aan de slag kunt gaan met kwantumprogrammering. De QDK bestaat uit:

- Q#-programmeertaal
- Een set bibliotheken voor abstractie van complexe functionaliteit in Q#
- API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren
- Hulpprogramma's om het ontwikkelen te vergemakkelijken

Q#-programma's kunnen worden uitgevoerd als zelfstandige toepassingen met Visual Studio Code of Visual Studio, via Jupyter Notebooks met de IQ# Jupyter-kernel of gekoppeld met een hostprogramma dat is geschreven in Python of een .NET-taal (C#, F#). U kunt ook Q#-programma's online uitvoeren met [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) of [Docker](#use-the-qdk-with-docker). 

## <a name="options-for-setting-up-the-qdk"></a>Opties om de QDK in te stellen

U kunt de QDK op drie manieren gebruiken:

- [De QDK lokaal installeren](#install-the-qdk-locally)
- [De QDK online gebruiken](#use-the-qdk-online)
- [Een QDK Docker-installatiekopie gebruiken](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a>De QDK lokaal installeren

U kunt Q#-code ontwikkelen in de meest gebruikte IDE's, evenals Q# integreren met andere talen zoals Python en .NET (C#, F#).

|&nbsp; | **VS Code<br>(2019 of hoger)**| **Visual Studio<br>(2019 of hoger)** | **Jupyter Notebooks** | **Opdrachtregel**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|**Besturingssysteem** |Windows, macOS, Linux |Alleen in Windows |Windows, macOS, Linux |Windows, macOS, Linux |
|<br>**Q# zelfstandig** |<br>[Installeren](xref:microsoft.quantum.install.standalone) |<br> [Installeren](xref:microsoft.quantum.install.standalone)  |<br> [Installeren](xref:microsoft.quantum.install.jupyter) |<br>[Installeren](xref:microsoft.quantum.install.standalone)|
|**Q# en Python** |[Installeren](xref:microsoft.quantum.install.python) |[Installeren](xref:microsoft.quantum.install.python) |[Installeren](xref:microsoft.quantum.install.jupyter) |[Installeren](xref:microsoft.quantum.install.python) |
|**Q# en .NET (C#, F#)**|[Installeren](xref:microsoft.quantum.install.cs) |[Installeren](xref:microsoft.quantum.install.cs)|&#10006; |[Installeren](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a>De QDK online gebruiken

U kunt ook Q#-code ontwikkelen zonder dat u iets lokaal installeert met de volgende opties:

|Resource|Voordelen|Beperkingen|
|---|---|---|
|[**Visual Studio Codespaces**](xref:microsoft.quantum.install.standalone)|Een rijke online ontwikkelomgeving  |Vereist een Azure-abonnement en -plan |
|[**Binder**](xref:microsoft.quantum.install.binder) | Gratis online notebookervaring |Geen persistentie |

## <a name="use-the-qdk-with-docker"></a>De QDK gebruiken met Docker

U kunt ook onze QDK Docker-installatiekopie gebruiken in uw lokale Docker-installatie of in de cloud via elke service die Docker-installatiekopieën ondersteunt, bijvoorbeeld ACI.

U kunt de IQ# Docker-installatiekopie downloaden via https://github.com/microsoft/iqsharp/#using-iq-as-a-container. 

U kunt Docker ook gebruiker met een Visual Studio Code Remote Development Container om snel ontwikkelomgevingen te definiëren. Raadpleeg https://github.com/microsoft/Quantum/tree/master/.devcontainer voor meet informatie over VS Code Development Containers.

## <a name="next-steps"></a>Volgende stappen

De werkstromen voor elk van deze configuraties worden beschreven en vergeleken in [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs).
