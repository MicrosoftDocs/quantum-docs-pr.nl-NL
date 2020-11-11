---
title: Opmerkingen bij de release van de Quantum Development Kit
description: Meer informatie over de meest recente updates voor de preview-versie van de Microsoft Quantum Development Kit.
author: bradben
ms.author: v-benbra
ms.date: 8/30/2020
ms.topic: article
uid: microsoft.quantum.relnotes
no-loc:
- Q#
- $$v
ms.openlocfilehash: d38482be17e67f180441440ee8ccc7f1f64ebc9d
ms.sourcegitcommit: fb75d8f30f1d91f644b2a594f46867eb5968cfda
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2020
ms.locfileid: "94448341"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a>Opmerkingen bij de release van de Microsoft Quantum Development Kit

Dit artikel bevat informatie over elke Quantum Development Kit-release.

Raadpleeg de [installatiehandleiding](xref:microsoft.quantum.install) voor instructies bij de installatie.

Raadpleeg de [updatehandleiding](xref:microsoft.quantum.update) voor instructies bij updates.

## <a name="version-01320111004"></a>Versie 0.13.20111004

*Release datum: 10 november 2020*

Met deze release worden IntelliSense-functies voor Q# bestanden in Visual Studio en Visual Studio code uitgeschakeld wanneer een project bestand niet aanwezig is. Hiermee wordt een probleem opgelost waarbij IntelliSense-functies niet meer werken nadat een nieuw Q# bestand is toegevoegd aan een project (Zie [qsharp-compiler # 720](https://github.com/microsoft/qsharp-compiler/issues/720)).

## <a name="version-01320102604"></a>Versie 0.13.20102604

*Release datum: oktober 27, 2020*

Deze release omvat het volgende:

- Bij resource raming worden nu naast het aantal Qubit tegelijkertijd de Maxi maal Behaal bare diepte-en breedte schattingen in rekening gebracht. Zie [hier](xref:microsoft.quantum.machines.resources-estimator#metrics-reported) voor meer informatie.

Bekijk de volledige lijst met gesloten pull voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+closed%3A2020-09-25..2020-10-22), [compileren](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+closed%3A2020-09-25..2020-10-22), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+closed%3A2020-09-25..2020-10-22), voor [beelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+closed%3A2020-09-25..2020-10-22), [ Q# I](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+closed%3A2020-09-25..2020-10-22) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+closed%3A2020-09-25..2020-10-22).

## <a name="version-01220100504"></a>Versie 0.12.20100504

*Release datum: 5 oktober, 2020*

Deze release corrigeert een fout die van invloed is op het laden van Q# notitie blokken (Zie [iqsharp # 331](https://github.com/microsoft/iqsharp/pull/331)).

## <a name="version-01220092803"></a>Versie 0.12.20092803

*Release datum: 29 september, 2020*

Deze release omvat het volgende:

- Aankondiging en ontwerp specificatie van [Quantum Intermediate vertegenwoordiging (QIR)](https://github.com/microsoft/qsharp-language/tree/main/Specifications/QIR#quantum-intermediate-representation-qir) die is bedoeld als een gemeen schappelijke indeling in verschillende front-en back-ends. Zie ook ons [blog bericht](https://devblogs.microsoft.com/qsharp/introducing-quantum-intermediate-representation-qir) op QIR.
- Lance ring van onze nieuwe [ Q# taal opslag plaats](https://github.com/microsoft/qsharp-language) met ook de volledige [ Q# documentatie](https://github.com/microsoft/qsharp-language/tree/main/Specifications/Language#q-language).
- Prestatie verbeteringen voor QuantumSimulator voor Program ma's met een groot aantal qubits: betere toepassing van Gate Fusion-beslissingen; verbeterd parallel Lise ring in Linux-systeem; Intelligent schema voor het uitvoeren van Gate is toegevoegd. oplossingen voor fouten.
- IntelliSense-functies worden nu ondersteund voor Q# bestanden in Visual Studio en Visual Studio code, zelfs zonder een project bestand.
- Diverse Q# verbeteringen in/python-interoperabiliteit en oplossingen voor problemen, inclusief betere ondersteuning voor numpy-gegevens typen.
- Verbeteringen in de naam ruimte micro soft. Quantum. arrays (Zie [micro soft/QuantumLibraries # 313](https://github.com/microsoft/QuantumLibraries/issues/313)).
- Er is een nieuw [herhalings-tot-resultaat-voor beeld](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/repeat-until-success) toegevoegd dat slechts twee qubits gebruikt.

Sinds de laatste release is de naam van de standaard vertakking in elk van de open source-opslag plaatsen gewijzigd in `main` .

Bekijk de volledige lijst met gesloten pull voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+closed%3A2020-08-24..2020-09-24), [compileren](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+closed%3A2020-08-24..2020-09-24), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+closed%3A2020-08-24..2020-09-24), voor [beelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+closed%3A2020-08-24..2020-09-24), [ Q# I](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+closed%3A2020-08-24..2020-09-24) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+closed%3A2020-08-24..2020-09-24).

## <a name="version-01220082513"></a>Versie 0.12.20082513

*Release datum: augustus 25e, 2020*

Deze release omvat het volgende:

- Nieuwe [micro soft. Quantum. wille keurige naam ruimte](xref:Microsoft.Quantum.Random), waardoor u een handigere manier hebt om wille keurige waarden uit Program ma's te laten zien Q# . ([QuantumLibraries # 311](https://github.com/microsoft/QuantumLibraries/pull/311), [qsharp-runtime # 328](https://github.com/microsoft/qsharp-runtime/pull/328))
- Verbeterde [micro soft. Quantum. Diagnostics-naam ruimte](xref:Microsoft.Quantum.Diagnostics) met een nieuwe [ `DumpOperation` bewerking](xref:Microsoft.Quantum.Diagnostics.DumpOperation)en nieuwe bewerkingen voor het beperken van Qubit-toewijzing en Oracle-aanroepen. ([QuantumLibraries # 302](https://github.com/microsoft/QuantumLibraries/pull/302))
- De nieuwe [ `%project` Magic-opdracht](xref:microsoft.quantum.iqsharp.magic-ref.project) in I Q# en [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) in python ter ondersteuning van verwijzingen naar Q# projecten buiten de huidige werkruimte map. Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor de huidige beperkingen van deze functie. 
- Ondersteuning voor het automatisch laden van `.csproj` bestanden voor de Q# /python-hosts, waardoor het mogelijk is dat externe project-of pakket verwijzingen worden geladen tijdens de initialisatie. Raadpleeg de hand leiding voor het gebruik [ Q# van python-en Jupyter-notebooks](xref:microsoft.quantum.guide.host-programs) voor meer informatie.
- Het voor beeld voor ErrorCorrection. Syndrome is toegevoegd.
- Instel bare-koppeling toegevoegd aan SimpleIsing.
- Bijgewerkt HiddenShift-voor beeld.
- Voor beeld voor het oplossen van Sudoku met het algoritme van Grover (externe bijdrage) is toegevoegd.
- Algemene oplossingen voor fouten.

Bekijk de volledige lijst met gesloten pull voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compileren](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), voor [beelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [ Q# I](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01220072031"></a>Versie 0.12.20072031

*Release datum: 21 juli 2020*

Deze release omvat het volgende:

- Open bare naam ruimten in Q# notitie blokken zijn nu beschikbaar wanneer alle toekomstige cellen worden uitgevoerd. Zo kunt u bijvoorbeeld een naam ruimte openen in een cel boven aan het notitie blok, in plaats van dat u relevante naam ruimten in elke code-cel hoeft te openen. Met een nieuwe `%lsopen` Magic-opdracht wordt de lijst met momenteel geopende naam ruimten weer gegeven.

Bekijk de volledige lijst met gesloten pull voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compileren](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), voor [beelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [ Q# I](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01220070124"></a>Versie 0.12.20070124

*Release datum: juli 2e, 2020*

Deze release omvat het volgende:

- Nieuw `qdk-chem` hulp programma voor het converteren van verouderde indelingen voor de serialisatie van problemen met de elektronische structuur (bijvoorbeeld: FCIDUMP) naar [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)
- Nieuwe functies en bewerkingen in de [`Microsoft.Quantum.Synthesis`](xref:Microsoft.Quantum.Synthesis) naam ruimte voor een samenhangende toepassing van klassieke Oracle met behulp van trans formatie-en ontledings synthese algoritmen.
- Ik Q# kan nu argumenten voor de `%simulate` , `%estimate` en andere Magic-opdrachten. Raadpleeg de [ `%simulate` Magic-opdracht verwijzing](xref:microsoft.quantum.iqsharp.magic-ref.simulate) voor meer informatie.
- Nieuwe fase weergave opties in I Q# . Raadpleeg de [ `%config` Magic-opdracht verwijzing](xref:microsoft.quantum.iqsharp.magic-ref.config) voor meer informatie.
- I Q# en het `qsharp` python-pakket worden nu via Conda packages ([qsharp](https://anaconda.org/quantum-engineering/qsharp) en [iqsharp](https://anaconda.org/quantum-engineering/iqsharp)) verschaft om de lokale installatie van Q# Jupyter-en python-functionaliteit naar een Conda omgeving te vereenvoudigen. Raadpleeg de [ Q# Jupyter-notebooks](xref:microsoft.quantum.install.jupyter) en [ Q# met python](xref:microsoft.quantum.install.python) -installatie handleidingen voor meer informatie.
- Wanneer u de simulator gebruikt, hoeft qubits niet langer in de ⟩-status voor | 0 te zijn bij de release, maar deze kan automatisch opnieuw worden ingesteld als deze onmiddellijk worden gemeten voordat de versie wordt vrijgegeven.
- Updates om het voor Q# gebruikers gemakkelijker te maken om bibliotheek pakketten te gebruiken met verschillende QDK-versies, zodat alleen grote & secundaire versie nummers overeenkomen in plaats van exact dezelfde versie
- Afgeschafte `Microsoft.Quantum.Primitive.*` naam ruimte verwijderd
- Verplaatste bewerkingen:
  - `Microsoft.Quantum.Intrinsic.Assert` is nu `Microsoft.Quantum.Diagnostics.AssertMeasurement`
  - `Microsoft.Quantum.Intrinsic.AssertProb` is nu `Microsoft.Quantum.Diagnostics.AssertMeasurementProbability`
- Opgeloste fouten 

Bekijk de volledige lijst met gesloten pull voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compileren](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), voor [beelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [ Q# I](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0112006403"></a>Versie 0.11.2006.403

*Releasedatum: 4 juni, 2020*

Deze release corrigeert een bug die invloed heeft op de compilatie van Q# projecten.

## <a name="version-0112006207"></a>Versie 0.11.2006.207

*Releasedatum: 3 juni 2020*

Deze release omvat het volgende:

- Q# notebooks en python-host-Program ma's mislukken niet meer wanneer een Q# ingangs punt aanwezig is
- Updates voor de [standaardbibliotheek](xref:microsoft.quantum.libraries.standard.intro) voor het gebruik van toegangsparameters
- Compiler kan nu een invoegtoepassing voor het herschrijven van stappen uitvoeren tussen de ingebouwde stappen voor herschrijven
- Er zijn verschillende afgeschafte functies en bewerkingen verwijderd volgens de planning die wordt beschreven in onze [API-principes](xref:microsoft.quantum.contributing.api-design). Q# Program ma's en bibliotheken die zonder waarschuwingen in versie 0.11.2004.2825 maken, blijven werken ongewijzigd.

Bekijk de volledige lijst met gesloten pull voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compileren](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), voor [beelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed), [ Q# I](https://github.com/microsoft/iqsharp/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

> [!NOTE]
> Deze versie bevat een bug die invloed heeft op de compilatie van Q# projecten. We raden u aan bij te werken naar een nieuwere versie.

## <a name="version-01120042825"></a>Versie 0.11.2004.2825

*Releasedatum: 30 april 2020*

Deze release omvat het volgende:

- Nieuwe ondersteuning voor Q# toepassingen waarvoor geen C#-of python-hostbestand meer nodig is. Zie hier voor meer informatie over het aan de slag Q# gaan met toepassingen. [here](xref:microsoft.quantum.install.standalone)
- De quickstart voor de kwantumgenerator voor willekeurige nummers is bijgewerkt. Er is nu geen C# of Python-hostbestand meer nodig. Bekijk de bijgewerkte [quickstart](xref:microsoft.quantum.quickstarts.qrng)
- Prestatie verbeteringen voor I Q# docker-installatie kopieën

> [!NOTE]
> Q# toepassingen die gebruikmaken van het nieuwe [`@EntryPoint()`](xref:Microsoft.Quantum.Core.EntryPoint) kenmerk kunnen momenteel niet worden aangeroepen vanuit Python-of .net-hostgroepen.
> Raadpleeg de gidsen voor [Python](xref:microsoft.quantum.install.python) en [.NET-interoperabiliteit](xref:microsoft.quantum.install.cs) voor meer informatie.

## <a name="version-01120033107"></a>Versie 0.11.2003.3107

*Releasedatum: 31 maart 2020*

Deze release bevat kleine foutoplossingen voor versie 0.11.2003.2506.

## <a name="version-01120032506"></a>Versie 0.11.2003.2506

*Releasedatum: 26 maart, 2020*

Deze release omvat het volgende:

- Nieuwe ondersteuning voor toegangs parameters in Q# , voor meer informatie, Zie [Bestands structuren](xref:microsoft.quantum.guide.filestructure)
- Bijgewerkt naar .NET Core SDK 3.1

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020022610"></a>Versie 0.10.2002.2610

*Releasedatum: 27 februari 2020*

Deze release omvat het volgende:

- Nieuwe kwantumbibliotheek voor Machine Learning; bezoek voor meer informatie onze pagina met [QML-documentatie](xref:microsoft.quantum.machine-learning.concepts.intro)
- Ik Q# Fout oplossingen, wat leidt tot een toename van 10 20x bij het laden van NuGet-pakketten

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020012831"></a>Versie 0.10.2001.2831

*Releasedatum: 29 januari 2020*

Deze release omvat het volgende:

- Nieuw NuGet-pakket Microsoft.Quantum.SDK, dat het NuGet-pakket Microsoft.Quantum.Development.Kit vervangt bij het maken van nieuwe projecten. Het NuGet-pakket Microsoft.Quantum.Development.Kit wordt nog steeds ondersteund voor bestaande projecten. 
- Ondersteuning voor Q# compiler uitbreidingen, ingeschakeld door de nieuwe micro soft. Quantum. SDK NuGet uitgebracht, voor meer informatie raadpleegt u de [documentatie over github](https://github.com/microsoft/qsharp-compiler/tree/main/src/QuantumSdk#extending-the-q-compiler), het voor beeld van de [compiler extensies](https://github.com/microsoft/qsharp-compiler/tree/main/examples/CompilerExtensions) en het [ Q# dev-blog](https://devblogs.microsoft.com/qsharp/extending-the-q-compiler/)
- Ondersteuning toegevoegd voor .NET Core 3.1. Het wordt zeer aanbevolen om versie 3.1.100 geïnstalleerd te hebben, omdat bouwen met oudere .NET Core SDK-versies mogelijk problemen veroorzaakt
- Nieuwe compilatietransformaties beschikbaar onder Microsoft.Quantum.QsCompiler.Experimental
- Nieuwe functionaliteit voor het beschikbaar maken van uitvoer status vectoren als HTML in IQ#
- Ondersteuning toegevoegd voor EstimateFrequencyA in Microsoft.Quantum.Characterization voor Hadamard- en SWAP-tests
- AmplitudeAmplification-naam ruimte maakt nu gebruik van Q# stijl gids

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019120501"></a>Versie 0.10.1912.0501

*Releasedatum: 5 december 2019*

Deze release omvat het volgende:

- Nieuw test kenmerk voor Q# eenheids tests, zie bijgewerkte API-documentatie [hier](xref:Microsoft.Quantum.Diagnostics.Test) en de bijgewerkte hand [here](xref:microsoft.quantum.guide.testingdebugging) leiding voor het testen & de fout opsporing
- Stack tracering toegevoegd bij een fout van een Q# programma-uitvoering
- Ondersteuning voor onderbrekingspunten in Visual Studio Code door een update in de [OmniSharp C# Visual Studio Code-extensie](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019111607"></a>Versie 0.10.1911.1607

*Releasedatum: 17 november 2019*

Deze release omvat het volgende:

- Prestatieverbetering voor [Quantum Katas-](https://github.com/Microsoft/QuantumKatas) en Jupyter-notebooks

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  


## <a name="version-0101911307"></a>Versie 0.10.1911.307

*Releasedatum: 1 november 2019*

Deze release omvat het volgende:

- Updates voor Visual Studio code & Visual Studio-extensies voor het implementeren van taal server als een zelfstandig uitvoerbaar bestand, waardoor de afhankelijkheid van de .NET Core SDK-versie wordt geëlimineerd  
- Migratie naar .NET Core 3.0
- Wijziging aan Microsoft.Quantum.Simulation.Core.IOperationFactory die fouten veroorzaakt met de introductie van een nieuwe `Fail`-methode. Dit heeft alleen betrekking op aangepaste simulatoren die SimulatorBase niet uitbreiden. [Bekijk de pull-aanvraag op GitHub](https://github.com/microsoft/qsharp-runtime/pull/59) voor meer informatie.
- Nieuwe ondersteuning voor afgeschafte kenmerken

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0919093002"></a>Versie 0.9.1909.3002

*Releasedatum: 30 september 2019*

Deze release omvat het volgende:

- Nieuwe ondersteuning voor het Q# volt ooien van code in Visual Studio 2019 (versie 16,3 & hoger) & Visual Studio code
- Nieuwe [Quantum Kata](https://github.com/Microsoft/QuantumKatas) voor kwantumtoevoegingen

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-09-packagereference-0919082902"></a>Versie 0.9 ( *PackageReference 0.9.1908.2902* )

*Releasedatum: 29 augustus 2019*

Deze release omvat het volgende:

- Nieuwe ondersteuning voor [conjugation-instructies](xref:microsoft.quantum.guide.operationsfunctions#conjugations) in Q#
- Nieuwe codeacties in de compiler, zoals 'vervangen door', 'documentatie toevoegen' en eenvoudige updates van matrix-items
- Installatiesjabloon en nieuwe projectopdrachten toegevoegd aan Visual Studio Code-extensie
- Nieuwe varianten van ApplyIf-combinatie toegevoegd, zoals [Microsoft.Quantum.Canon.ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- Aanvullende [Quantum Katas](https://github.com/Microsoft/QuantumKatas) geconverteerd in Jupyter Notebooks
- Visual Studio-extensie vereist nu Visual Studio 2019

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

De wijzigingen zijn hier samengevat, evenals de instructies om uw huidige programma's bij te werken.  Meer informatie over deze wijzigingen vindt u in het [ Q# dev-blog](https://devblogs.microsoft.com/qsharp).

## <a name="version-08-packagereference-0819071701"></a>Versie 0.8 ( *PackageReference 0.8.1907.1701* )

*Releasedatum: 12 juli 2019*

Deze release omvat het volgende:

- Nieuwe indexeerlocaties voor slicermatrices. [Raadpleeg de taalreferentie](xref:microsoft.quantum.guide.expressions#array-slices) voor meer informatie.
- Dockerfile toegevoegd die worden gehost op de [micro soft-container Registry](https://github.com/microsoft/ContainerRegistry), zie de [ Q# opslag plaats voor meer informatie](https://github.com/microsoft/iqsharp/blob/main/README.md)
- Belangrijke wijziging voor de [traceersimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): configuratie-instellingen bijgewerkt, naam veranderd. Raadpleeg de [.NET API-browser voor de bijgewerkte namen](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration).

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) en [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-07-packagereference-0719053109"></a>Versie 0.7 ( *PackageReference 0.7.1905.3109* )

*Releasedatum: 31 mei 2019*

Deze release omvat het volgende:
- toevoegingen aan de Q# taal, 
- updates in de chemiebibliotheek, 
- een nieuwe numerieke bibliotheek.

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) en [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

De wijzigingen zijn hier samengevat, evenals de instructies om uw huidige programma's bij te werken.  Meer informatie over deze wijzigingen vindt u in het [ Q# dev-blog](https://devblogs.microsoft.com/qsharp).

### <a name="no-locq-language-syntax"></a>Q# taal syntaxis
Deze release voegt een nieuwe Q# taal syntaxis toe:
* Benoemde items toegevoegd voor [door de gebruiker gedefinieerde typen](xref:microsoft.quantum.guide.types#user-defined-types).  
* Door de gebruiker gedefinieerde typeconstructies kunnen nu als functies worden gebruikt.
* Ondersteuning toegevoegd voor [copy-and-update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) en [apply-and-reassign](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols) in door gebruiker gedefinieerde typen.
* Correctieblok voor [repeat-until-succes](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop)-lussen is nu optioneel.
* We ondersteunen nu een lus in functies (niet in bewerkingen).

### <a name="library"></a>Bibliotheek 

In deze release is een numerieke bibliotheek toegevoegd: Meer informatie over hoe u [de nieuwe numerieke bibliotheek gebruikt](xref:microsoft.quantum.numerics.usage) en de [nieuwe voorbeelden probeert](https://github.com/microsoft/quantum/tree/main/Numerics).  [PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).  

In deze release is de chemiebibliotheek opnieuw geordend en uitgebreid:
* De modulariteit van onderdelen is verbeterd en uitgebreid en de algemene code is opgeschoond.  [PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).
* Ondersteuning toegevoegd voor [wavefuncties met meerdere verwijzingen](xref:microsoft.quantum.chemistry.concepts.multireference), zowel verspreide wavefuncties met meerdere verwijzingen als unitaire gekoppelde clusters.  [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).
* (Bedankt!) [1QBit](https://1qbit.com)-inzender ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Energie-evaluatie met behulp van variatie-ansatz. [PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).
* [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)-schema bijgewerkt naar de nieuwe [versie 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2), waarbij unitaire gekoppelde clusters zijn toegevoegd. [Probleem #65](https://github.com/microsoft/QuantumLibraries/issues/65).
* Interoperabiliteit van Python toegevoegd aan functies van chemiebibliotheek. Probeer dit [voorbeeld](https://github.com/microsoft/Quantum/tree/main/Chemistry/PythonIntegration). [Probleem #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).

## <a name="version-061905"></a>Versie 0.6.1905

*Releasedatum: 3 mei 2019*

Deze release omvat het volgende:
- wijzigingen aanbrengen in de Q# taal, 
- nieuwe ordening van de Quantum Development Kit-bibliotheken, 
- nieuwe voorbeelden toegevoegd en 
- opgeloste fouten.  Verschillende gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) en [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

De wijzigingen zijn hier samengevat, evenals de instructies om uw huidige programma's bij te werken.  Lees meer over deze wijzigingen op devblogs.microsoft.com/qsharp.

### <a name="no-locq-language-syntax"></a>Q# taal syntaxis
Deze release voegt een nieuwe Q# taal syntaxis toe:
* Een [stenomanier toegevoegd om specialisaties van kwantumbewerkingen uit te drukken](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations) (controles en aangrenzenden) met `+`-operators.  De oude syntaxis is afgeschaft.  Programma's die gebruikmaken van de oude syntaxis (bijvoorbeeld `: adjoint`) werken nog steeds, maar er wordt een waarschuwing voor een compilatietijd gegenereerd.  
* Nieuwe operator toegevoegd voor [copy-and-update](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions), `w/`, kan ook worden gebruikt om het maken van een matrix uit te drukken als een wijziging van een bestaande matrix.
* Voeg de algemene instructie [apply-and-update](xref:microsoft.quantum.guide.variables#rebinding-of-mutable-symbols) toe, bijvoorbeeld `+=`, `w/=`.
* Een manier toegevoegd om een korte naam op te geven voor naamruimten in [open instructies](xref:microsoft.quantum.guide.filestructure#open-directives).

In deze release staan we niet meer toe dat een matrix-element wordt opgegeven aan de linkerkant van een ingestelde instructie.  Dat komt omdat de syntaxis impliceert dat matrices veranderlijk zijn, terwijl het resultaat van de bewerking altijd het maken van een nieuwe matrix met de bewerking is geweest.  In plaats daarvan wordt een compileerfout gegenereerd met een suggestie om de nieuwe operator copy-and-update, `w/`, te gebruiken om hetzelfde resultaat te bereiken.  

### <a name="library-restructuring"></a>Herstructurering van bibliotheek
In deze release zijn de bibliotheken opnieuw ingericht om te zorgen dat hun groei op een consistente manier plaatsvindt:
* De naamruimte Microsoft.Quantum.Primitive is hernoemd naar Microsoft.Quantum.Intrinsic.  Deze bewerkingen worden geïmplementeerd door de doelmachine.  De naamruimte Microsoft.Quantum.Primitive is afgeschaft.  Een runtime-waarschuwing wordt weergegeven wanneer aanroepbewerkingen en functies voor programma's afgeschafte namen gebruiken.

* Het pakket Microsoft.Quantum.Canon is hernoemd naar Microsoft.Quantum.Standard.  Dit pakket bevat naam ruimten die gemeen schappelijk zijn voor de meeste Q# Program ma's.  Dit omvat:  
    - Microsoft.Quantum.Canon voor algemene bewerkingen
    - Microsoft.Quantum.Arithmetic voor aritmetische bewerkingen met algemene doeleinden
    - Microsoft.Quantum.Preparation voor bewerkingen die worden gebruikt om de qubit-status voor te bereiden
    - Microsoft.Quantum.Simulation voor simulatiefunctionaliteit

Met deze wijziging treden er mogelijk opbouwfouten op in programma's met een enkele 'open' instructie voor de naamruimte Microsoft.Quatum.Canon als het programma verwijst naar bewerkingen die zijn verplaatst naar de andere drie nieuwe naamruimten.  Het toevoegen van aanvullende open instructies voor de drie nieuwe naamruimte is een logische manier om dit probleem op te lossen.  

* Verschillende naamruimten zijn aangeschaft, omdat de bewerkingen daarin zijn ingedeeld in andere naamruimten. Programma's die gebruikmaken van deze naamruimten blijven werken en een waarschuwing voor de compilatietijd geeft de naamruimte aan waar de bewerking is gedefinieerd.  

* De naamruimte Microsoft.Quantum.Arithmetic is genormaliseerd om gebruik te maken van het door de gebruiker gedefinieerde type <xref:Microsoft.Quantum.Arithmetic.LittleEndian>. Gebruik de functie [BigEndianAsLittleEndian](xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian) wanneer u die nodig hebt om een little endian te converteren.  

* De namen van verschillende callables (functies en bewerkingen) zijn gewijzigd in overeenstemming met de [ Q# stijl gids](xref:microsoft.quantum.contributing.style).  De oude namen van callables zijn afgeschaft.  Programma's die gebruikmaken van de oude callables blijven werken met een waarschuwing voor compilatietijd. 

### <a name="new-samples"></a>Nieuwe voorbeelden

We hebben een voor beeld toegevoegd van het gebruik van een [ Q# F #-stuur programma](https://github.com/Microsoft/Quantum/pull/164).  

**Bedankt!** aan de volgende inzender van onze open-codebasis op http://github.com/Microsoft/Quantum. Deze bijdragen nemen aanzienlijk toe aan de uitgebreide voor beelden van Q# code:

* Mathias Soeken ([@msoeken](https://github.com/msoeken)): Synthese van Oracle-functie. [PR #135](https://github.com/Microsoft/Quantum/pull/135).

### <a name="migrating-existing-projects-to-061905"></a>Bestaande projecten migreren naar 0.6.1905.

Raadpleeg de [installatiegids](xref:microsoft.quantum.install) om de QDK bij te werken.
  
Als u bestaande Q# projecten van versie 0,5 van de Quantum Development Kit hebt, zijn de volgende stappen voor het migreren van die projecten naar de nieuwste versie.

1. Projecten moeten in volgorde worden bijgewerkt.  Als u een oplossing hebt met meerdere projecten, werkt u elk project bij in de volgorde waarop ernaar wordt verwezen.
2. Voer vanaf een opdracht prompt uit `dotnet clean` om alle bestaande binaire bestanden en tussenliggende bestand te verwijderen.
3. Bewerk het .csproj-bestand in een teksteditor om de versie van alle 'Microsoft.Quantum' `PackageReference` te veranderen in versie 0.6.1904 en de naam van het pakket 'Microsoft.Quantum.Canon' te veranderen in 'Microsoft.Quantum.Standard', bijvoorbeeld:

    ```xml
    <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
    <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
    ```
4. Voer de volgende opdracht uit vanaf de opdracht prompt: `dotnet msbuild`  
5. Nadat u de opdracht hebt uitgevoerd, moet u mogelijk nog steeds handmatig fouten aanpakken door de bovenstaande wijzigingen.  In veel gevallen worden deze fouten ook gerapporteerd door IntelliSense in Visual Studio of Visual Studio Code.
    - Open de hoofdmap van het project of de oplossing in Visual Studio 2019 of Visual Studio Code.
    - Nadat u een. QS-bestand in de editor hebt geopend, ziet u de uitvoer van de Q# taal extensie in het uitvoer venster.
    - Nadat het project succesvol is geladen (aangegeven in het uitvoervenster), opent u elk bestand handmatig om de resterende problemen aan te pakken.

> [!NOTE]
> * Voor release 0.6 ondersteunt de taalserver in de Quantum Development Kit niet meerdere werkruimten.
> * Als u met een project in Visual Studio Code wilt werken, opent u de hoofdmap met het project zelf en alle projecten waarnaar wordt verwezen.   
> * Als u wilt werken met een oplossing in Visual Studio, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing of in een van de submappen.  
> * Verwijzingen tussen projecten die naar 0.6 en hoger zijn gemigreerd en projecten die oudere pakketversies gebruiken, worden **niet** ondersteund.

## <a name="version-051904"></a>Versie 0.5.1904

*Releasedatum: 15 april 2019*

De release omvat oplossingen van fouten.


## <a name="version-051903"></a>Versie 0.5.1903

*Releasedatum: 27 maart 2019*

Deze release omvat het volgende:

- Voegt ondersteuning toe voor Jupyter Notebook. Dit biedt een uitstekende manier om meer te weten te komen over Q# .  [Bekijk nieuwe Jupyter Notebook-voorbeelden en leer hoe u uw eigen Notebooks schrijft](xref:microsoft.quantum.install). 

- Aritmetische toevoeging van hele getallen toegevoegd aan de Quantum Canon-bibliotheek.  Raadpleeg ook een Jupyter Notebook die [beschrijft hoe u de nieuwe toevoegingen van hele getallen gebruikt](https://github.com/microsoft/Quantum/blob/main/samples/arithmetic/AdderExample.ipynb).

- Foutoplossing voor DumpRegister-probleem die door de community is gerapporteerd ([#148](https://github.com/Microsoft/Quantum/issues/148)).

- Mogelijkheid toegevoegd om terug te keren vanuit een [gebruiksinstructie](xref:microsoft.quantum.guide.qubits#allocating-qubits).

- [Introductiehandleiding](xref:microsoft.quantum.install) herschreven.


## <a name="version-051902"></a>Versie 0.5.1902

*Releasedatum: 27 februari 2019*

Deze release omvat het volgende:

- Ondersteuning toegevoegd voor platformoverschrijdende Python-host.  Met het `qsharp` pakket voor python kunt u eenvoudig Q# bewerkingen en functies in python simuleren. Meer informatie over [interoperabiliteit van Python](xref:microsoft.quantum.install). 

- De Visual Studio- en Visual Studio Code-extensies ondersteunen nu het hernoemen van symbolen (bijvoorbeeld functies en bewerkingen).

- De Visual Studio-extensie kan nu worden geïnstalleerd in Visual Studio 2019.

## <a name="version-041901"></a>Versie 0.4.1901

*Releasedatum: 30 januari 2019*

Deze release omvat het volgende:

- ondersteuning toegevoegd voor een nieuw primitief type, BigInt, dat een geheel getal met teken van arbitraire grootte vertegenwoordigt.  Meer informatie over het [BigInt-type](xref:microsoft.quantum.guide.types).
- nieuwe Toffoli-simulator toegevoegd, een snelle simulator voor speciale doeleinden die X-, CNOT- en meerdere gecontroleerde X-kwantumbewerkingen kan simuleren met grote aantallen qubits.  Meer informatie over de [Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator).
- voegt een eenvoudige resource-Estimator toe die een schatting maakt van de resources die nodig zijn om een bepaalde instantie van een Q# bewerking op een quantum computer uit te voeren.  Meer informatie over [Resource-inschatting](xref:microsoft.quantum.machines.resources-estimator).


## <a name="version-0318112802"></a>Versie 0.3.1811.2802

*Releasedatum: 28 november 2018*

Hoewel onze VS Code-extensie er geen gebruik van maakte, is een waarschuwing opgetreden en is het verwijderd uit de marketplace tijdens [de extensieverwijdering](https://code.visualstudio.com/blogs/2018/11/26/event-stream) met betrekking tot het NPM-pakket `event-stream`. In deze versie zijn alle runtime-afhankelijkheden verwijderd die een waarschuwing konden activeren in de extensie.

Als u de extensie eerder hebt geïnstalleerd, moet u deze opnieuw installeren. Ga naar de extensie [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) in de Visual Studio-marketplace en klik op Installeren. Onze excuses voor het ongemak.


## <a name="version-0318111511"></a>Versie 0.3.1811.1511

*Releasedatum: 20 november 2018*

In deze release wordt een fout opgelost waardoor sommige gebruikers de Visual Studio-extensie niet konden laden.

## <a name="version-031811203"></a>Versie 0.3.1811.203

*Releasedatum: 2 november 2018*

Deze release bevat enkele foutoplossingen, waaronder voor de volgende:

* `DumpMachine` aanroepen kon ervoor zorgen dat de status van de simulator onder bepaalde omstandigheden veranderde.
* Compilatiewaarschuwingen verwijderd bij het bouwen van projecten met een versie van .NET Core voor 2.1.403.
* Documentatie opgeschoond, in het bijzonder de tooltips die worden weergegeven wanneer in VS Code of Visual Studio de muisaanwijzer op een item wordt geplaatst.

## <a name="version-0318102508"></a>Versie 0.3.1810.2508

*Releasedatum: 29 oktober 2018*

Deze release bevat nieuwe taalfuncties en een verbeterde ontwikkelaarservaring:

* Deze release bevat een taal server voor Q# , evenals de client integraties voor Visual Studio en Visual Studio code. Hierdoor zijn meer IntelliSense-functies mogelijk, evenals live feedback bij typen, in de vorm van krabbeltjes onder fouten en waarschuwingen. 
* Met deze update worden diagnostische berichten in het algemeen aanzienlijk verbeterd, met eenvoudige navigatie naar en precieze bereiken voor diagnostische gegevens en aanvullende informatie in de weergegeven, zwevende informatie.
* De Q# taal is uitgebreid op manieren die de manieren bundelen waarop ontwikkel aars veelvoorkomende bewerkingen kunnen uitvoeren en nieuwe verbeteringen in de taal functies voor een krachtige snelle Quantum berekening.  Er zijn een aantal belang rijke wijzigingen in de Q# taal met deze release.   

Deze release bevat ook een nieuwe kwantumchemiebibliotheek:

* De chemiebibliotheek bevat nieuwe hamiltoniaanse simulatiefuncties, waaronder:
    - Trotter–Suzuki-integraties van willekeurige gelijke volgorde voor verbeterde simulatienauwkeurigheid.
    - Qubitization-simulatietechniek met specifieke chemieoptimalisaties om $T$-poortcomplexiteit te verminderen.
* Een nieuw open-sourceschema, het Broombridge-schema (verwijzend naar de [bezienswaardigheid](https://en.wikipedia.org/wiki/Broom_Bridge) die wordt gezien als de geboorteplaats van hamiltonianen), is geïntroduceerd om vertegenwoordigingen van moleculen te importeren en die te simuleren.
* Meerdere chemievertegenwoordigingen die zijn gedefinieerd met het Broombridge-schema worden opgegeven.  Deze modellen zijn gegenereerd door [NWChem](http://www.nwchem-sw.org/), een open-sourcehulpprogramma met hoge prestaties voor computationele chemie.
* Zelfstudies en voorbeelden beschrijven hoe u de chemiebibliotheek en de Broombridge-gegevensmodellen gebruikt voor het volgende:
    - Eenvoudige hamiltionianen maken met de chemiebibliotheek
    - Aangeslagen en grondtoestand van energie van Lithium Hydride visualiseren met fase-inschattingen.
    - Resource-inschattingen uitvoeren van kwantumchemiesimulatie.
    - Energieniveaus inschatten van moleculen van het Broombridge-schema.
* In de documentatie wordt beschreven hoe u NWChem kunt gebruiken om extra chemische modellen te genereren voor Quantum simulatie met Q# .

Meer informatie over de [Quantum Development Kit-chemiebibliotheek](xref:microsoft.quantum.chemistry.concepts.intro).

Met de nieuwe chemiebibliotheek plaatsen we de bibliotheken in een nieuwe GitHub-opslagplaats, [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).  De voorbeelden bevinden zich in de opslagplaats [Microsoft/Quantum](https://github.com/Microsoft/Quantum).  Bijdragen aan beide zijn welkom.

Deze release omvat foutoplossingen en functies voor problemen die door de community zijn gemeld:

* IntelliSense voor Q# ? ([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918)).
* .qs-bestanden ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049)).
* Foutbericht verbeterd wanneer accolades worden afgekort in de if-instructie ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518)).
* Ondersteuning voor tuple-ontsleuteling bij onveranderlijke (her)binding ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444)).
* Fout bij de uitvoering van opgegeven BitFlipCode ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).
* H2SimulationGUI geeft soms grote pieken weer ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).

### <a name="community-contributions"></a>Bijdragen van de community

**Bedankt!** aan de volgende inzenders van onze open-codebasis op http://github.com/Microsoft/Quantum. Deze bijdragen nemen aanzienlijk toe aan de uitgebreide voor beelden van Q# code:

* Rolf Huisman ( [@RolfHuisman](https://github.com/RolfHuisman) ): de ervaring voor QASM/ Q# ontwikkel aars is verbeterd door een QASM te maken voor Q# conversie. [PR #58](https://github.com/Microsoft/Quantum/pull/58).

* Andrew Helwer ([@ahelwer](https://github.com/ahelwer)):  Heeft een voorbeeld bijgedragen van de implementatie van de CHSH Game, een kwantumgame met betrekking tot niet-lokaliteit.  [PR #84](https://github.com/Microsoft/Quantum/pull/84).

We bedanken ook Rohit Gupta ([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi ([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)) en Lee James O'Riordan ([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) voor hun werk aan de verbetering van de inhoud door documentatie en spel- en typfouten! 

## <a name="version-021809701"></a>Versie 0.2.1809.701

*Releasedatum: 10 september 2018*

Deze release omvat foutoplossingen voor problemen die door de community zijn gemeld. Waaronder:

* Kan de shift-operator niet gebruiken ([GitHub](https://github.com/Microsoft/Quantum/issues/75)).
* `DumpMachine` / `DumpRegister` mislukt in `QCTraceSimulator` wanneer wordt geprint naar de console ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680)).
* Toewijzen van 0 qubits toegestaan ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits)).
* `AssertQubitState` vereist expliciete aanroep Complex() ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call)).
* De bewerking `Measure` retourneert altijd `One` in macOS ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).

Bedankt! 

## <a name="version-0218063001"></a>Versie 0.2.1806.3001

*Releasedatum: 30 juni 2018*

Deze releases zijn slechts een snelle oplossing voor het [probleem #48 gerapporteerd op github](https://github.com/Microsoft/Quantum/issues/48) ( Q# compilatie mislukt als de gebruikers naam een lege ruimte bevat). Volg dezelfde update-instructies als `0.2.1806.1503` met de bijbehorende nieuwe versie (`0.2.1806.3001-preview`).

## <a name="version-0218061503"></a>Versie 0.2.1806.1503

*Releasedatum: 22 juni 2018*

Deze release omvat verschillende bijdragen van de community, evenals een verbeterde ervaring voor foutopsporing en verbeterde prestaties.  Met name:

* Prestatieverbeteringen in zowel kleine als grote simulaties voor de QuantumSimulator-doelmachine.
* Verbeterde functionaliteit voor foutopsporing.
* Bijdragen van de community voor probleemoplossingen, nieuwe helper-functies, bewerkingen en nieuwe voorbeelden.

### <a name="performance-improvements"></a>Prestatieverbeteringen

Deze update omvat belangrijke prestatieverbeteringen voor simulaties van grote en kleine aantallen qubits voor alle doelmachines.  Deze verbetering is eenvoudig zichtbaar met de H<sub>2</sub>-simulatie, een standaardvoorbeeld in de Quantum Development Kit.

### <a name="improved-debugging-functionality"></a>Verbeterde functionaliteit voor foutopsporing

Deze update voegt nieuw functionaliteit voor foutopsporing toe:
* Twee nieuwe bewerkingen toegevoegd, @"microsoft.quantum.extensions.diagnostics.dumpmachine" en @"microsoft.quantum.extensions.diagnostics.dumpregister", die op een bepaald moment wave-informatie uitvoeren over de doelkwantummachine.  
* In Visual Studio wordt de kans op het meten van een $\ket{1}$ in een enkele qubit nu automatisch weergegeven in het foutopsporingsvenster voor de QuantumSimulator-doelmachine.
* In Visual Studio is de weergave verbeterd van variabele eigenschappen in de foutopsporingsvensters **Autos** en **Locals**. 

Meer informatie over [testen en foutopsporing](xref:microsoft.quantum.guide.testingdebugging).

### <a name="community-contributions"></a>Bijdragen van de community

De Q# Codeer community groeit en wij erg enthousiast de eerste gebruiker heeft bijgedragen aan de bibliotheken en voor beelden die zijn ingediend bij onze open code base op http://github.com/Microsoft/quantum .  **Hartelijk dank!** aan de volgende inzenders:
* Mathias Soeken ([@msoeken](https://github.com/msoeken)): heeft een voorbeeld bijgedragen dat een op transformatie gebaseerde logische synthesemethode definieert waarmee Toffoli-netwerken worden gemaakt om een bepaalde permutatie te implementeren. De code wordt volledig geschreven in Q# functies en bewerkingen.  [PR #41](https://github.com/Microsoft/Quantum/pull/41).
* RolfHuisman ( [@RolfHuisman](https://github.com/RolfHuisman) ): micro soft MVP Rolf Huisman heeft een steek proef bijgedragen waarmee platte QASM code wordt gegenereerd op basis van Q# code voor een beperkte groep Program ma's die geen klassieke controle stroom en beperkte Quantum bewerkingen hebben. [PR #59](https://github.com/Microsoft/Quantum/pull/59)
* Sarah Kasier ([@crazy4pi314](https://github.com/crazy4pi314)): heeft geholpen onze codebasis te verbeteren door een bibliotheekfunctie in te zenden voor gecontroleerde bewerkingen. [PR #53](https://github.com/Microsoft/Quantum/pull/53)
* Jessica Lemieux ([@Lemj3111](https://github.com/Lemj3111)): heeft @"microsoft.quantum.canon.quantumphaseestimation" opgelost een nieuwe moduletests gemaakt.  [PR #54](https://github.com/Microsoft/Quantum/pull/54)
* Tama McGlinn ([@TamaHobbit](https://github.com/TamaHobbit)): heeft het Teleportation-voorbeeld opgeschoond door ervoor te zorgen dat het QuantumSimulator-exemplaar wordt verwijderd. [PR #20](https://github.com/Microsoft/Quantum/pull/20)

Daarnaast nog **Hartelijk dank!** aan deze Microsoft Software-Engineers van het Commercial Engineering Services-team, die belangrijke wijzigingen hebben doorgevoerd in onze documentatie tijdens hun Hackathon.  Dankzij hun wijzigingen is de duidelijkheid van de onboarding-ervaring voor ons allemaal aanzienlijk verbeterd:
* Sascha Corti
* Mihaela Curmei
* John Donnelly
* Kirill Logachev
* Jan Pospisil
* Anita Ramanan
* Frances Tibble
* Alessandro Vozza

### <a name="update-existing-projects"></a>Bestaande projecten bijwerken

Deze versie is volledig compatibel met eerdere versies. U hoeft alleen de NuGet-pakketten in uw projecten bij te werken naar versie `0.2.1806.1503-preview` en een **volledige heropbouw** uit te voeren om ervoor te zorgen dat alle tussenliggende bestanden opnieuw worden gegenereerd.

Volg in Visual Studio de normale instructies over hoe u een [pakket bijwerkt](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package).

Als u projectsjablonen voor de opdrachtregel wilt bijwerken, voert u de volgende opdracht uit:
```
dotnet new -i "Microsoft.Quantum.ProjectTemplates::0.2.1806.1503-preview"
```

Nadat u deze opdracht hebt uitgevoerd, maken nieuwe project die zijn gemaakt met `dotnet new <project-type> -lang Q#`, automatisch gebruik van deze versie van de Quantum Development Kit.

Als u een bestaand project wilt bijwerken, zodat die gebruikmaakt van de nieuwste versie, voert u de volgende opdracht uit vanuit de map voor elk project:

```
dotnet add package Microsoft.Quantum.Development.Kit -v "0.2.1806.1503-preview"
dotnet add package Microsoft.Quantum.Canon -v "0.2.1806.1503-preview"
```

Als een bestaand project ook gebruikmaakt van XUnit-integratie voor moduletests, kan een soortgelijke opdracht worden gebruikt om ook dat pakket bij te werken:
```
dotnet add package Microsoft.Quantum.Xunit -v "0.2.1806.1503-preview"
```

Afhankelijk van de versie van XUnit die uw testproject gebruikt, moet u mogelijk ook XUnit bijwerken naar 2.3.1:
```
dotnet add package xunit -v "2.3.1" 
```

Na de update moet u ervoor zorgen dat u alle tijdelijke bestanden verwijdert die door vorige versie zijn gegenereerd. U doet dat zo:
```
dotnet clean 
```

### <a name="known-issues"></a>Bekende problemen

Er zijn verder geen bekende problemen te melden.


## <a name="version-0218022202"></a>Versie 0.2.1802.2202

*Releasedatum: 26 februari 2018*

Deze release biedt ondersteuning voor ontwikkeling in meerdere platforms, interoperabiliteit van talen en prestatieverbeteringen. Met name:

- Ondersteuning voor ontwikkeling in macOS en Linux. 
- .NET Core-compatibiliteit, inclusief ondersteuning voor Visual Studio Code op verschillende platforms.
- Een volledige Open Source-licentie voor de Quantum Development Kit-bibliotheken.
- Verbeterde simulatieprestaties in projecten die 20 of meer qubits nodig hebben.
- Interoperabiliteit met de Python-taal (preview-versie beschikbaar in Windows).

### <a name="net-editions"></a>.NET-edities

Het .NET-platform is beschikbaar via twee verschillende edities, het .NET Framework dat wordt geleverd met Windows en het open source .NET Core dat beschikbaar is in Windows, macOS en Linux.
In deze release worden de meeste delen van de Quantum Development Kit geleverd als bibliotheken voor .NET Standard, de set klassen die te vinden zijn in zowel Framework als Core.
Deze bibliotheken zijn daarom compatibel met recente versie van .NET Framework of .NET Core.

Om ervoor te zorgen dat projecten die worden geschreven met de Quantum Development Kit zo mobiel mogelijk zijn, raden we aan dat bibliotheekprojecten die zijn geschreven met de Quantum Development Kit .NET Standard als doel hebben, terwijl consoletoepassingen .NET Core als doel hebben.
Aangezien eerdere release van de Quantum Development Kit alleen .NET Framework ondersteunde, moet u uw bestaande projecten mogelijk migreren. Kijk hieronder voor informatie over hoe u dit doet.

### <a name="project-migration"></a>Projectmigratie

Projecten die zijn gemaakt met eerdere versies van de Quantum Development Kit blijven werken zolang u de NuGet-pakketten daarin niet bijwerkt. Als u bestaande code wilt migreren naar de nieuwe versie, voert u de volgende stappen uit:
1. Maak een nieuw .NET core-project met het juiste type Q# project sjabloon (toepassing, bibliotheek of test project).
2. Kopieer bestaande .qs- en .cs-/.fs-bestanden van het oude project naar het nieuwe project (met behulp van Toevoegen > Bestaand item). Kopieer het bestand AssemblyInfo.cs niet.
3. Bouw het nieuwe project en voer het uit.

Houd er rekening mee dat de bewerking RandomWalkPhaseEstimation van de raamruimte Microsoft.Quantum.Canon is verplaatst naar de naamruimte Microsoft.Research.Quantum.RandomWalkPhaseEstimation in de opslagplaats [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc).

### <a name="known-issues"></a>Bekende problemen

- De `--filter` optie `dotnet test` werkt niet correct voor testen die in zijn geschreven Q# .
  Als gevolg hiervan kunnen afzonderlijke eenheids tests niet worden uitgevoerd in Visual Studio code. u `dotnet test` kunt het beste bij de opdracht prompt gebruiken om alle tests opnieuw uit te voeren.

## <a name="version-0118011707"></a>Versie 0.1.1801.1707

*Releasedatum: 18 januari 2018*

In deze release is een aantal fouten opgelost die zijn gemeld door de community. In het bijzonder:

- De simulator werkt nu met eerdere CPU's zonder AVX-functionaliteit.
- De instellingen voor de regionale decimalen zorgen er niet toe dat de Q# parser mislukt.
- De primitieve bewerking `SignD` retourneert nu `Int` in plaats van `Double`.


## <a name="version-011712901"></a>Versie 0.1.1712.901

*Releasedatum: 11 december 2017*

### <a name="known-issues"></a>Bekende problemen

#### <a name="hardware-and-software-requirements"></a>Hardware-en software vereisten

- Om de simulator in de Quantum Development Kit uit te voeren, is een 64-bits installatie van Microsoft Windows vereist.
- De kwantumsimulator van Microsoft, geïnstalleerd met de Quantum Development Kit, maakt gebruik van Advanced Vector Extensions (AVX) en vereist een CPU met AVX-functionaliteit. Intel-processors die zijn verzonden in Q1 van 2011 (Sandy Bridge) of later ondersteunen AVX. We evalueren ondersteuning voor eerdere CPU's en kondigen mogelijk later details aan.

#### <a name="project-creation"></a>Een project maken

- Bij het maken van een oplossing (. SLN) die wordt gebruikt Q# , moet de oplossing één map zijn die hoger is dan elk project (. csproj) in de oplossing. Wanneer u een nieuwe oplossing maakt, doet u dit door ervoor te zorgen dat het selectievakje 'Map voor oplossing maken' in het dialoogvenster 'Nieuw project' is aangevinkt. Als dit niet is gebeurd, moeten de NuGet-pakketten van de Quantum Development Kit handmatig worden geïnstalleerd.

#### Q#

- In IntelliSense worden de juiste fouten voor code niet weer gegeven Q# . Zorg ervoor dat er in de Visual Studio-Foutenlijst opbouw fouten worden weer gegeven om de juiste fouten te bekijken Q# . Houd er ook rekening mee dat Q# fouten pas worden weer gegeven nadat u een build hebt gemaakt.
- Het gebruik van een onveranderlijke matrix in een gedeeltelijke toepassing leidt mogelijk tot onverwacht gedrag.
- Als u een veranderlijke matrix bindt aan een onveranderlijke (bijvoorbeeld a = b, waar b een onveranderlijke matrix is), leidt dat mogelijk tot onverwacht gedrag.
- Profileren, code dekking en andere VS-invoeg toepassingen zijn mogelijk niet altijd nauw keurig voor het tellen van Q# regels en blokken.
- De niet- Q# geïnterpoleerde teken reeksen worden niet gevalideerd door de compiler. Het is mogelijk om C#-compilatie fouten te maken door de naam van variabelen te controleren of door expressies te gebruiken in Q# geïnterpoleerde teken reeksen.

#### <a name="simulation"></a>Simulatie

- De QuantumSimulator maakt gebruik van OpenMP om de vereiste lineaire algebra te parallelliseren. OpenMP gebruikt standaard alle beschikbare hardware-threads, wat wil zeggen dat programma's met kleine aantallen qubits vaak langzaam worden uitgevoerd door de coördinatie die nodig is om het werkelijke werk te klein te laten lijken. Dit kan worden opgelost door de omgevingsvariable OMP_NUM_THREADS in te stellen op een kleiner getal. Als brede richtlijn is één thread goed voor ongeveer vier qubits en is vervolgens een aanvullende thread per qubit goed, hoewel dit zeer afhankelijk is van uw algoritme.

#### <a name="debugging"></a>Foutopsporing

- F11 (stap in) werkt niet in Q# code.
- Het markeren van code in Q# code bij een onderbrekings punt of onderbreking met één stap is soms onjuist. De juiste regel wordt gemarkeerd, maar soms begint en eindigt de markering bij onjuiste kolommen in de regel.

#### <a name="testing"></a>Testen

- Tests moeten worden uitgevoerd in de 64-bits modus. Als uw tests mislukken met BadImageFormatException, gaat u naar het menu Test en selecteert u Testinstellingen > Standaard processorarchitectuur > X64.
- Sommige tests duren lang (waarschijnlijk vijf minuten, afhankelijk van uw computer). Dat is normaal, aangezien sommige tests meer dan 20 qubits gebruiken. Onze grootste test wordt momenteel uitgevoerd op 23 qubits.

#### <a name="samples"></a>Voorbeelden

- In sommige machines is het mogelijk dat sommige kleine voorbeelden langzaam worden uitgevoerd, tenzij de omgevingsvariabele OMP_NUM_THREADS is ingesteld op '1'. Raadpleeg ook de releaseopmerking onder 'Simulatie'.

#### <a name="libraries"></a>Bibliotheken

- Er is een impliciete veronderstelling dat de qubits die worden doorgevoerd naar een bewerking in verschillende argumenten, allemaal verschillend zijn. Alle bibliotheekbewerkingen (en alle simulatoren) gaan er bijvoorbeeld vanuit dat de twee qubits die worden doorgevoerd naar een gecontroleerde NOT, verschillende qubits zijn. Als deze aanname wordt geschonden, leidt dat mogelijk tot onverwacht gedrag. Het is mogelijk om hierop te testen met de traceringssimulator voor kwantumcomputers.
- De functie Microsoft.Quantum.Bind gedraagt zich mogelijk niet alle gevallen zoals verwacht.
- In de naamruimte Microsoft.Quantum.Extensions.Math retourneert de functie SignD een Double in plaats van een Int, hoewel de onderliggende functie System.Math.Sign altijd een geheel getal retourneert. De resultaten kunnen worden vergeleken met 1.0, -1.0 en 0.0, aangezien al deze dubbelen exacte binaire vertegenwoordigingen hebben.
