---
title: Ontwikkelen met Q#-toepassingen
description: Meer informatie over hoe u een Q#-toepassing maakt die wordt uitgevoerd vanuit de opdrachtprompt.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 68f530d80e5c5f40dc2bcbb185879c3cb6f93f91
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834411"
---
# <a name="develop-with-no-locq-applications"></a>Ontwikkelen met Q#-toepassingen

Volg de instructies op het tabblad dat hoort bij de omgeving.

Q#-programma's kunnen zonder stuurprogramma zelfstandig worden uitgevoerd in een hosttaal als C#, F# of Python.

## <a name="prerequisites"></a>Vereisten

- [.NET Core SDK 3.1 of hoger](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installatie

Hoewel u Q#-toepassingen in een IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken als u uw Q#-toepassingen lokaal wilt ontwikkelen. Als u uw toepassingen in de cloud wilt ontwikkelen via de webbrowser, raden we Visual Studio Codespaces aan. Ontwikkelen in deze omgevingen omvat de uitgebreide functies van de QDK-extensie, waaronder waarschuwingen, markeren van syntaxis, projectsjablonen, en meer. 

Ga als volgt te werk om VS Code te configureren:

1. Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).
2. Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Ga als volgt te werk om Visual Studio te configureren:

1. Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.
2. Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).

Voor de configuratie van Visual Studio Codespaces gaat u als volgt te werk:

1. Maak een [Azure-account](https://azure.microsoft.com/free/).
2. Maak een Codespaces-omgeving. Volg de [quickstart-gids](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser). We raden u aan om bij het maken van de Codespace `microsoft/Quantum` in te voeren in het veld Git-opslagplaats om QDK-specifieke instellingen te laden.
3. Nu kunt u uw nieuwe omgeving starten en beginnen met ontwikkelen in de browser via de [VS Codespaces cloud-IDE](https://online.visualstudio.com/environments). Het is ook mogelijk om uw lokale installatie van VS Code te gebruiken en Codespaces te gebruiken als een [externe omgeving](https://docs.microsoft.com/visualstudio/online/how-to/vscode).


Als u de QDK wilt installeren in een andere omgeving, voert u het volgende bij de opdrachtprompt in:

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a>Ontwikkelen met Q#

Volg de instructies op het tabblad dat hoort bij de omgeving.

### <a name="vs-code"></a>[VS-code](#tab/tabid-vscode)

Ga als volgt te werk om een nieuw project te maken:

1. Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.
2. Klik op **Zelfstandige consoletoepassing**.
3. Ga naar de locatie waar het project moet worden opgeslagen en klik op **Project maken**.
4. Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.

Controleer het project. Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.

De toepassing uitvoeren:

1. Klik op **Terminal** -> **Nieuwe terminal**.
2. Voer bij de terminalprompt `dotnet run` in.
3. Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`

> [!NOTE]
> Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de VS Code Q#-extensie. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs)

Controleer uw Visual Studio-installatie door een Q# `Hello World`-toepassing te maken.

Een nieuwe Q#-toepassing maken:

1. Open Visual Studio en klik op **Bestand** -> **Nieuw** -> **Project**.
2. Typ `Q#` in het zoekvak, selecteer **Q#-toepassing** en klik op **Volgende**.
3. Geef een naam en een locatie op voor uw toepassing en klik op **Maken**.


Controleer het project. Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.

De toepassing uitvoeren:

1. Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**.
2. Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.

> [!NOTE]
> Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.  

### <a name="other-editors-with-the-command-prompt"></a>[Andere editors met de opdrachtprompt](#tab/tabid-cmdline)

Controleer de installatie door een Q# `Hello World`-toepassing te maken.

1. Installeer de projectsjablonen.

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. Een nieuwe toepassing maken:

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. Navigeer naar de toepassingsmap:

    ```dotnetcli
    cd runSayHello
    ```

    De map bevat nu een bestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven. U kunt deze sjabloon wijzigen met een teksteditor en overschrijven met uw eigen kwantumtoepassingen. 

1. Voer het programma uit:

    ```dotnetcli
    dotnet run
    ```

1. U ziet nu de volgende tekst: `Hello quantum world!`

***

## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
