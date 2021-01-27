---
title: De Microsoft Quantum Development Kit (QDK) instellen
description: Meer informatie over hoe u de Microsoft Quantum Development Kit installeert voor verschillende omgevingen.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: quickstart
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15067f1762f4468345beee38c98e1b943081fc1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859028"
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

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><b>VS-code<br>(2019 of later)</b></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><b>Visual Studio<br>(2019 of later)</b></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><b>Jupyter Notebooks</b></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><b>Opdrachtregel</b></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><b>Besturingssysteemondersteuning:</b></td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Alleen in Windows</td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Windows, macOS, Linux</td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><b>Q# zelfstandig</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.jupyter">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Installeren</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><b>Q# en Python</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installeren</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><b>Q# en .NET (C#, F#)</b></td> 
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Installeren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Installeren</a></td>
        <td align="center">&#10006;</td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Installeren</a></td>
   </tr>
</table>

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
