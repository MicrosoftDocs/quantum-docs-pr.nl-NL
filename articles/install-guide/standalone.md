---
title: "Q #-Program ma's uitvoeren zonder stuur programma en host-taal"
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706798"
---
# <a name="q-command-line-applications"></a>Q # opdracht regel toepassingen

Q #-Program ma's kunnen zelfstandig worden uitgevoerd, zonder een stuur programma in een host-taal als C#, F # of python.

## <a name="pre-requisites"></a>Vereisten

- [.NET Core SDK 3,1 of hoger](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installatie

Hoewel u Q # opdracht regel toepassingen in een IDE kunt maken, raden we u aan om Visual Studio code (VS code) of Visual Studio IDE te gebruiken voor uw Q #-toepassingen. Door gebruik te maken van VS code of Visual Studio en de QDK Visual Studio code-extensie kunt u toegang krijgen tot uitgebreide functionaliteit.

- [VS-code](https://code.visualstudio.com/download) installeren (Windows, Linux en Mac)
- De [QDK-uitbrei ding voor VS code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) installeren of
- [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld
- Down load en installeer de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)


## <a name="develop-with-q-using-vs-code"></a>Ontwikkelen met Q # met behulp van VS code

Installeer de Quantum-projectsjablonen:

- Ga naar het**opdracht palet** **weer geven** -> 
- Selecteer **Q #: Project sjablonen installeren**

De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.
- Maak een nieuw project:
  - Ga naar het**opdracht palet** **weer geven** -> 
  - Selecteer **Q #: nieuw project maken**
  - **Zelfstandige console toepassing** selecteren
  - Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken
  - Klik op de knop **Nieuw project openen...** zodra het project is gemaakt
        
- Controleer het project
  - U ziet dat een bestand wordt gemaakt `Program.qs` met de naam Create, een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.

- Voer de toepassing uit:
  - Ga naar **Terminal** -> **New Terminal**
  - Voer `dotnet run` in
  - Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`


> [!NOTE]
> * Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

## <a name="develop-with-q-using-visual-studio"></a>Ontwikkelen met Q # met behulp van Visual Studio

Controleer de installatie door een `Hello World`-toepassing te maken

- Maak een nieuwe Q#-toepassing
  - Ga naar het **bestand** -> **Nieuw** -> **project**
  - Typ `Q#` in het zoekvak
  - Selecteer **Q#-toepassing**
  - Selecteer **volgende**
  - Kies een naam en een locatie voor uw toepassing
  - Selecteer **maken**

- Controleer het project
  - U ziet dat er een bestand met `Program.qs` de naam is gemaakt. Dit is een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.

- De toepassing uitvoeren
  - Selecteer **fouten opsporen** -> **starten zonder fout opsporing**
  - Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.

> [!NOTE]
> * Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.  


## <a name="whats-next"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.
