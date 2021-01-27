---
title: Ontwikkelen met Q#-toepassingen in een IDE
description: Meer informatie over hoe u een Q#-toepassing maakt die wordt uitgevoerd vanuit de opdrachtprompt.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3e4f1e97477ecb0547b1586b1c7603c8a9954584
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844323"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a>Ontwikkelen met Q#-toepassingen in een IDE

Q#-programma's kunnen zonder stuurprogramma zelfstandig worden uitgevoerd in een hosttaal als C#, F# of Python. U kunt Q#-toepassingen ontwikkelen in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces of in andere editors/IDE's en toepassingen uitvoeren vanuit de .NET-console. 

## <a name="prerequisites-for-all-environments"></a>Vereisten voor alle omgevingen

- [.NET Core SDK 3.1 of hoger](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installatie

Hoewel u Q#-toepassingen in een IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken als u uw Q#-toepassingen lokaal wilt ontwikkelen. Als u uw toepassingen in de cloud wilt ontwikkelen via de webbrowser, raden we Visual Studio Codespaces aan. Bij het ontwikkelen in deze omgevingen wordt gebruikgemaakt van de uitgebreide functies van de QDK-extensie, waaronder waarschuwingen, markeren van syntaxis, projectsjablonen, en meer. 

### <a name="to-configure-for-vs-code"></a>Ga als volgt te werk om voor VS Code te configureren:

1. Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).
2. Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

### <a name="to-configure-for-visual-studio"></a>Ga als volgt te werk om voor Visual Studio te configureren:

1. Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.
2. Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).

### <a name="to-configure-for-another-environment"></a>Ga als volgt te werk als u voor een andere omgeving wilt configureren: 

1. Voer het volgende in de opdrachtprompt in

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a>Ga als volgt te werk als u voor Visual Studio Codespaces wilt configureren:

1. Maak een [Azure-account](https://azure.microsoft.com/free/).
2. Maak een Codespaces-omgeving. Volg de [quickstart-gids](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser). We raden u aan om bij het maken van de Codespace `microsoft/Quantum` in te voeren in het veld Git-opslagplaats om QDK-specifieke instellingen te laden.
3. Nu kunt u uw nieuwe omgeving starten en beginnen met ontwikkelen in de browser via de [VS Codespaces cloud-IDE](https://online.visualstudio.com/environments). Het is ook mogelijk om uw lokale installatie van VS Code te gebruiken en Codespaces te gebruiken als een [externe omgeving](https://docs.microsoft.com/visualstudio/online/how-to/vscode).

## <a name="develop-with-no-locq"></a>Ontwikkelen met Q#

Volg de instructies op het tabblad dat hoort bij de ontwikkelomgeving.

### <a name="vs-code"></a>[VS-code](#tab/tabid-vscode)

Ga als volgt te werk om een nieuw project te maken:

1. Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.
2. Klik op **Zelfstandige consoletoepassing**.
3. Navigeer naar de locatie om het project op te slaan. Voer de projectnaam in en klik op **Project maken**.
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
