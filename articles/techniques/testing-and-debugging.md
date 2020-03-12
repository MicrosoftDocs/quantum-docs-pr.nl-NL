---
title: "Q #-Program ma's testen en fouten opsporen"
description: Meer informatie over het gebruik van eenheids testen, feiten en beweringen en dump functies om Quantum-Program ma's te testen en fout opsporing uit te voeren.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 8131c2ec9320b5075c37370e12ad39a4df5bd3d5
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022848"
---
# <a name="testing-and-debugging"></a>Testen en fout opsporing

Net als bij het klassieke Program meren is het essentieel om te controleren of Quantum Program ma's functioneren zoals bedoeld en om te kunnen vaststellen of een Quantum programma onjuist is.
In deze sectie hebben we de hulp middelen die worden aangeboden door Q # voor het testen en opsporen van fouten in Quantum Program ma's.

## <a name="unit-tests"></a>Eenheids tests

Een veelvoorkomende aanpak voor het testen van klassieke Program ma's is het schrijven van kleine Program ma's, de naam *eenheid testen* , die code uitvoeren in een bibliotheek en de uitvoer vergelijkt met een verwachte uitvoer.
We willen er bijvoorbeeld voor zorgen dat `Square(2)` `4`retourneert, omdat we *een priori* weten dat $2 ^ 2 = $4.

Q # ondersteunt het maken van eenheids tests voor Quantum-Program ma's en die kunnen worden uitgevoerd als tests in het Framework van de [xUnit](https://xunit.github.io/) -analyse-eenheid.

### <a name="creating-a-test-project"></a>Een test project maken

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Open Visual Studio 2019. Ga naar het menu `File` en selecteer `New` > `Project...`.
Zoek in de rechter bovenhoek naar `Q#`en selecteer de sjabloon `Q# Test Project`.

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

Voer vanuit uw favoriete opdracht regel de volgende opdracht uit:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Het nieuwe project heeft één bestand `Tests.qs`, dat een handige plaats biedt om nieuwe Q #-eenheids tests te definiëren.
In eerste instantie bevat dit bestand een test voor een voorbeeld eenheid `AllocateQubit` die controleert of een nieuw toegewezen Qubit zich in de $ \ket{0}$ status bevindt en een bericht afdrukt:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

: Nieuw: elke Q #-bewerking of-functie die een argument van het type `Unit` gebruikt en retourneert `Unit` als een eenheids test kan worden gemarkeerd via het `@Test("...")` kenmerk. Het argument voor dat kenmerk, `"QuantumSimulator"` hierboven, geeft het doel aan waarop de test wordt uitgevoerd. Eén test kan op meerdere doelen worden uitgevoerd. Voeg bijvoorbeeld een kenmerk `@Test("ResourcesEstimator")` toe boven `AllocateQubit`. 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Sla het bestand op en voer alle tests uit. Er moeten nu twee eenheids tests worden uitgevoerd, één waarbij AllocateQubit op de QuantumSimulator-server wordt verwerkt en een waar deze wordt uitgevoerd in de ResourceEstimator. 

De Q #-compiler herkent de ingebouwde doelen "QuantumSimulator", "ToffoliSimulator" en "ResourcesEstimator" als geldige uitvoerings doelen voor eenheids testen. Het is ook mogelijk om een volledig gekwalificeerde naam op te geven voor het definiëren van een aangepast uitvoerings doel. 

### <a name="running-q-unit-tests"></a>Er worden Q #-eenheids tests uitgevoerd

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Als eenmalige installatie per oplossing, gaat u naar `Test` menu en selecteert u `Test Settings` > `Default Processor Architecture` > `X64`.

> [!TIP]
> De standaard instelling voor de architectuur van de processor voor Visual Studio wordt opgeslagen in het bestand met oplossings opties (`.suo`) voor elke oplossing.
> Als u dit bestand verwijdert, moet u opnieuw `X64` selecteren als uw processor architectuur.

Bouw het project, ga naar het menu `Test` en selecteer `Windows` > `Test Explorer`. `AllocateQubit` wordt weer gegeven in de lijst met tests in de `Not Run Tests` groep. Selecteer `Run All` of voer deze afzonderlijke test uit en probeer het opnieuw.

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

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

Eenheids tests kunnen worden gefilterd op basis van hun naam en/of het uitvoerings doel:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

De intrinsieke functie <xref:microsoft.quantum.intrinsic.message> is van het type `(String -> Unit)` en maakt het mogelijk diagnostische berichten te maken.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nadat u een test in test Explorer hebt uitgevoerd en op de test hebt geklikt, wordt er een paneel weer gegeven met informatie over de test uitvoering: geslaagd/mislukt status, verstreken tijd en de koppeling uitvoer. Als u op de koppeling uitvoer klikt, wordt de test uitvoer in een nieuw venster geopend.

![test uitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

De status pass/fail voor elke test wordt op de-console afgedrukt door `dotnet test`.
Voor mislukte tests worden ook de uitvoer naar de console afgedrukt om de fout te kunnen vaststellen.

***

## <a name="facts-and-assertions"></a>Feiten en verklaringen

Omdat functies in Q # geen _logische_ neven effecten hebben, kunnen _andere soorten_ effecten van het uitvoeren van een functie waarvan het uitvoer type de lege tuple `()`, nooit worden waargenomen vanuit een Q #-programma.
Dat wil zeggen dat een doel computer ervoor kiest geen functie uit te voeren die `()` retourneert met de garantie dat dit weglatings gedrag van de volgende Q #-code niet wordt gewijzigd.
Zo kunnen functies die `()` retour neren (dat wil zeggen `Unit`) een nuttig hulp middel voor het insluiten van beweringen en fout opsporing in Q #-Program ma's. 

Laten we eens een eenvoudig voor beeld bekijken:

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

Hier geeft het tref woord `fail` aan dat de berekening niet moet worden voortgezet, waardoor er een uitzonde ring wordt gegenereerd op de doel computer waarop het Q #-programma wordt uitgevoerd.
Een fout in deze soort kan per definitie niet worden waargenomen, omdat er geen verdere Q #-code wordt uitgevoerd nadat een `fail`-instructie is bereikt.
Daarom kunnen we er zeker van zijn dat de invoer van het `PositivityFact`positief is.

Houd er rekening mee dat we hetzelfde gedrag kunnen implementeren als `PositivityFact` met behulp van de [`Fact`](xref:microsoft.quantum.diagnostics.fact) -functie van de <xref:microsoft.quantum.diagnostics> naam ruimte:

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

*Beweringen*, daarentegen, worden op dezelfde manier gebruikt als feiten, maar kunnen afhankelijk zijn van de status van de doel computer. Ze worden dienovereenkomstig gedefinieerd als bewerkingen, terwijl feiten worden gedefinieerd als functies (zoals hierboven).
Voor een beter begrip van het onderscheid moet u rekening houden met het volgende gebruik van een feit binnen een bewering:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Hier gebruiken we de bewerking <xref:microsoft.quantum.environment.getqubitsavailabletouse> om het aantal beschik bare qubits te retour neren dat kan worden gebruikt.
Zoals dit duidelijk is afhankelijk van de algemene status van het programma en de uitvoerings omgeving, moet onze definitie van `AssertQubitsAreAvailable` ook een bewerking zijn.
We kunnen die globale status echter gebruiken om een eenvoudige `Bool` waarde te leveren als invoer voor de `Fact` functie.

Op basis van deze ideeën biedt [de prelude](xref:microsoft.quantum.libraries.standard.prelude) twee nuttige beweringen, <xref:microsoft.quantum.intrinsic.assert> en <xref:microsoft.quantum.intrinsic.assertprob> beide gemodelleerd als bewerkingen op `()`. Deze beweringen maken elk deel uit van een Pauli-operator die een bepaalde waardering van belang beschrijft, een Quantum registratie waarop een meting moet worden uitgevoerd en een hypothetisch resultaat.
Op doel computers die door simulatie werken, zijn we niet gebonden aan [het niet-klonen van theorema](https://en.wikipedia.org/wiki/No-cloning_theorem)en kunnen deze metingen worden uitgevoerd zonder dat de registratie wordt verstoord die aan dergelijke verklaringen wordt door gegeven.
Een Simulator kan vervolgens, vergelijkbaar met de bovenstaande `PositivityFact` functie, de berekening afbreken als de hypothetische uitkomst niet in de praktijk wordt waargenomen:

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

De Full-State Quantum Simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [functie Wave](https://en.wikipedia.org/wiki/Wave_function) van het hele Quantum systeem, als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitude vormt van de kans op het meten van de berekenings basis status $ \ket{n} $, waarbij $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ voor bits $\{b_i\}$. Bijvoorbeeld op een machine met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10}, \end{align} $ $ aanroepen <xref:microsoft.quantum.diagnostics.dumpmachine> genereert deze uitvoer:

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


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > U kunt een Qubit-id in Visual Studio uitzoeken door een onderbrekings punt in uw code te plaatsen en de waarde van een Qubit-variabele te controleren, bijvoorbeeld:
  > 
  > ![Qubit-id weer geven in Visual Studio](~/media/qubit_id.png)
  >
  > de Qubit met index `0` op `register2` heeft id =`3`. de Qubit met index `1` heeft id =`2`.

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

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

Net als bij <xref:microsoft.quantum.diagnostics.dumpmachine>is de informatie die door <xref:microsoft.quantum.diagnostics.dumpregister> wordt gegenereerd, afhankelijk van de doel computer. Voor de volle Quantum Simulator schrijft het naar het bestand met de functie Wave tot een globale fase van het Quantum subsysteem dat wordt gegenereerd door de geleverde qubits in dezelfde indeling als <xref:microsoft.quantum.diagnostics.dumpmachine>.  Neem bijvoorbeeld opnieuw een machine met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10} =-e ^ {-i \ Pi/4} ((\frac{1}{\sqrt{2}} \ket{0}-\frac{(1 + i)}{2} \ket{1}) \otimes \frac{-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ aanroepende <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[0]` deze uitvoer genereert :

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

Op de `Assert`-en `Dump` functies en-bewerkingen ondersteunt Q # een subset van de standaard mogelijkheden voor Visual Studio-fout opsporing: [regel onderbrekingen instellen](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [door code te bladeren met behulp van F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) en de [waarden van klassieke variabelen te controleren](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) , zijn allemaal mogelijk tijdens het uitvoeren van code in de Simulator.

Fout opsporing in Visual Studio code maakt gebruik van de mogelijkheden voor fout C# opsporing van de Visual Studio code-extensie die wordt ondersteund door OmniSharp en vereist de installatie van de [nieuwste versie](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp). 
