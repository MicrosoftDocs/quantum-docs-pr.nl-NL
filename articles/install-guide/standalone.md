---
title: 'Ontwikkelen met Q # opdracht regel toepassingen'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e829862521951c50cb42eebf261c803071a95275
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426424"
---
# <a name="develop-with-q-command-line-applications"></a>Ontwikkelen met Q # opdracht regel toepassingen

Q #-Program ma's kunnen zelfstandig worden uitgevoerd, zonder een stuur programma in een host-taal als C#, F # of python.

## <a name="pre-requisites"></a>Vereisten

- [.NET Core SDK 3,1 of hoger](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installatie

Hoewel u Q # opdracht regel toepassingen in een IDE kunt maken, raden we u aan om Visual Studio code (VS code) of Visual Studio IDE te gebruiken voor uw Q #-toepassingen. Het ontwikkelen van deze hulpprogram ma's biedt toegang tot uitgebreide functionaliteit.

VS-code configureren:

1. Down load en Installeer [VS code](https://code.visualstudio.com/download) (Windows, Linux en Mac).
2. Installeer de [micro soft-QDK voor VS code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Visual Studio configureren:

1. Down load en Installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 of hoger met de .net core-werk belasting voor meerdere platform ontwikkeling ingeschakeld.
2. Down load en installeer de [micro soft-QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).


## <a name="develop-with-q-using-vs-code"></a>Ontwikkelen met Q # met behulp van VS code

De Q # project-sjablonen installeren:

1. Open VS code.
2. Klik **View**op  ->  **opdracht palet**weer geven.
3. Selecteer **Q #: Project sjablonen installeren**.

Wanneer de **geïnstalleerde project sjablonen** worden weer gegeven, is de QDK klaar voor gebruik met uw eigen toepassingen en bibliotheken.

Een nieuw project maken:

1. Klik **View**op  ->  **opdracht palet** weer geven en selecteer **Q #: nieuw project maken**.
2. Klik op **zelfstandige console toepassing**.
3. Ga naar de locatie waar u het project wilt opslaan en klik op **project maken**.
4. Wanneer het project is gemaakt, klikt u op **Nieuw project openen...** in de rechter benedenhoek.
        
Inspecteer het project. U ziet een bron bestand met de naam `Program.qs` , een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.

De toepassing uitvoeren:
1. Klik op **Terminal**  ->  **New Terminal**.
2. Voer op de terminal prompt in `dotnet run` .
3. Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`


> [!NOTE]
> Werk ruimten met meerdere hoofd mappen worden momenteel niet ondersteund door de extensie VS code Q #. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

## <a name="develop-with-q-using-visual-studio"></a>Ontwikkelen met Q # met behulp van Visual Studio

Controleer uw Visual Studio-installatie door een Q #-toepassing te maken `Hello World` .

Een nieuwe Q #-toepassing maken:
1. Open Visual Studio en klik op **bestand**  ->  **Nieuw**  ->  **project**.
2. Typ `Q#` in het zoekvak de optie **Q # toepassing** en klik op **volgende**.
3. Voer een naam en locatie in voor uw toepassing en klik op **maken**.


Inspecteer het project. U ziet een bron bestand met de naam `Program.qs` , een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.

De toepassing uitvoeren:
1. Selecteer **fout opsporing**  ->  **starten zonder fout opsporing**.
2. Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.

> [!NOTE]
> Als u meerdere projecten binnen één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing of in een van de submappen.  


## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
