---
title: Manieren om een programma uit te voeren Q#
description: Overzicht van de verschillende manieren om Program ma's uit te voeren Q# . Vanaf de opdracht prompt, Q# Jupyter-notebooks en klassieke host-Program ma's in Python of een .net-taal.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: e44a366b7eea133499beb44dbb338a02174c0073
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863194"
---
# <a name="ways-to-run-a-no-locq-program"></a>Manieren om een programma uit te voeren Q#

Een van de grootste sterke punten van de Quantum Development Kit is de flexibiliteit tussen platforms en ontwikkel omgevingen.
Dit betekent echter ook dat nieuwe Q# gebruikers zichzelf kunnen vinden of worden overspoeld door de talloze opties die in de [installatie handleiding](xref:microsoft.quantum.install)worden gevonden.
Op deze pagina wordt uitgelegd wat er gebeurt wanneer een Q# programma wordt uitgevoerd en kunt u de verschillende manieren vergelijken waarop gebruikers dit kunnen doen.

Een primair onderscheid is dat Q# kan worden uitgevoerd:
- als zelfstandige toepassing, waarbij de Q# enige taal betrokken is en het programma rechtstreeks wordt aangeroepen. In deze categorie vallen twee methoden daad werkelijk:
  - de opdracht regel interface
  - Q# Jupyter-notebooks
- met een extra *hostprogramma*, geschreven in Python of een .net-taal (bijvoorbeeld C# of F #), die vervolgens het programma aanroept en de geretourneerde resultaten verder kan verwerken.

Voor een beter begrip van deze processen en hun verschillen, wordt een eenvoudig Q# programma beschouwd en worden de manieren vergeleken waarop het proces kan worden uitgevoerd.

## <a name="basic-no-locq-program"></a>Basic- Q# programma

Een basis Quantum programma kan bestaan uit het voorbereiden van een Qubit in een gelijke superpositie van Staten $ \ket {0} $ en $ \ket {1} $, het meten ervan en het retour neren van het resultaat, dat wille keurig een van beide statussen met een gelijke kans is.
Dit proces is inderdaad de kern van de versnelde Generator van de [Quantum wille keurige getallen](xref:microsoft.quantum.quickstarts.qrng) .

In Q# wordt dit uitgevoerd met de volgende code:

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

Deze code kan echter alleen worden uitgevoerd door Q# .
Hiervoor moet de hoofd tekst van een [bewerking](xref:microsoft.quantum.guide.basics#q-operations-and-functions)worden uitgevoerd, die vervolgens rechtstreeks of door een andere bewerking wordt aangeroepen---. Daarom kunt u een bewerking van het volgende formulier schrijven:
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
U hebt een bewerking gedefinieerd, `MeasureSuperposition` die geen invoer heeft en een waarde van het type [resultaat](xref:microsoft.quantum.guide.types)retourneert.

Hoewel de voor beelden op deze pagina alleen bestaan uit Q# *bewerkingen*, zijn alle concepten die we bespreken gelijk aan de Q# *functies*en daarom verwijzen ze gezamenlijk naar hun *callables*. Hun verschillen worden besproken op basis van het [ Q# volgende: bewerkingen en functies](xref:microsoft.quantum.guide.basics#q-operations-and-functions), en meer informatie over het definiëren van ze vindt u op [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions).

### <a name="callable-defined-in-a-no-locq-file"></a>Aanroepable gedefinieerd in een Q# bestand

De aanroep zou precies worden aangeroepen en worden uitgevoerd door Q# .
Er zijn echter enkele extra toevoegingen vereist om een volledig bestand te vormen `*.qs` Q# .

Alle Q# typen en callables (zowel die u hebt gedefinieerd als de ingebouwde taal) worden gedefinieerd in *naam ruimten*, die elke volledige naam geven waarnaar vervolgens kan worden verwezen.

De [`H`](xref:microsoft.quantum.intrinsic.h) bewerkingen en zijn bijvoorbeeld te [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) vinden in de [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) naam ruimten en (onderdeel van de [ Q# standaard bibliotheken](xref:microsoft.quantum.qsharplibintro)).
Zo kunnen ze altijd worden aangeroepen via hun *volledige* naam `Microsoft.Quantum.Intrinsic.H(<qubit>)` en `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` , maar dit wordt altijd wel tot zeer ruime code.

In plaats daarvan `open` kunnen met behulp van de instructies callables worden gerefereerd aan een beknoptere steno, zoals in de bovenstaande hoofd tekst is uitgevoerd.
Het volledige Q# bestand met onze bewerking zou daarom bestaan uit het definiëren van onze eigen naam ruimte, het openen van de naam ruimten voor de callables die door onze bewerking worden gebruikt, en de bewerking:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> Naam ruimten kunnen ook worden *gealiasd* wanneer deze worden geopend. Dit kan handig zijn als er sprake is van aanroep bare/type namen in twee naam ruimten.
> We kunnen bijvoorbeeld in plaats daarvan `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` hierboven gebruiken en vervolgens aanroepen `H` via `NamespaceWithH.H(<qubit>)` .

> [!NOTE]
> Een uitzonde ring op dit is de [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) naam ruimte, die altijd automatisch wordt geopend.
> Daarom kan callables bijvoorbeeld [`Length`](xref:microsoft.quantum.core.length) altijd rechtstreeks worden gebruikt.

### <a name="execution-on-target-machines"></a>Uitvoering op doel computers

Het algemene uitvoerings model van een Q# programma wordt nu duidelijk.

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

De specifieke aanroepable die moet worden uitgevoerd, heeft eerst toegang tot andere callables en typen die in dezelfde naam ruimte zijn gedefinieerd.
U kunt ook toegang krijgen tot die van een van de [ Q# bibliotheken](xref:microsoft.quantum.libraries), maar deze moeten worden gerefereerd via de volledige naam of door middel van het gebruik van de `open` hierboven beschreven instructies.

De aanroep kan zelf worden uitgevoerd op een *[doel computer](xref:microsoft.quantum.machines)*.
Dergelijke doel computers kunnen echte Quantum hardware zijn of de meerdere simulatoren die beschikbaar zijn als onderdeel van de QDK.
Voor onze doel einden is de meest nuttige doel computer een exemplaar van de [Full-State Simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` waarmee het gedrag van het programma wordt berekend alsof het wordt uitgevoerd op een quantum computer zonder ruis.

Tot nu toe hebben we beschreven wat er gebeurt wanneer een specifieke Q# aanroepable wordt uitgevoerd.
Ongeacht of het wordt Q# gebruikt in een zelfstandige toepassing of met een gast programma, is dit algemene proces meer of minder hetzelfde---dus de flexibiliteit van QDK.
De verschillen tussen de verschillende manieren van aanroepen in de Quantum Development Kit geven daarom duidelijk aan *hoe* die Q# aanroep bare wordt uitgevoerd en op welke manier de resultaten worden geretourneerd.
In het bijzonder zijn de verschillen van belang om 
1. Hiermee wordt aangegeven welke Q# aanroepable moet worden uitgevoerd.
2. Hoe mogelijke aanroep bare argumenten worden gegeven,
3. opgeven van de doel computer waarop deze moet worden uitgevoerd, en
4. hoe er resultaten worden geretourneerd.

Eerst bespreken we hoe dit wordt gedaan met de Q# zelfstandige toepassing vanaf de opdracht prompt en gaat u verder met het gebruik van python-en C#-host-Program ma's.
We behouden de zelfstandige toepassing van Q# Jupyter-notebooks voor het laatst aan, omdat de primaire functionaliteit in tegens telling tot de eerste drie niet is gecentreerd rond een lokaal Q# bestand.

> [!NOTE]
> Hoewel we dit niet in deze voor beelden illustreren, is een gemeen schappelijk tussen de uitvoerings methoden dat elke wille keurige berichten die vanuit het programma worden afgedrukt Q# (via [`Message`](xref:microsoft.quantum.intrinsic.message) of [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) bijvoorbeeld), altijd worden afgedrukt op de respectieve console.

## <a name="no-locq-from-the-command-prompt"></a>Q# vanaf de opdracht prompt
Een van de eenvoudigste manieren om aan de slag te gaan met het schrijven Q# van Program ma's is om te voor komen dat u zich zorgen maakt over afzonderlijke bestanden en een tweede taal.
Het gebruik van Visual Studio code of Visual Studio met de QDK-extensie biedt een naadloze werk stroom waarbij we Q# callables uit slechts één Q# bestand uitvoeren.

Hiervoor wordt de uitvoering van het programma uiteindelijk opgeroepen door het volgende in te voeren:
```dotnetcli
dotnet run
```
bij de opdracht prompt.
De eenvoudigste werk stroom is wanneer de locatie van de map van de Terminal gelijk is aan die van het Q# bestand, dat eenvoudig kan worden verwerkt naast het Q# bewerken van bestanden met behulp van de geïntegreerde terminal in VS code.
De [ `dotnet run` opdracht](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepteert echter talloze opties en het programma kan ook worden uitgevoerd vanaf een andere locatie door simpelweg `--project <PATH>` de locatie van het bestand op te geven Q# .


### <a name="add-entry-point-to-no-locq-file"></a>Invoer punt toevoegen aan Q# bestand

De meeste Q# bestanden bevatten meer dan één aanroepable, dus we moeten er natuurlijk voor zorgen dat de compiler weet *welke* aanroep kan worden uitgevoerd wanneer we de `dotnet run` opdracht opgeven.
Dit wordt gedaan met een eenvoudige wijziging in het Q# bestand zelf: 
    - Voeg een regel toe met `@EntryPoint()` de direct voorafgaande oproep bare.

Ons bestand van bovenstaande zou daarom worden
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

Nu wordt een aanroep van `dotnet run` vanaf de opdracht prompt om te `MeasureSuperposition` worden uitgevoerd en wordt de geretourneerde waarde vervolgens rechtstreeks naar de Terminal afgedrukt.
Daarom ziet u ofwel `One` of `Zero` afgedrukt. 

Houd er rekening mee dat het niet van belang is dat er meer callables worden gedefinieerd, maar alleen `MeasureSuperposition` worden uitgevoerd.
Daarnaast is het geen probleem als uw aanroep mogelijk [documentatie commentaar](xref:microsoft.quantum.guide.filestructure#documentation-comments) bevat vóór de declaratie van het `@EntryPoint()` kenmerk, maar dit kan eenvoudigweg worden geplaatst.

### <a name="callable-arguments"></a>Aanroep bare argumenten

Tot nu toe hebben we alleen een bewerking gezien die geen invoer heeft.
Stel dat we een vergelijk bare bewerking willen uitvoeren, maar op meerdere qubits---het aantal dat als argument wordt gegeven.
Een dergelijke bewerking kan worden geschreven als
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
waarbij de geretourneerde waarde een matrix is van de meet resultaten.
Houd er rekening mee dat [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) en [`ForEach`](xref:microsoft.quantum.arrays.foreach) zich in de en de naam ruimte bevindt [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) . hiervoor [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) moeten aanvullende instructies worden vereist `open` .

Als we het `@EntryPoint()` kenmerk voorafgaand aan deze nieuwe bewerking verplaatsen (Houd er dan rekening mee dat er slechts één regel in een bestand kan worden uitgevoerd). er wordt geprobeerd deze uit te voeren met alleen `dotnet run` resultaten in een fout bericht dat aangeeft welke extra opdracht regel opties vereist zijn en hoe u deze kunt uitdrukken.

De algemene notatie voor de opdracht regel is in werkelijkheid `dotnet run [options]` en aanroep bare argumenten worden daar vermeld.
In dit geval ontbreekt het argument `n` en ziet u dat we de optie moeten opgeven `-n <n>` . Om uit te voeren `MeasureSuperpositionArray` voor `n=4` qubits, gebruiken we daarom

```dotnetcli
dotnet run -n 4
```

levert een uitvoer op die vergelijkbaar is met

```output
[Zero,One,One,One]
```

Deze cursus wordt uitgebreid naar meerdere argumenten.

> [!NOTE]
> Argument namen die zijn gedefinieerd in `camelCase` , worden enigszins gewijzigd door de compiler om te worden geaccepteerd als Q# invoer. Als `n` we bijvoorbeeld de bovenstaande naam hebben gebruikt `numQubits` , wordt deze invoer opgegeven in de opdracht regel in `--num-qubits 4` plaats van `-n 4` .

Het fout bericht bevat ook andere opties die kunnen worden gebruikt, met inbegrip van het wijzigen van de doel computer.

### <a name="different-target-machines"></a>Verschillende doel computers

Omdat de uitvoer van onze activiteiten tot nu toe de verwachte resultaten van hun actie op echte qubits was, is het duidelijk dat de standaard doel computer van de opdracht regel de Full-State Quantum Simulator is `QuantumSimulator` .
We kunnen er echter voor zorgen dat callables worden uitgevoerd op een specifieke doel computer met de optie `--simulator` (of de steno `-s` ).

Dit kan bijvoorbeeld worden uitgevoerd op [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

De afgedrukte uitvoer wordt vervolgens

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

Zie [resource Estimator: metrische](xref:microsoft.quantum.machines.resources-estimator#metrics-reported)gegevens voor meer informatie over wat deze metrische gegevens aangeven.

### <a name="command-line-execution-summary"></a>Samen vatting van uitvoering van opdracht regel
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a>Niet- Q# `dotnet run` Opties

Zoals hierboven hierboven vermeld met de `--project` optie, accepteert de [ `dotnet run` opdracht](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) ook opties die niet gerelateerd zijn aan de Q# aanroep bare argumenten.
Als u beide soorten opties opgeeft, `dotnet` moeten de specifieke opties eerst worden opgegeven, gevolgd door een delimiter `--` , en vervolgens de Q# -specifieke opties.
Specifiying bijvoorbeeld een pad samen met een qubits voor de bovenstaande bewerking zou worden uitgevoerd via `dotnet run --project <PATH> -- -n <n>` .

## <a name="no-locq-with-host-programs"></a>Q# met host-Program ma's

Met ons Q# bestand is een alternatief voor het aanroepen van een bewerking of functie rechtstreeks vanaf de opdracht prompt het gebruik van een *hostprogramma* in een andere klassieke taal. Dit kan met name worden gedaan met python of een .NET-taal, zoals C# of F # (in het geval van een beknopt overzicht van de informatie over C#.
Er zijn nog meer instellingen vereist om de interoperabiliteit in te scha kelen, maar u kunt deze details vinden in de [installatie handleidingen](xref:microsoft.quantum.install).

In een kort gezegd bevat de situatie nu een bestand van een host (bijvoorbeeld `*.py` of `*.cs` ) op dezelfde locatie als het Q# bestand.
Het is nu het *hostprogramma* dat wordt uitgevoerd, en in de loop van de uitvoering kunnen specifieke Q# bewerkingen en functies vanuit het bestand worden aangeroepen Q# .
De kern van de interoperabiliteit is gebaseerd op de Q# compiler die de inhoud van het Q# bestand toegankelijk maakt voor het hostprogramma, zodat deze kan worden aangeroepen.

Een van de belangrijkste voor delen van het gebruik van een hostprogramma is dat de klassieke gegevens die door het Q# programma worden geretourneerd, vervolgens verder kunnen worden verwerkt in de taal van de host.
Dit kan bestaan uit een aantal geavanceerde gegevens verwerking (bijvoorbeeld iets dat niet intern kan worden uitgevoerd Q# ) en vervolgens aanroepen van verdere Q# acties op basis van deze resultaten, of iets zo eenvoudig als het uitzetten van de Q# resultaten.

Het algemene schema wordt hier weer gegeven en we bespreken de specifieke implementaties voor python en C# hieronder. Een voor beeld van het gebruik van een F #-hostprogramma vindt u in de voor [beelden van .net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> Het `@EntryPoint()` kenmerk dat voor toepassingen wordt gebruikt, Q# kan niet worden gebruikt met host-Program ma's.
> Er wordt een fout gegenereerd als deze aanwezig is in het Q# bestand dat wordt aangeroepen door een host. 

Als u wilt werken met andere host-Program ma's, hoeft u geen wijzigingen aan te brengen in een `*.qs` Q# bestand.
De volgende implementaties van een host-programma werken allemaal met hetzelfde Q# bestand:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

Selecteer het tabblad dat overeenkomt met de taal van uw host.

### <a name="python"></a>[Python](#tab/tabid-python)
Een python-hostprogramma is als volgt samengesteld:
1. Importeer de `qsharp` module, die de module lader voor interoperabiliteit registreert Q# . 
    Op die manier kunnen Q# naam ruimten worden weer gegeven als python-modules, waaruit we callables kunnen importeren Q# .
    Houd er rekening mee dat het technisch gezien niet het Q# callables is dat wordt geïmporteerd, maar dat er python-stubs zijn waarmee ze kunnen worden aangeroepen.
    Deze werken vervolgens als objecten van python-klassen, waarop we methoden gebruiken om de doel machines op te geven waarnaar de bewerking moet worden verzonden.

2. Importeer de Q# callables die in dit geval direct---worden aangeroepen, `MeasureSuperposition` en `MeasureSuperpositionArray` .
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    Als de `qsharp` module is geïmporteerd, kunt u ook rechtstreeks vanuit de Q# bibliotheek naam ruimten callables importeren.

3. Onder andere python-code kunt u deze callables op specifieke doel computers aanroepen en de bijbehorende retour waarden toewijzen aan variabelen (als ze een waarde Retour neren) voor verder gebruik.

#### <a name="specifying-target-machines"></a>Doel machines opgeven
Het aanroepen van een bewerking die moet worden uitgevoerd op een specifieke doel computer, wordt uitgevoerd via verschillende python-methoden voor het geïmporteerde object.
`.simulate(<args>)`Maakt bijvoorbeeld gebruik `QuantumSimulator` van de om de bewerking uit te voeren, terwijl dat `.estimate_resources(<args>)` wel het geval is `ResourcesEstimator` .

#### <a name="passing-inputs-to-q"></a>Invoer door geven aan Q\#
Argumenten voor de Q# aanroepable moeten worden aangegeven in de vorm van een trefwoord argument, waarbij het sleutel woord de argument naam in de Q# aanroep bare definitie is.
Dat wil zeggen, `MeasureSuperpositionArray.simulate(n=4)` is geldig, terwijl `MeasureSuperpositionArray.simulate(4)` een fout optreedt.

Daarom wordt het python-hostprogramma 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

resulteert in een uitvoer zoals de volgende:

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a>Q#Code uit andere projecten of pakketten gebruiken

Standaard `import qsharp` laadt de opdracht alle `.qs` bestanden in de huidige map en Q# worden de bewerkingen en functies beschikbaar voor gebruik in het python-script.

Als u Q# code wilt laden vanuit een andere map, kan de [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp/qsharp.projects.projects) worden gebruikt voor het toevoegen van een verwijzing naar een `.csproj` bestand voor een Q# project (dat wil zeggen een project waarnaar wordt verwezen `Microsoft.Quantum.Sdk` ).
Met deze opdracht worden alle `.qs` bestanden in de map die de submappen bevat, gecompileerd `.csproj` . Ook worden alle pakketten die via of projecten verwijzen waarnaar wordt `PackageReference` Q# verwezen `ProjectReference` in dat bestand, recursief geladen `.csproj` .

Met de volgende python-code wordt bijvoorbeeld een extern project geïmporteerd, dat verwijst naar het pad ten opzichte van de huidige map en wordt een van de Q# bewerkingen aangeroepen:

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

Dit resulteert in uitvoer als de volgende:

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

Als u externe pakketten wilt laden die Q# code bevatten, gebruikt u de [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages).

Als de Q# code in de huidige map afhankelijk is van externe projecten of pakketten, kunnen er fouten optreden tijdens `import qsharp` de uitvoering, omdat de afhankelijkheden nog niet zijn geladen.
Als u de vereiste externe pakketten of Q# projecten tijdens de opdracht wilt laden, moet u `import qsharp` ervoor zorgen dat de map met het python-script een `.csproj` bestand bevat waarnaar wordt verwezen `Microsoft.Quantum.Sdk` . Voeg in dat `.csproj` de eigenschap toe `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` aan de `<PropertyGroup>` . Dit geeft de instructie Q# om een of meer items te `ProjectReference` laden `PackageReference` die zijn gevonden in die `.csproj` tijdens de `import qsharp` opdracht.

Dit is bijvoorbeeld een eenvoudig `.csproj` bestand dat ervoor zorgt dat Q# het pakket automatisch wordt geladen `Microsoft.Quantum.Chemistry` :

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> Deze aangepaste `<IQSharpLoadAutomatically>` eigenschap is momenteel vereist voor python-hosts, maar in de toekomst kan dit het standaard gedrag voor een bestand zijn dat `.csproj` zich in dezelfde map bevindt als het python-script.

> [!NOTE]
> Momenteel `<QsharpCompile>` wordt de instelling in de `.csproj` wordt genegeerd door python-hosts en `.qs` worden alle bestanden in de map `.csproj` (inclusief submappen) geladen en gecompileerd. Ondersteuning voor `.csproj` instellingen wordt in de toekomst verbeterd (Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor meer informatie).


### <a name="c"></a>[C#](#tab/tabid-csharp)

Een C#-hostprogramma heeft meerdere onderdelen en werkt zeer nauw samen met enkele onderdelen van de QDK, zoals de simulators die zelf zijn gebouwd op C#.

De Q# compiler werkt hier door een overeenkomende C#-naam ruimte te genereren uit de Q# naam ruimte in het Q# bestand.
Daarnaast wordt er een gelijkwaardige C#-klasse gegenereerd voor elk van de Q# callables of typen die daarin zijn gedefinieerd.

Eerst maken we de klassen die in ons hostprogramma worden gebruikt, beschikbaar met `using` instructies, die ongeveer analagous zijn voor de `open` instructies in ons Q# bestand:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

Vervolgens declareren we onze C#-naam ruimte, een paar andere bits en delen (Zie het volledige code blok hieronder) en vervolgens een klassieke programmering (zoals het berekenen van argumenten voor de Q# callables).
Dit is niet nodig in ons geval, maar een voor beeld van een dergelijk gebruik is te vinden in het voor  [beeld van .net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

#### <a name="target-machines"></a>Doelcomputers

Als u terugkeert naar Q# , moeten we een instantie maken van de doel computer waarop we onze bewerkingen zullen uitvoeren.

```csharp
            using var sim = new QuantumSimulator();
```

Het gebruik van andere doel machines is net zo eenvoudig als het instantiëren van een andere computer, hoewel de manier waarop u dit doet en het verwerken van de geretourneerde items iets anders kan zijn.
Voor het oog op de boog is het [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) nu van toepassing op de voor-en de voor beelden [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).

Elke C#-klasse die is gegenereerd op basis van de Q# bewerkingen, heeft een `Run` methode, het eerste argument waarvan het doel computer exemplaar moet zijn.
Daarom gebruiken we om uit te voeren `MeasureSuperposition` op de `QuantumSimulator` `MeasureSuperposition.Run(sim)` .
De geretourneerde resultaten kunnen vervolgens worden toegewezen aan variabelen in C#:

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> De `Run` methode wordt asynchroon uitgevoerd, omdat dit het geval is voor echte Quantum hardware `await` . het sleutel woord blokkeert daarom verder totdat de taak is voltooid.

Als de Q# aanroep geen retouren heeft (bijvoorbeeld retour type `Unit` ), kan de uitvoering nog steeds op dezelfde manier worden uitgevoerd zonder deze aan een variabele toe te wijzen.
In dat geval zou de volledige regel gewoon bestaan uit 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a>Argumenten

Argumenten die kunnen worden Q# aangeroepen, worden eenvoudigweg door gegeven als aanvullende argumenten wanneer de doel machine.
Daarom worden de resultaten van `MeasureSuperpositionArray` op `n=4` qubits opgehaald via 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

Een volledig C#-hostprogramma kan er dus als volgt uitzien

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

Op de locatie van het C#-bestand kan het host-programma worden uitgevoerd vanaf de opdracht prompt door het in te voeren
```dotnetcli
dotnet run
```
in dit geval ziet u uitvoer die is geschreven naar de-console, vergelijkbaar met 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> Als gevolg van de interoperabiliteit van de compiler met naam ruimten, kunnen we een andere Q# callables beschikbaar maken zonder de `using NamespaceName;` -instructie, en alleen de naam van de C#-titel ruimte erop.
> Dat wil zeggen door te vervangen door `namespace host` `namespace NamespaceName` .

#### <a name="including-the-resources-estimator"></a>Inclusief de bronnen estimator

[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Er is een iets andere implementatie vereist om de uitvoer op te halen.

In plaats van ze als een variabele te instantiëren met een- `using` instructie (zoals we met de) hebben gedaan `QuantumSimulator` , kunnen we objecten van de klasse direct instantiëren via

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

U ziet dat in plaats van één doel-Simulator door meerdere bewerkingen wordt gebruikt Q# , er één voor elk wordt geïnstantieerd. Dit komt doordat de objecten zelf worden gewijzigd wanneer ze worden gebruikt als doel machines en de resultaten ervan daarna kunnen worden opgehaald met de methode Class `.ToTSV()` .

Voor het uitvoeren van de bewerkingen op resource schattingen gebruiken we

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
Daarna haalt u de resultaten op als door tabs gescheiden waarden (TSV) met `estimatorSingleQ.ToTSV()` en `estimatorMultiQ.ToTSV()` .

Een volledig C#-hostprogramma dat zowel het gebruik `QuantumSimulator` als `ResourcesEstimator` het formulier maakt, kan dan het volgende doen:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


wat resulteert in uitvoer die vergelijkbaar is met

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a>Q# Jupyter-notebooks
Q# Jupyter-notebooks maken gebruik van de I Q# -kernel, waarmee u callables in één notitie blok kunt definiëren, compileren en uitvoeren Q# ---alle naast instructies, notities en andere inhoud.
Dit betekent dat hoewel het mogelijk is om de inhoud van bestanden te importeren en `*.qs` Q# te gebruiken, ze niet nodig zijn in het uitvoerings model.

Hier wordt beschreven hoe u de Q# hierboven gedefinieerde bewerkingen uitvoert, maar een uitgebreidere inleiding tot het gebruik van Q# Jupyter-notebooks is beschikbaar op [Inleiding tot Q# en Jupyter-notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).

### <a name="defining-operations"></a>Bewerkingen definiëren

In een Q# Jupyter notebook voert u code in op Q# dezelfde manier als in de naam ruimte van een Q# bestand.

Daarom kunnen we toegang tot callables van de [ Q# standaard bibliotheken](xref:microsoft.quantum.qsharplibintro) inschakelen met `open` instructies voor hun respectieve naam ruimten.
Bij het uitvoeren van een cel met een dergelijke instructie zijn de definities van deze naam ruimten beschikbaar in de hele werk ruimte.

> [!NOTE]
> Callables van [micro soft. Quantum. intrinsieke](xref:microsoft.quantum.intrinsic) en [micro soft. Quantum. Canon](xref:microsoft.quantum.canon) (bijvoorbeeld [`H`](xref:microsoft.quantum.intrinsic.h) en [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) zijn automatisch beschikbaar voor bewerkingen die zijn gedefinieerd in cellen in Q# Jupyter-notebooks.
> Dit geldt echter niet voor code die wordt binnengebracht in vanuit externe Q# bron bestanden (een proces dat wordt weer gegeven bij [Inleiding tot Q# en Jupyter-notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)). 
> 

Op dezelfde manier hoeft u alleen maar de Q# code te schrijven en de cel uit te voeren.

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

De uitvoer vermeldt deze bewerkingen, die vervolgens kunnen worden aangeroepen vanuit toekomstige cellen.

### <a name="target-machines"></a>Doelcomputers

De functionaliteit voor het uitvoeren van bewerkingen op specifieke doel computers wordt gegeven via een [ Q# Magic-opdracht](xref:microsoft.quantum.guide.quickref.iqsharp).
`%simulate`Maakt bijvoorbeeld gebruik van de `QuantumSimulator` , en maakt gebruik van `%estimate` `ResourcesEstimator` :

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a>Invoer door geven aan functies en bewerkingen

Als u invoer wilt door geven aan de Q# bewerkingen, kunnen de argumenten worden door gegeven als `key=value` paren aan de Magic-runtime opdracht.
Om uit te voeren `MeasureSuperpositionArray` met vier qubits kunnen we de `%simulate MeasureSuperpositionArray n=4` volgende handelingen uitvoeren:

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

Dit patroon kan worden gebruikt in combi natie met `%estimate` en andere uitvoerings opdrachten.

### <a name="using-no-locq-code-from-other-projects-or-packages"></a>Q#Code uit andere projecten of pakketten gebruiken

Standaard worden in een Q# Jupyter notebook alle `.qs` bestanden in de huidige map geladen en Q# worden de bewerkingen en functies beschikbaar voor gebruik in het notitie blok. De [ `%who` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.who) bevat een lijst met alle momenteel beschik bare Q# bewerkingen en functies.

Als u Q# code uit een andere map wilt laden, kunt u de [ `%project` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.project) gebruiken om een verwijzing naar een `.csproj` bestand voor een project toe te voegen Q# (dat wil zeggen, een project waarnaar wordt verwezen `Microsoft.Quantum.Sdk` ). Met deze opdracht worden alle `.qs` bestanden in de map met de `.csproj` (en submappen) gecompileerd. Ook worden alle pakketten die via of projecten verwijzen waarnaar wordt `PackageReference` Q# verwezen `ProjectReference` in dat bestand, recursief geladen `.csproj` . 

Zo simuleren de volgende cellen een Q# bewerking vanuit een extern project, waarbij naar het pad van het project wordt verwezen ten opzichte van de huidige map:

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

Als u externe pakketten met Q# code wilt laden, gebruikt u de [ `%package` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).
Als u een pakket laadt, worden ook aangepaste Magic-opdrachten beschikbaar of worden coderings Programma's weer gegeven die zijn opgenomen in alle assembly's die deel uitmaken van het pakket.

Als u wilt dat externe pakketten of Q# projecten op notebook intialization keer worden geladen, moet u ervoor zorgen dat de notitieblokmap een `.csproj` bestand bevat waarnaar wordt verwezen `Microsoft.Quantum.Sdk` . Voeg in dat `.csproj` de eigenschap toe `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` aan de `<PropertyGroup>` . Dit geeft een instructie Q# om een of meer items te `ProjectReference` laden `PackageReference` die zijn gevonden in de `.csproj` laad tijd van notebooks.

Dit is bijvoorbeeld een eenvoudig `.csproj` bestand dat ervoor zorgt dat Q# het pakket automatisch wordt geladen `Microsoft.Quantum.Chemistry` :

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> Deze aangepaste `<IQSharpLoadAutomatically>` eigenschap is momenteel vereist Q# voor Jupyter notebook hosts, maar in de toekomst kan dit het standaard gedrag voor een bestand zijn dat `.csproj` zich in dezelfde map bevindt als het notitie blok-bestand.

> [!NOTE]
> Momenteel `<QsharpCompile>` wordt de instelling in de `.csproj` wordt genegeerd door Q# Jupyter notebook-hosts en `.qs` worden alle bestanden in de map `.csproj` (inclusief submappen) geladen en gecompileerd. Ondersteuning voor `.csproj` instellingen wordt in de toekomst verbeterd (Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor meer informatie).
