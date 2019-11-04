---
title: 'Q # technieken-testen en fout opsporing | Microsoft Docs'
description: 'Q # technieken-testen en fout opsporing'
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 25679331f1bed9f98b86c6eb20f511c891bac1af
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183485"
---
# <a name="testing-and-debugging"></a>Testen en fout opsporing

Net als bij het klassieke Program meren is het essentieel om te controleren of Quantum Program ma's functioneren zoals bedoeld en om te kunnen vaststellen of een Quantum programma onjuist is.
In deze sectie hebben we de hulp middelen die worden aangeboden door Q # voor het testen en opsporen van fouten in Quantum Program ma's.

## <a name="unit-tests"></a>Eenheids tests

Een veelvoorkomende aanpak voor het testen van klassieke Program ma's is het schrijven van kleine Program ma's, de naam *eenheid testen* , die code uitvoeren in een bibliotheek en de uitvoer vergelijkt met een verwachte uitvoer.
We willen er bijvoorbeeld voor zorgen dat `Square(2)` `4`retourneert, omdat we *een priori* weten dat $2 ^ 2 = $4.

Q # ondersteunt het maken van eenheids tests voor Quantum-Program ma's en die kunnen worden uitgevoerd als tests in het Framework van de [xUnit](https://xunit.github.io/) -analyse-eenheid.

### <a name="creating-a-test-project"></a>Een test project maken

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Open Visual Studio 2019. Ga naar het menu `File` en selecteer `New` > `Project...`.
Selecteer in de project-sjabloon Verkenner onder `Installed` > `Visual C#`de sjabloon `Q# Test Project`.

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Opdracht regel/Visual Studio code](#tab/tabid-vscode)

Voer vanuit uw favoriete opdracht regel de volgende opdracht uit:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

In beide gevallen heeft het nieuwe project twee bestanden geopend.
Het eerste bestand, `Tests.qs`, biedt een handige plaats om nieuwe Q #-eenheids tests te definiëren.
In eerste instantie bevat dit bestand een test voor een voorbeeld eenheid `AllocateQubitTest` die controleert of een nieuw toegewezen Qubit zich in de $ \ket{0}$ status bevindt en een bericht afdrukt:

```qsharp
    operation AllocateQubitTest () : Unit {
        using (q = Qubit()) {
            Assert([PauliZ], [q], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

Een Q #-bewerking die compatibel is met het type `(Unit => Unit)` of functie die compatibel is met `(Unit -> Unit)` kan worden uitgevoerd als een eenheids test. 

Het tweede bestand `TestSuiteRunner.cs` bevat een methode die Q #-eenheids tests detecteert en uitvoert. Dit is de methode `TestTarget` voorzien van een `OperationDriver` kenmerk.
Het kenmerk `OperationDriver` maakt deel uit van de xUnit extension library micro soft. Quantum. simulatie. xUnit.
Het Framework voor het testen van de eenheid roept `TestTarget` methode voor elke Q #-eenheids test op.
In het raam werk wordt de beschrijving van de eenheids test door gegeven aan de methode via `op` argument. De volgende regel code:
```csharp
op.TestOperationRunner(sim);
```
Hiermee wordt de eenheids test uitgevoerd op `QuantumSimulator`.

Het test detectie mechanisme van de eenheid zoekt standaard naar alle Q #-functies of-bewerkingen van compatibele typen die voldoen aan de volgende eigenschappen:
* Deze bevindt zich in dezelfde assembly als de methode die is gekoppeld aan het kenmerk `OperationDriver`.
* Bevindt zich in dezelfde naam ruimte als de methode die is gekoppeld aan het kenmerk `OperationDriver`.
* Heeft een naam die eindigt op `Test`.

Een assembly, een naam ruimte en een achtervoegsel voor de functies en bewerkingen voor de eenheids test kunnen worden ingesteld met behulp van optionele para meters van het kenmerk `OperationDriver`:
* `AssemblyName` para meter wordt de naam van de assembly ingesteld waarnaar wordt gezocht op tests.
* `TestNamespace` para meter wordt de naam van de naam ruimte die wordt doorzocht op tests ingesteld.
* `Suffix` stelt het achtervoegsel in van de bewerkings-of functie namen die als eenheids testen worden beschouwd.

Daarnaast kunt u met de optionele para meter `TestCasePrefix` een voor voegsel instellen voor de naam van de test case. Het voor voegsel voor de naam van de bewerking wordt weer gegeven in de lijst met test cases. `TestCasePrefix = "QSim:"` zal er bijvoorbeeld voor zorgen dat `AllocateQubitTest` als `QSim:AllocateQubitTest` worden weer gegeven in de lijst met gevonden tests. Dit kan handig zijn om te bepalen welke Simulator wordt gebruikt om een test uit te voeren.

### <a name="running-q-unit-tests"></a>Er worden Q #-eenheids tests uitgevoerd

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Als eenmalige installatie per oplossing, gaat u naar `Test` menu en selecteert u `Test Settings` > `Default Processor Architecture` > `X64`.

> [!TIP]
> De standaard instelling voor de architectuur van de processor voor Visual Studio wordt opgeslagen in het bestand met oplossings opties (`.suo`) voor elke oplossing.
> Als u dit bestand verwijdert, moet u opnieuw `X64` selecteren als uw processor architectuur.

Bouw het project, ga naar het menu `Test` en selecteer `Windows` > `Test Explorer`. `AllocateQubitTest` wordt weer gegeven in de lijst met tests in de `Not Run Tests` groep. Selecteer `Run All` of voer deze afzonderlijke test uit en probeer het opnieuw.

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Opdracht regel/Visual Studio code](#tab/tabid-vscode)

Als u tests wilt uitvoeren, gaat u naar de projectmap (de map die `Tests.csproj`bevat) en voert u de volgende opdracht uit:

```bash
$ dotnet restore
$ dotnet test
```

U ziet dat de uitvoer er ongeveer als volgt uitziet:

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

***

## <a name="logging-and-assertions"></a>Logboek registratie en bevestigingen

Een belang rijk gevolg van het feit dat functies in Q # geen neven effecten hebben, is dat alle gevolgen van het uitvoeren van een functie waarvan het uitvoer type de lege tuple `()`, nooit in acht kunnen worden genomen vanuit een Q #-programma.
Dat wil zeggen dat een doel computer ervoor kiest geen functie uit te voeren die `()` retourneert met de garantie dat dit weglatings gedrag van de volgende Q #-code niet wordt gewijzigd.
Hiermee kunnen functies `()` een nuttig hulp programma voor het insluiten van beweringen en fout opsporing in Q #-Program ma's worden geretourneerd. 

### <a name="logging"></a>Logboekregistratie

De intrinsieke functie <xref:microsoft.quantum.intrinsic.message> is van het type `(String -> Unit)` en maakt het mogelijk diagnostische berichten te maken.

De `onLog` actie van `QuantumSimulator` kan worden gebruikt om acties te definiëren die worden uitgevoerd wanneer Q #-code aanroepen `Message`. Standaard worden logboek berichten afgedrukt op standaard uitvoer.

Bij het definiëren van een eenheids test suite kunnen de geregistreerde berichten worden omgeleid naar de test uitvoer. Wanneer een project wordt gemaakt op basis van Q # test project sjabloon, wordt deze omleiding vooraf geconfigureerd voor de suite en als volgt gemaakt:

```qsharp
using (var sim = new QuantumSimulator())
{
    // OnLog defines action(s) performed when Q# test calls operation Message
    sim.OnLog += (msg) => { output.WriteLine(msg); };
    op.TestOperationRunner(sim);
}
```

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nadat u een test in test Explorer hebt uitgevoerd en op de test hebt geklikt, wordt er een paneel weer gegeven met informatie over de test uitvoering: geslaagd/mislukt status, verstreken tijd en de koppeling uitvoer. Als u op de koppeling uitvoer klikt, wordt de test uitvoer in een nieuw venster geopend.

![test uitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Opdracht regel/Visual Studio code](#tab/tabid-vscode)

De status pass/fail voor elke test wordt op de-console afgedrukt door `dotnet test`.
Voor mislukte tests worden de uitvoer die is geregistreerd als resultaat van de `output.WriteLine(msg)` bovenstaande aanroep ook naar de console afgedrukt om de fout te kunnen vaststellen.

***

### <a name="assertions"></a>Asserties

Dezelfde logica kan worden toegepast voor het implementeren van bevestigingen. Laten we eens een eenvoudig voor beeld bekijken:

```qsharp
function AssertPositive(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

Hier geeft het tref woord `fail` aan dat de berekening niet moet worden voortgezet, waardoor er een uitzonde ring wordt gegenereerd op de doel computer waarop het Q #-programma wordt uitgevoerd.
Een fout in deze soort kan per definitie niet worden waargenomen, omdat er geen verdere Q #-code wordt uitgevoerd nadat een `fail`-instructie is bereikt.
Daarom kunnen we er zeker van zijn dat de invoer van het `AssertPositive`positief is.

Op basis van deze ideeën biedt [de prelude](xref:microsoft.quantum.libraries.standard.prelude) twee nuttige beweringen, <xref:microsoft.quantum.intrinsic.assert> en <xref:microsoft.quantum.intrinsic.assertprob> beide gemodelleerd als bewerkingen op `()`. Deze beweringen maken elk deel uit van een Pauli-operator die een bepaalde waardering van belang beschrijft, een Quantum registratie waarop een meting moet worden uitgevoerd en een hypothetisch resultaat.
Op doel computers die door simulatie werken, zijn we niet gebonden aan [het niet-klonen van theorema](https://en.wikipedia.org/wiki/No-cloning_theorem)en kunnen deze metingen worden uitgevoerd zonder dat de registratie wordt verstoord die aan dergelijke verklaringen wordt door gegeven.
Een Simulator kan vervolgens, vergelijkbaar met de bovenstaande `AssertPositive` functie, de berekening afbreken als de hypothetische uitkomst niet in de praktijk wordt waargenomen:

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

In fysieke Quantum hardware, waarbij het niet-klonen van theorema het onderzoek van de Quantum status voor komt, worden de `Assert`-en `AssertProb`-bewerkingen gewoon `()` zonder ander effect weer gegeven.

De <xref:microsoft.quantum.diagnostics>-naam ruimte biedt een aantal meer functies van de `Assert`-familie waarmee we meer geavanceerde voor waarden kunnen controleren. 

## <a name="dump-functions"></a>Dump functies

Voor het oplossen van problemen met Quantum Program ma's biedt de <xref:microsoft.quantum.diagnostics> naam ruimte twee functies die in een bestand kunnen dumpen van de huidige status van de doel computer: <xref:microsoft.quantum.diagnostics.dumpmachine> en <xref:microsoft.quantum.diagnostics.dumpregister>. De gegenereerde uitvoer van beide is afhankelijk van de doel computer.

### <a name="dumpmachine"></a>DumpMachine

De Full-State Quantum Simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [functie Wave](https://en.wikipedia.org/wiki/Wave_function) van het hele Quantum systeem, als een eendimensionale matrix van complexe getallen, waarbij elk element de amplitude van de de waarschijnlijkheid van het meten van de berekenings basis status $ \ket{n} $, waarbij $ \ket{n} = \ket{b_{n-1}... b_1b_0} $ voor bits $\{b_i\}$. Bijvoorbeeld op een machine met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10}, \end{align} $ $ aanroepen <xref:microsoft.quantum.diagnostics.dumpmachine> deze uitvoer genereert :

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

De eerste rij bevat een opmerking met de Id's van de bijbehorende qubits in hun significante volg orde.
De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{n} $ in zowel Cartesisch als polaire indeling. Gedetailleerd voor de eerste rij:

* **`∣0❭:`** deze rij overeenkomt met de status van de `0` berekening
* **`0.707107 +  0.000000 i`** : de waarschijnlijke amplitude in Cartesisch formaat.
* **` == `** : in het `equal`-teken worden beide equivalente verklaringen gescheiden.
* **`**********  `** : een grafische weer gave van de omvang, het aantal `*` is evenredig met de waarschijnlijkheid van het meten van deze status vector.
* **`[ 0.500000 ]`** : de numerieke waarde van de grootte
* **`    ---`** : een grafische weer gave van de amplitude fase (zie hieronder).
* **`[ 0.0000 rad ]`** : de numerieke waarde van de fase (in radialen).

Zowel de grootte als de fase worden weer gegeven met een grafische weer gave. De weer gave met de grootte is direct vooruit: er wordt een balk van `*`weer gegeven, hoe groter de kans dat de balk groter is. Voor de fase worden de volgende symbolen weer gegeven die de hoek aangeven op basis van bereiken:

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

In de volgende voor beelden ziet u `DumpMachine` voor een aantal algemene statussen:

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > De id van een Qubit wordt tijdens runtime toegewezen en is niet noodzakelijkerwijs uitgelijnd met de volg orde waarin de Qubit is toegewezen of hun positie binnen een Qubit-REGI ster.


#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > U kunt een Qubit-id in Visual Studio uitzoeken door een onderbrekings punt in uw code te plaatsen en de waarde van een Qubit-variabele te controleren, bijvoorbeeld:
  > 
  > ![Qubit-id weer geven in Visual Studio](~/media/qubit_id.png)
  >
  > de Qubit met index `0` op `register2` heeft id =`3`. de Qubit met index `1` heeft id =`2`.

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Opdracht regel/Visual Studio code](#tab/tabid-vscode)

  > [!TIP]
  > U kunt een Qubit-id berekenen met behulp van de functie <xref:microsoft.quantum.intrinsic.message> en de variabele Qubit in het bericht door geven, bijvoorbeeld:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > Dit kan deze uitvoer genereren:
  >```
  > 0=q:3; 1=q:2
  >```
  > Dit betekent dat de Qubit met index `0` op `register2` een id =`3`heeft, de Qubit met index `1` een id =`2`heeft.


***

<xref:microsoft.quantum.diagnostics.dumpmachine> maakt deel uit van de <xref:microsoft.quantum.diagnostics> naam ruimte, dus als u deze wilt gebruiken, moet u een `open`-instructie toevoegen:

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a>DumpRegister

<xref:microsoft.quantum.diagnostics.dumpregister> werkt als <xref:microsoft.quantum.diagnostics.dumpmachine>, maar er wordt ook een matrix van qubits gebruikt om de hoeveelheid gegevens te beperken tot alleen die relevant voor de bijbehorende qubits.

Net als bij <xref:microsoft.quantum.diagnostics.dumpmachine>is de informatie die door <xref:microsoft.quantum.diagnostics.dumpregister> wordt gegenereerd, afhankelijk van de doel computer. Voor de volle Quantum Simulator schrijft het naar het bestand met de functie Wave tot een globale fase van het Quantum subsysteem dat wordt gegenereerd door de geleverde qubits in dezelfde indeling als <xref:microsoft.quantum.diagnostics.dumpmachine>.  Neem bijvoorbeeld opnieuw een machine met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10} =-e ^ {-i \ Pi/4} ((\frac{1}{\sqrt{2}} \ Ket{0}-\frac{(1 + i)}{2} \ket{1}) \otimes \frac{-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ die <xref:microsoft.quantum.diagnostics.dumpregister> aanroept voor `qubit[0]`, wordt deze uitvoer gegenereerd:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

en het aanroepen van <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[1]` genereert deze uitvoer:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Over het algemeen is de status van een REGI ster dat Entangled met een ander REGI ster een gemengde status in plaats van een zuivere status. In dit geval wordt <xref:microsoft.quantum.diagnostics.dumpregister> het volgende bericht uitgevoerd:

```
Qubits provided (0;) are entangled with some other qubit.
```

In het volgende voor beeld ziet u hoe u zowel <xref:microsoft.quantum.diagnostics.dumpregister> als <xref:microsoft.quantum.diagnostics.dumpmachine> kunt gebruiken in uw Q #-code:

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a>Foutopsporing

Op de `Assert`-en `Dump` functies en-bewerkingen ondersteunt Q # een subset van de standaard mogelijkheden voor Visual Studio-fout opsporing: [regel onderbrekingen instellen](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), de [code door lopen met behulp van F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) en [waarden van klassieke variabelen controleren ](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows)zijn allemaal mogelijk tijdens het uitvoeren van code in de Simulator.

Fout opsporing in Visual Studio code wordt nog niet ondersteund.

