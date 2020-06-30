---
title: Ontwikkelen met Q#-opdrachtregeltoepassingen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274065"
---
# <a name="develop-with-q-command-line-applications"></a>Ontwikkelen met Q#-opdrachtregeltoepassingen

Q#-programma's kunnen zelfstandig worden uitgevoerd zonder een stuurprogramma in een hosttaal, zoals C#, F# of Python.

## <a name="prerequisites"></a>Vereisten

- [.NET Core SDK 3.1 of hoger](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installatie

Hoewel u Q#-opdrachtregeltoepassingen in elke IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken voor uw Q#-toepassingen. Tijdens het ontwikkelen in deze hulpprogramma's hebt u de beschikking over een groot aantal functies.

Ga als volgt te werk om VS Code te configureren:

1. Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).
2. Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Ga als volgt te werk om Visual Studio te configureren:

1. Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.
2. Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).


## <a name="develop-with-q-using-vs-code"></a>Ontwikkelen met Q#, met behulp van VS Code

Ga als volgt te werk om de Q#-projectsjablonen te installeren:

1. Open VS Code.
2. Klik op **Weergave** -> **Opdrachtpalet**.
3. Selecteer **Q#: Installeer de projectsjablonen**.

Als de melding **Projectsjablonen zijn geïnstalleerd** wordt weergegeven, is de QDK klaar om te worden gebruikt met uw eigen toepassingen en bibliotheken.

Ga als volgt te werk om een nieuw project te maken:

1. Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.
2. Klik op **Zelfstandige consoletoepassing**.
3. Ga naar de locatie waar het project moet worden opgeslagen en klik op **Project maken**.
4. Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.
        
Controleer het project. Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.

Ga als volgt te werk om de toepassing uit te voeren:
1. Klik op **Terminal** -> **Nieuwe terminal**.
2. Voer bij de terminalprompt `dotnet run` in.
3. Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`


> [!NOTE]
> Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de VS Code Q#-extensie. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

## <a name="develop-with-q-using-visual-studio"></a>Ontwikkelen met Q# met behulp van Visual Studio

Controleer uw Visual Studio-installatie door een Q# `Hello World`-toepassing te maken.

Ga als volgt te werk om een nieuwe Q#-toepassing te maken:
1. Open Visual Studio en klik op **Bestand** -> **Nieuw** -> **Project**.
2. Typ `Q#` in het zoekvak, selecteer **Q#-toepassing** en klik op **Volgende**.
3. Geef een naam en een locatie op voor uw toepassing en klik op **Maken**.


Controleer het project. Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.

De toepassing uitvoeren:
1. Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**.
2. Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.

> [!NOTE]
> Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.  


## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
