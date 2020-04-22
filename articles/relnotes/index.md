---
title: Opmerkingen bij de release van de Quantum Development Kit
description: Meer informatie over de meest recente updates voor de preview-versie van de Microsoft Quantum Development Kit.
author: natke
ms.author: nakersha
ms.date: 09/30/2019
ms.topic: article
uid: microsoft.quantum.relnotes
ms.openlocfilehash: 7a080f82e586f06d40e9d793ee05932db4c3ccef
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "81481419"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a>Opmerkingen bij de release van de Microsoft Quantum Development Kit

Dit artikel bevat informatie over elke Quantum Development Kit-release.

Raadpleeg de [installatiehandleiding](xref:microsoft.quantum.install) voor instructies bij de installatie.

Raadpleeg de [updatehandleiding](xref:microsoft.quantum.update) voor instructies bij updates.


## <a name="version-01120032506"></a>Versie 0.11.2003.2506

*Releasedatum: 26 maart, 2020*

Deze release omvat het volgende:

- Nieuwe ondersteuning om modifiers te openen in Q#. Raadpleeg [Bestandsstructuren](xref:microsoft.quantum.language.file-structure#internal-declarations) voor meer informatie.
- Bijgewerkt naar .NET Core SDK 3.1

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020022610"></a>Versie 0.10.2002.2610

*Releasedatum: 27 februari 2020*

Deze release omvat het volgende:

- Nieuwe kwantumbibliotheek voor Machine Learning; bezoek voor meer informatie onze pagina met [QML-documentatie](https://docs.microsoft.com/quantum/libraries/machine-learning/?view=qsharp-preview)
- Er zijn fouten opgelost in IQ#, wat resulteert in prestatieverbeteringen van 10-20x bij het laden van NuGet-pakketten

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020012831"></a>Versie 0.10.2001.2831

*Releasedatum: 29 januari 2020*

Deze release omvat het volgende:

- Nieuw NuGet-pakket Microsoft.Quantum.SDK, dat het NuGet-pakket Microsoft.Quantum.Development.Kit vervangt bij het maken van nieuwe projecten. Het NuGet-pakket Microsoft.Quantum.Development.Kit wordt nog steeds ondersteund voor bestaande projecten. 
- Ondersteuning voor Q#-compilerextensies, mogelijk gemaakt door het nieuwe NuGet-pakket Microsoft.Quantum.SDK; raadpleeg voor meer informatie de [documentatie op Github](https://github.com/microsoft/qsharp-compiler/tree/master/src/QuantumSdk#extending-the-q-compiler), het [voorbeeld van compilerextensies](https://github.com/microsoft/qsharp-compiler/tree/master/examples/CompilerExtensions) en het [Q#- dev-blog](https://devblogs.microsoft.com/qsharp/extending-the-q-compiler/)
- Ondersteuning toegevoegd voor .NET Core 3.1. Het wordt zeer aanbevolen om versie 3.1.100 geïnstalleerd te hebben, omdat bouwen met oudere .NET Core SDK-versies mogelijk problemen veroorzaakt
- Nieuwe compilatietransformaties beschikbaar onder Microsoft.Quantum.QsCompiler.Experimental
- Nieuwe functionaliteit om uitvoerstatusvectors beschikbaar te maken als HTML in IQ#
- Ondersteuning toegevoegd voor EstimateFrequencyA in Microsoft.Quantum.Characterization voor Hadamard- en SWAP-tests
- Naamruimte AmplitudeAmplification maakt nu gebruik van de Q#-stijlgids

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019120501"></a>Versie 0.10.1912.0501

*Releasedatum: 5 december 2019*

Deze release omvat het volgende:

- Nieuwe kenmerk Test voor Q#-eenheidstest. Raadpleeg [hier](https://docs.microsoft.com/qsharp/api/qsharp/microsoft.quantum.diagnostics.test) bijgewerkte API-documentatie en [hier](xref:microsoft.quantum.techniques.testing-and-debugging) bijgewerkte handleiding voor tests en foutopsporing
- Stack-trace toegevoegd in het geval van een fout in een Q#-programmabewerking
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

- Updates voor Visual Studio Code en Visual Studio-extensies die het mogelijk maken de taalserver als zelfstandig uitvoerbaar bestand te implementeren, waardoor de versieafhankelijkheid van de .NET Core SDK wordt geëlimineerd  
- Migratie naar .NET Core 3.0
- Wijziging aan Microsoft.Quantum.Simulation.Core.IOperationFactory die fouten veroorzaakt met de introductie van een nieuwe `Fail`-methode. Dit heeft alleen betrekking op aangepaste simulatoren die SimulatorBase niet uitbreiden. [Bekijk de pull-aanvraag op GitHub](https://github.com/microsoft/qsharp-runtime/pull/59) voor meer informatie.
- Nieuwe ondersteuning voor afgeschafte kenmerken

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0919093002"></a>Versie 0.9.1909.3002

*Releasedatum: 30 september 2019*

Deze release omvat het volgende:

- Nieuwe ondersteuning voor Q#-codeaanvulling in Visual Studio 2019 (versie 16.3 en later) en Visual Studio Code
- Nieuwe [Quantum Kata](https://github.com/Microsoft/QuantumKatas) voor kwantumtoevoegingen

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-09-packagereference-0919082902"></a>Versie 0.9 (*PackageReference 0.9.1908.2902*)

*Releasedatum: 29 augustus 2019*

Deze release omvat het volgende:

- Nieuwe ondersteuning voor [vervoegingsverklaringen](xref:microsoft.quantum.language.statements#conjugations) in Q#
- Nieuwe codeacties in de compiler, zoals 'vervangen door', 'documentatie toevoegen' en eenvoudige updates van matrix-items
- Installatiesjabloon en nieuwe projectopdrachten toegevoegd aan Visual Studio Code-extensie
- Nieuwe varianten van ApplyIf-combinatie toegevoegd, zoals [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone)
- Aanvullende [Quantum Katas](https://github.com/Microsoft/QuantumKatas) geconverteerd in Jupyter Notebooks
- Visual Studio-extensie vereist nu Visual Studio 2019

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) en [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

De wijzigingen zijn hier samengevat, evenals de instructies om uw huidige programma's bij te werken.  Bekijk meer informatie over deze wijzigingen in het [Q#-ontwikkelaarsblog](https://devblogs.microsoft.com/qsharp).

## <a name="version-08-packagereference-0819071701"></a>Versie 0.8 (*PackageReference 0.8.1907.1701*)

*Releasedatum: 12 juli 2019*

Deze release omvat het volgende:

- Nieuwe indexeerlocaties voor slicermatrices. [Raadpleeg de taalreferentie](xref:microsoft.quantum.language.expressions#array-slices) voor meer informatie.
- Dockerfile toegevoegd dat werd gehost in [Microsoft Container Registry](https://github.com/microsoft/ContainerRegistry). Raadpleeg de [IQ#-opslagplaats voor meer informatie](https://github.com/microsoft/iqsharp/blob/master/README.md)
- Belangrijke wijziging voor de [traceersimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): configuratie-instellingen bijgewerkt, naam veranderd. Raadpleeg de [.NET API-browser voor de bijgewerkte namen](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration).

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) en [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-07-packagereference-0719053109"></a>Versie 0.7 (*PackageReference 0.7.1905.3109*)

*Releasedatum: 31 mei 2019*

Deze release omvat het volgende:
- toevoegingen aan de Q#-taal, 
- updates in de chemiebibliotheek, 
- een nieuwe numerieke bibliotheek.

Bekijk de volledige lijst met gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) en [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

De wijzigingen zijn hier samengevat, evenals de instructies om uw huidige programma's bij te werken.  Bekijk meer informatie over deze wijzigingen in het [Q#-ontwikkelaarsblog](https://devblogs.microsoft.com/qsharp).

### <a name="q-language-syntax"></a>Q#-taalsyntaxis
In deze release is een nieuwe Q#-taalsyntaxis toegevoegd:
* Benoemde items toegevoegd voor [door de gebruiker gedefinieerde typen](xref:microsoft.quantum.language.type-model#user-defined-types).  
* Door de gebruiker gedefinieerde typeconstructies kunnen nu als functies worden gebruikt.
* Ondersteuning toegevoegd voor [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions) en [apply-and-reassign]((xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols)) in door gebruiker gedefinieerde typen.
* Correctieblok voor [repeat-until-succes](xref:microsoft.quantum.language.statements#repeat-until-success-loop)-lussen is nu optioneel.
* We ondersteunen nu een lus in functies (niet in bewerkingen).

### <a name="library"></a>Bibliotheek 

In deze release is een numerieke bibliotheek toegevoegd: Meer informatie over hoe u [de nieuwe numerieke bibliotheek gebruikt](xref:microsoft.quantum.numerics.usage) en de [nieuwe voorbeelden probeert](https://github.com/microsoft/quantum/tree/master/Numerics).  [PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).  

In deze release is de chemiebibliotheek opnieuw geordend en uitgebreid:
* De modulariteit van onderdelen is verbeterd en uitgebreid en de algemene code is opgeschoond.  [PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).
* Ondersteuning toegevoegd voor [wavefuncties met meerdere verwijzingen](xref:microsoft.quantum.chemistry.concepts.multireference), zowel verspreide wavefuncties met meerdere verwijzingen als unitaire gekoppelde clusters.  [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).
* (Bedankt!) [1QBit](https://1qbit.com)-inzender ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Energie-evaluatie met behulp van variatie-ansatz. [PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).
* [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)-schema bijgewerkt naar de nieuwe [versie 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2), waarbij unitaire gekoppelde clusters zijn toegevoegd. [Probleem #65](https://github.com/microsoft/QuantumLibraries/issues/65).
* Interoperabiliteit van Python toegevoegd aan functies van chemiebibliotheek. Probeer dit [voorbeeld](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration). [Probleem #53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).

## <a name="version-061905"></a>Versie 0.6.1905

*Releasedatum: 3 mei 2019*

Deze release omvat het volgende:
- wijzigingen in de Q#-taal, 
- nieuwe ordening van de Quantum Development Kit-bibliotheken, 
- nieuwe voorbeelden toegevoegd en 
- opgeloste fouten.  Verschillende gesloten pull-aanvragen voor [bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) en [voorbeelden](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

De wijzigingen zijn hier samengevat, evenals de instructies om uw huidige programma's bij te werken.  Lees meer over deze wijzigingen op devblogs.microsoft.com/qsharp.

### <a name="q-language-syntax"></a>Q#-taalsyntaxis
In deze release is een nieuwe Q#-taalsyntaxis toegevoegd:
* Een [stenomanier toegevoegd om specialisaties van kwantumbewerkingen uit te drukken](xref:microsoft.quantum.language.type-model#functors) (controles en aangrenzenden) met `+`-operators.  De oude syntaxis is afgeschaft.  Programma's die gebruikmaken van de oude syntaxis (bijvoorbeeld `: adjoint`) werken nog steeds, maar er wordt een waarschuwing voor een compilatietijd gegenereerd.  
* Nieuwe operator toegevoegd voor [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions), `w/`, kan ook worden gebruikt om het maken van een matrix uit te drukken als een wijziging van een bestaande matrix.
* De algemene [instructie apply-and-update](xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols) toegevoegd, bijvoorbeeld `+=`, `w/=`.
* Een manier toegevoegd om een korte naam op te geven voor naamruimten in [open instructies](xref:microsoft.quantum.language.file-structure#open-directives).

In deze release staan we niet meer toe dat een matrix-element wordt opgegeven aan de linkerkant van een ingestelde instructie.  Dat komt omdat de syntaxis impliceert dat matrices veranderlijk zijn, terwijl het resultaat van de bewerking altijd het maken van een nieuwe matrix met de bewerking is geweest.  In plaats daarvan wordt een compileerfout gegenereerd met een suggestie om de nieuwe operator copy-and-update, `w/`, te gebruiken om hetzelfde resultaat te bereiken.  

### <a name="library-restructuring"></a>Herstructurering van bibliotheek
In deze release zijn de bibliotheken opnieuw ingericht om te zorgen dat hun groei op een consistente manier plaatsvindt:
* De naamruimte Microsoft.Quantum.Primitive is hernoemd naar Microsoft.Quantum.Intrinsic.  Deze bewerkingen worden geïmplementeerd door de doelmachine.  De naamruimte Microsoft.Quantum.Primitive is afgeschaft.  Een runtime-waarschuwing wordt weergegeven wanneer aanroepbewerkingen en functies voor programma's afgeschafte namen gebruiken.

* Het pakket Microsoft.Quantum.Canon is hernoemd naar Microsoft.Quantum.Standard.  Dit pakket bevat naamruimten die gemeenschappelijk zijn voor de meeste Q#-programma's.  Dit omvat:  
    - Microsoft.Quantum.Canon voor algemene bewerkingen
    - Microsoft.Quantum.Arithmetic voor aritmetische bewerkingen met algemene doeleinden
    - Microsoft.Quantum.Preparation voor bewerkingen die worden gebruikt om de qubit-status voor te bereiden
    - Microsoft.Quantum.Simulation voor simulatiefunctionaliteit

Met deze wijziging treden er mogelijk opbouwfouten op in programma's met een enkele 'open' instructie voor de naamruimte Microsoft.Quatum.Canon als het programma verwijst naar bewerkingen die zijn verplaatst naar de andere drie nieuwe naamruimten.  Het toevoegen van aanvullende open instructies voor de drie nieuwe naamruimte is een logische manier om dit probleem op te lossen.  

* Verschillende naamruimten zijn aangeschaft, omdat de bewerkingen daarin zijn ingedeeld in andere naamruimten. Programma's die gebruikmaken van deze naamruimten blijven werken en een waarschuwing voor de compilatietijd geeft de naamruimte aan waar de bewerking is gedefinieerd.  

* De naamruimte Microsoft.Quantum.Arithmetic is genormaliseerd om gebruik te maken van het door de gebruiker gedefinieerde type <xref:microsoft.quantum.arithmetic.littleendian>. Gebruik de functie [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian) wanneer u die nodig hebt om een little endian te converteren.  

* De namen van verschillende callables (functies en bewerkingen) zijn gewijzigd conform de [Q#-stijlgids](xref:microsoft.quantum.contributing.style).  De oude namen van callables zijn afgeschaft.  Programma's die gebruikmaken van de oude callables blijven werken met een waarschuwing voor compilatietijd. 

### <a name="new-samples"></a>Nieuwe voorbeelden

We hebben een [gebruiksvoorbeeld voor Q# met een F#-driver](https://github.com/Microsoft/Quantum/pull/164) toegevoegd.  

**Bedankt!** aan de volgende inzender van onze open-codebasis op http://github.com/Microsoft/Quantum. Deze bijdragen zorgen voor rijke voorbeelden van Q#-code:

* Mathias Soeken ([@msoeken](https://github.com/msoeken)): Synthese van Oracle-functie. [PR #135](https://github.com/Microsoft/Quantum/pull/135).

### <a name="migrating-existing-projects-to-061905"></a>Bestaande projecten migreren naar 0.6.1905.

Raadpleeg de [installatiegids](xref:microsoft.quantum.install) om de QDK bij te werken.
  
Als u bestaande Q#-projecten van versie 0.5 van de Quantum Development Kit hebt, migreert u de projecten in de volgende stappen naar de nieuwste versie.

    1. Projecten moeten in volgorde worden bijgewerkt.  Als u een oplossing hebt met meerdere projecten, werkt u elk project bij in de volgorde waarop ernaar wordt verwezen.
    2. Voer in een opdrachtregel `dotnet clean` uit om alle bestaande binaire en tussenliggende bestanden te verwijderen.
    3. Bewerk het .csproj-bestand in een teksteditor om de versie van alle 'Microsoft.Quantum' `PackageReference` te veranderen in versie 0.6.1904 en de naam van het pakket 'Microsoft.Quantum.Canon' te veranderen in 'Microsoft.Quantum.Standard', bijvoorbeeld:

         ```xml
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
        ```
    4. Voer vanuit de opdrachtregel deze opdracht uit: `dotnet msbuild`  
    5. Nadat u de opdracht hebt uitgevoerd, moet u mogelijk nog steeds handmatig fouten aanpakken door de bovenstaande wijzigingen.  In veel gevallen worden deze fouten ook gerapporteerd door IntelliSense in Visual Studio of Visual Studio Code.
        - Open de hoofdmap van het project of de oplossing in Visual Studio 2019 of Visual Studio Code.
        - Nadat u een .qs-bestand hebt geopend in de editor, zou u de uitvoer van de Q#-taalextensie moeten zien in het uitvoervenster.
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

- Ondersteuning toegevoegd voor Jupyter Notebook, een geweldige manier om meer te leren over Q#.  [Bekijk nieuwe Jupyter Notebook-voorbeelden en leer hoe u uw eigen Notebooks schrijft](xref:microsoft.quantum.install). 

- Aritmetische toevoeging van hele getallen toegevoegd aan de Quantum Canon-bibliotheek.  Raadpleeg ook een Jupyter Notebook die [beschrijft hoe u de nieuwe toevoegingen van hele getallen gebruikt](https://github.com/microsoft/Quantum/blob/master/samples/arithmetic/AdderExample.ipynb).

- Foutoplossing voor DumpRegister-probleem die door de community is gerapporteerd ([#148](https://github.com/Microsoft/Quantum/issues/148)).

- Mogelijkheid toegevoegd om terug te keren vanuit een [gebruiksinstructie](xref:microsoft.quantum.language.statements).

- [Introductiehandleiding](xref:microsoft.quantum.install) herschreven.


## <a name="version-051902"></a>Versie 0.5.1902

*Releasedatum: 27 februari 2019*

Deze release omvat het volgende:

- Ondersteuning toegevoegd voor platformoverschrijdende Python-host.  Met het pakket `qsharp` voor Python is het eenvoudig om Q#-bewerkingen en -functies te selecteren vanuit Python. Meer informatie over [interoperabiliteit van Python](xref:microsoft.quantum.install). 

- De Visual Studio- en Visual Studio Code-extensies ondersteunen nu het hernoemen van symbolen (bijvoorbeeld functies en bewerkingen).

- De Visual Studio-extensie kan nu worden geïnstalleerd in Visual Studio 2019.

## <a name="version-041901"></a>Versie 0.4.1901

*Releasedatum: 30 januari 2019*

Deze release omvat het volgende:

- ondersteuning toegevoegd voor een nieuw primitief type, BigInt, dat een geheel getal met teken van arbitraire grootte vertegenwoordigt.  Meer informatie over het [BigInt-type](xref:microsoft.quantum.language.type-model).
- nieuwe Toffoli-simulator toegevoegd, een snelle simulator voor speciale doeleinden die X-, CNOT- en meerdere gecontroleerde X-kwantumbewerkingen kan simuleren met grote aantallen qubits.  Meer informatie over de [Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator).
- een eenvoudige resource-inschatting toegevoegd die een schatting maakt van het aantal benodigde resources om een bepaald exemplaar uit te voeren van een Q#-bewerking in een kwantumcomputer.  Meer informatie over [Resource-inschatting](xref:microsoft.quantum.machines.resources-estimator).


## <a name="version-0318112802"></a>Versie 0.3.1811.2802

*Releasedatum: 28 november 2018*

Hoewel onze VS Code-extensie er geen gebruik van maakte, is een waarschuwing opgetreden en is het verwijderd uit de marketplace tijdens [de extensieverwijdering](https://code.visualstudio.com/blogs/2018/11/26/event-stream) met betrekking tot het NPM-pakket `event-stream`. In deze versie zijn alle runtime-afhankelijkheden verwijderd die een waarschuwing konden activeren in de extensie.

Als u de extensie eerder hebt geïnstalleerd, moet u deze opnieuw installeren. Ga naar de extensie [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode) in de Visual Studio-marketplace en klik op Installeren. Onze excuses voor het ongemak.


## <a name="version-0318111511"></a>Versie 0.3.1811.1511

*Releasedatum: 20 november 2018*

In deze release wordt een fout opgelost waardoor sommige gebruikers de Visual Studio-extensie niet konden laden.

Als u upgradet van de versie 0.2 van de Quantum Development Kit, gaat u voor meer informatie naar [Q#-taalwijzigingen en uw Q#-programma migreren](xref:microsoft.quantum.relnotes.migration-0-3).

## <a name="version-031811203"></a>Versie 0.3.1811.203

*Releasedatum: 2 november 2018*

Deze release bevat enkele foutoplossingen, waaronder voor de volgende:

* `DumpMachine` aanroepen kon ervoor zorgen dat de status van de simulator onder bepaalde omstandigheden veranderde.
* Compilatiewaarschuwingen verwijderd bij het bouwen van projecten met een versie van .NET Core voor 2.1.403.
* Documentatie opgeschoond, in het bijzonder de tooltips die worden weergegeven wanneer in VS Code of Visual Studio de muisaanwijzer op een item wordt geplaatst.

Als u upgradet van de versie 0.2 van de Quantum Development Kit, gaat u voor meer informatie naar [Q#-taalwijzigingen en uw Q#-programma migreren](xref:microsoft.quantum.relnotes.migration-0-3).

## <a name="version-0318102508"></a>Versie 0.3.1810.2508

*Releasedatum: 29 oktober 2018*

Deze release bevat nieuwe taalfuncties en een verbeterde ontwikkelaarservaring:

* Deze release bevat een taalserver voor Q#, evenals clientintegraties voor Visual Studio en Visual Studio Code. Hierdoor zijn meer IntelliSense-functies mogelijk, evenals live feedback bij typen, in de vorm van krabbeltjes onder fouten en waarschuwingen. 
* Met deze update worden diagnostische berichten in het algemeen aanzienlijk verbeterd, met eenvoudige navigatie naar en precieze bereiken voor diagnostische gegevens en aanvullende informatie in de weergegeven, zwevende informatie.
* De Q#-taal is dusdanig uitgebreid dat ontwikkelaars op een uniforme manier bewerkingen kunnen uitvoeren en er zijn nieuwe verbeteringen voor taalfuncties doorgevoerd om kwantumberekeningen beter uit te drukken.  Deze release bevat een aantal wijzigingen die fouten veroorzaken in de Q#-taal.   

Meer informatie over [Q#-taalwijzigingen en het migreren van uw Q#-programma](xref:microsoft.quantum.relnotes.migration-0-3).

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
* In de documentatie wordt beschreven hoe u NWChem gebruikt om aanvullende chemische modellen te genereren voor kwantumsimulatie met Q#.

Meer informatie over de [Quantum Development Kit-chemiebibliotheek](xref:microsoft.quantum.chemistry.concepts.intro).

Met de nieuwe chemiebibliotheek plaatsen we de bibliotheken in een nieuwe GitHub-opslagplaats, [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).  De voorbeelden bevinden zich in de opslagplaats [Microsoft/Quantum](https://github.com/Microsoft/Quantum).  Bijdragen aan beide zijn welkom.

Deze release omvat foutoplossingen en functies voor problemen die door de community zijn gemeld:

* IntelliSense voor Q#? ([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918)).
* .qs-bestanden ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049)).
* Foutbericht verbeterd wanneer accolades worden afgekort in de if-instructie ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518)).
* Ondersteuning voor tuple-ontsleuteling bij onveranderlijke (her)binding ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444)).
* Fout bij de uitvoering van opgegeven BitFlipCode ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).
* H2SimulationGUI geeft soms grote pieken weer ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).

### <a name="community-contributions"></a>Bijdragen van de community

**Bedankt!** aan de volgende inzenders van onze open-codebasis op http://github.com/Microsoft/Quantum. Deze bijdragen zorgen voor rijke voorbeelden van Q#-code:

* Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)): Verbeterde ervaring voor QASM/Q#-ontwikkelaars door een vertaler te maken voor QASM naar Q#. [PR #58](https://github.com/Microsoft/Quantum/pull/58).

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

Deze release is een snelle oplossing voor [probleem #48 in GitHub](https://github.com/Microsoft/Quantum/issues/48) (Q#-compilatie mislukt als de gebruikersnaam een lege ruimte bevat). Volg dezelfde update-instructies als `0.2.1806.1503` met de bijbehorende nieuwe versie (`0.2.1806.3001-preview`).

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

Meer informatie over [testen en foutopsporing](xref:microsoft.quantum.techniques.testing-and-debugging).

### <a name="community-contributions"></a>Bijdragen van de community

De Q#-codecommunity groeit en we zijn enthousiast om te zien dat de eerste gebruiker bibliotheken en voorbeelden heeft bijgedragen die zijn ingediend in onze open-codebasis op http://github.com/Microsoft/quantum.  **Hartelijk dank!** aan de volgende inzenders:
* Mathias Soeken ([@msoeken](https://github.com/msoeken)): heeft een voorbeeld bijgedragen dat een op transformatie gebaseerde logische synthesemethode definieert waarmee Toffoli-netwerken worden gemaakt om een bepaalde permutatie te implementeren. De code is volledig geschreven in Q#-functies en -bewerkingen.  [PR #41](https://github.com/Microsoft/Quantum/pull/41).
* Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)): MVP van Microsoft Rolf Huisman heeft een voorbeeld bijgedragen die QASM-code genereert van Q#-code voor een beperkte klasse programma's die niet beschikken over klassieke controlestroom en beperkte kwantumbewerkingen. [PR #59](https://github.com/Microsoft/Quantum/pull/59)
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
1. Maak een nieuw .NET Core-project met het juiste type Q#-projectsjabloon (toepassing, bibliotheek of testproject).
2. Kopieer bestaande .qs- en .cs-/.fs-bestanden van het oude project naar het nieuwe project (met behulp van Toevoegen > Bestaand item). Kopieer het bestand AssemblyInfo.cs niet.
3. Bouw het nieuwe project en voer het uit.

Houd er rekening mee dat de bewerking RandomWalkPhaseEstimation van de raamruimte Microsoft.Quantum.Canon is verplaatst naar de naamruimte Microsoft.Research.Quantum.RandomWalkPhaseEstimation in de opslagplaats [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc).

### <a name="known-issues"></a>Bekende problemen

- De optie `--filter` voor `dotnet test` werkt niet correct voor tests die zijn geschreven in Q#.
  Als gevolg hiervan kunnen afzonderlijke moduletests niet worden uitgevoerd in Visual Studio Code. We raden aan dat u `dotnet test` gebruikt in de opdrachtregel om alle tests opnieuw uit te voeren.

## <a name="version-0118011707"></a>Versie 0.1.1801.1707

*Releasedatum: 18 januari 2018*

In deze release is een aantal fouten opgelost die zijn gemeld door de community. In het bijzonder:

- De simulator werkt nu met eerdere CPU's zonder AVX-functionaliteit.
- Regionale instellingen voor decimalen zorgen er niet meer voor dat Q#-parsering mislukt.
- De primitieve bewerking `SignD` retourneert nu `Int` in plaats van `Double`.


## <a name="version-011712901"></a>Versie 0.1.1712.901

*Releasedatum: 11 december 2017*

### <a name="known-issues"></a>Bekende problemen

#### <a name="hardware-and-software-requirements"></a>Hardware-en software vereisten

- Om de simulator in de Quantum Development Kit uit te voeren, is een 64-bits installatie van Microsoft Windows vereist.
- De kwantumsimulator van Microsoft, geïnstalleerd met de Quantum Development Kit, maakt gebruik van Advanced Vector Extensions (AVX) en vereist een CPU met AVX-functionaliteit. Intel-processors die zijn verzonden in Q1 van 2011 (Sandy Bridge) of later ondersteunen AVX. We evalueren ondersteuning voor eerdere CPU's en kondigen mogelijk later details aan.

#### <a name="project-creation"></a>Een project maken

- Wanneer u een oplossing (.sln) maakt die gebruikmaakt van Q#, moet de oplossing één map hoger liggen dan elk project (.csproj) in de oplossing. Wanneer u een nieuwe oplossing maakt, doet u dit door ervoor te zorgen dat het selectievakje 'Map voor oplossing maken' in het dialoogvenster 'Nieuw project' is aangevinkt. Als dit niet is gebeurd, moeten de NuGet-pakketten van de Quantum Development Kit handmatig worden geïnstalleerd.

#### <a name="q"></a>Q#

- IntelliSense geeft de juiste fouten voor Q#-code niet weer. Zorg ervoor dat u opbouwfouten weergeeft in de foutenlijst van Visual Studio om de juiste Q#-fouten te bekijken. Houd er ook rekening mee dat Q#-fouten pas verschijnen nadat u een build hebt uitgevoerd.
- Het gebruik van een onveranderlijke matrix in een gedeeltelijke toepassing leidt mogelijk tot onverwacht gedrag.
- Als u een veranderlijke matrix bindt aan een onveranderlijke (bijvoorbeeld a = b, waar b een onveranderlijke matrix is), leidt dat mogelijk tot onverwacht gedrag.
- Profielsamenstelling, codedekking en andere VS-invoegtoepassingen tellen Q#-regels en -blokken niet altijd nauwkeurig.
- De Q#-compiler valideert intergepoleerde tekenreeksen niet. Het is mogelijk om C#-compilatiefouten te maken door namen van variabelen verkeerd te spellen of gebruik te maken van expressies in intergepoleerde Q#-tekenreeksen.

#### <a name="simulation"></a>Simulatie

- De QuantumSimulator maakt gebruik van OpenMP om de vereiste lineaire algebra te parallelliseren. OpenMP gebruikt standaard alle beschikbare hardware-threads, wat wil zeggen dat programma's met kleine aantallen qubits vaak langzaam worden uitgevoerd door de coördinatie die nodig is om het werkelijke werk te klein te laten lijken. Dit kan worden opgelost door de omgevingsvariable OMP_NUM_THREADS in te stellen op een kleiner getal. Als brede richtlijn is één thread goed voor ongeveer vier qubits en is vervolgens een aanvullende thread per qubit goed, hoewel dit zeer afhankelijk is van uw algoritme.

#### <a name="debugging"></a>Foutopsporing

- F11 (stap) werkt niet in Q#-code.
- Codemarkering in Q#-code in een onderbrekingspunt of een enkele onderbreking is soms onnauwkeurig. De juiste regel wordt gemarkeerd, maar soms begint en eindigt de markering bij onjuiste kolommen in de regel.

#### <a name="testing"></a>Testen

- Tests moeten worden uitgevoerd in 64-bits modus. Als uw tests mislukken met BadImageFormatException, gaat u naar het menu Test en selecteert u Testinstellingen > Standaard processorarchitectuur > X64.
- Sommige tests duren lang (waarschijnlijk vijf minuten, afhankelijk van uw computer). Dat is normaal, aangezien sommige tests meer dan 20 qubits gebruiken. Onze grootste test wordt momenteel uitgevoerd op 23 qubits.

#### <a name="samples"></a>Voorbeelden

- In sommige machines is het mogelijk dat sommige kleine voorbeelden langzaam worden uitgevoerd, tenzij de omgevingsvariabele OMP_NUM_THREADS is ingesteld op '1'. Raadpleeg ook de releaseopmerking onder 'Simulatie'.

#### <a name="libraries"></a>Bibliotheken

- Er is een impliciete veronderstelling dat de qubits die worden doorgevoerd naar een bewerking in verschillende argumenten, allemaal verschillend zijn. Alle bibliotheekbewerkingen (en alle simulatoren) gaan er bijvoorbeeld vanuit dat de twee qubits die worden doorgevoerd naar een gecontroleerde NOT, verschillende qubits zijn. Als deze aanname wordt geschonden, leidt dat mogelijk tot onverwacht gedrag. Het is mogelijk om hierop te testen met de traceringssimulator voor kwantumcomputers.
- De functie Microsoft.Quantum.Bind gedraagt zich mogelijk niet alle gevallen zoals verwacht.
- In de naamruimte Microsoft.Quantum.Extensions.Math retourneert de functie SignD een Double in plaats van een Int, hoewel de onderliggende functie System.Math.Sign altijd een geheel getal retourneert. De resultaten kunnen worden vergeleken met 1.0, -1.0 en 0.0, aangezien al deze dubbelen exacte binaire vertegenwoordigingen hebben.
