---
title: Testen en foutopsporing
description: Meer informatie over het gebruik van eenheids testen, feiten en beweringen en dump functies om Quantum-Program ma's te testen en fout opsporing uit te voeren.
author: tcNickolas
ms.author: mamykhai
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5505086c5efac89f6940cde1ecae2ce629cfeda5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690965"
---
# <a name="testing-and-debugging"></a>Testen en foutopsporing

Net als bij klassiek Program meren is het essentieel om te controleren of Quantum-Program ma's functioneren zoals bedoeld en om te kunnen vaststellen of het probleem onjuist is.
In deze sectie hebben we de hulp middelen die worden aangeboden Q# voor het testen en opsporen van fouten in Quantum Program ma's.

## <a name="unit-tests"></a>Eenheids tests

Een gemeen schappelijke aanpak voor het testen van klassieke Program ma's is het schrijven van kleine Program ma's met de naam *unit-tests* , waarmee code wordt uitgevoerd in een bibliotheek en de uitvoer ervan wordt vergeleken met een verwachte uitvoer.
U kunt er bijvoorbeeld voor zorgen dat er `Square(2)` wordt geretourneerd, `4` omdat u *een priori* weet dat $2 ^ 2 = $4.

Q# biedt ondersteuning voor het maken van eenheids tests voor Quantum-Program ma's en die als tests kunnen worden uitgevoerd binnen het test raamwerk van de [xUnit](https://xunit.github.io/) -eenheid.

### <a name="creating-a-test-project"></a>Een test project maken

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Open Visual Studio 2019. Ga naar het menu **bestand** en selecteer **Nieuw > project...** . Zoek in de rechter bovenhoek `Q#` de **Q# test project** sjabloon en selecteer deze.

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

Voer vanuit uw favoriete opdracht regel de volgende opdracht uit:
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Het nieuwe project heeft één bestand `Tests.qs` , dat een handige plaats biedt om nieuwe Q# eenheids tests te definiëren.
In eerste instantie bevat dit bestand één sample-eenheids test `AllocateQubit` waarmee wordt gecontroleerd of een nieuw toegewezen Qubit zich in de status $ \ket $ bevindt {0} en een bericht afdrukt:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

Elke Q# bewerking of functie die een argument van het type `Unit` en retourneert, `Unit` kan worden gemarkeerd als een eenheids test via het `@Test("...")` kenmerk. In het vorige voor beeld, het argument voor dat kenmerk, `"QuantumSimulator"` geeft het doel aan waarop de test wordt uitgevoerd. Eén test kan op meerdere doelen worden uitgevoerd. Voeg bijvoorbeeld eerst een kenmerk toe `@Test("ResourcesEstimator")` `AllocateQubit` . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Sla het bestand op en voer alle tests uit. Er moeten nu twee eenheids tests zijn, één waarbij `AllocateQubit` wordt uitgevoerd op de `QuantumSimulator` en een waar deze wordt uitgevoerd in de `ResourcesEstimator` . 

De Q# compiler herkent de ingebouwde doelen `"QuantumSimulator"` , `"ToffoliSimulator"` en `"ResourcesEstimator"` als geldige uitvoerings doelen voor eenheids testen. Het is ook mogelijk om een volledig gekwalificeerde naam op te geven voor het definiëren van een aangepast uitvoerings doel. 

### <a name="running-no-locq-unit-tests"></a>Actieve Q# eenheids tests

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Als eenmalige installatie per oplossing, gaat u naar het menu **test** en selecteert u **instellingen testen > standaard processor architectuur > x64** .

> [!TIP]
> De standaard instelling voor de architectuur van de processor voor Visual Studio wordt opgeslagen in het bestand met oplossings opties ( `.suo` ) voor elke oplossing.
> Als u dit bestand verwijdert, moet u opnieuw **x64** selecteren als uw processor architectuur.

Bouw het project, open het menu **test** en selecteer **Windows > test Verkenner** . **AllocateQubit** wordt weer gegeven in de lijst met tests in de groep **niet-uitgevoerde tests** . Selecteer **alles uitvoeren** of voer deze afzonderlijke test uit.

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

Als u tests wilt uitvoeren, gaat u naar de projectmap (de map die bevat `Tests.csproj` ) en voert u de volgende opdracht uit:

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

Eenheids tests kunnen worden gefilterd op basis van de naam of het uitvoerings doel:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


**_

De intrinsieke functie <xref:Microsoft.Quantum.Intrinsic.Message> heeft type `(String -> Unit)` en maakt het mogelijk diagnostische berichten te maken.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nadat u een test in test Explorer hebt uitgevoerd en op de test hebt geklikt, wordt een deel venster weer gegeven met informatie over de test uitvoering: status van geslaagd/mislukt, verstreken tijd en een koppeling naar de uitvoer. Klik op _ *uitvoer* * om de test uitvoer in een nieuw venster te openen.

![test uitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

De status pass/fail voor elke test wordt door gegeven aan de console `dotnet test` .
Voor mislukte tests worden ook de uitvoer naar de console afgedrukt om de fout te kunnen vaststellen.

**_

## <a name="facts-and-assertions"></a>Feiten en verklaringen

Omdat functies in Q# geen _logische_ neven effecten hebben, kunt u nooit nagaan, vanuit een Q# programma, andere soorten effecten van het uitvoeren van een functie waarvan het uitvoer type de lege tuple is `()` .
Dat wil zeggen dat een doel computer ervoor kiest geen functie uit te voeren die wordt geretourneerd `()` met de garantie dat dit weglatings gedrag van de volgende code niet wordt gewijzigd Q# .
Dit gedrag zorgt ervoor dat functies die worden geretourneerd `()` (zoals `Unit` ) een handig hulp middel voor het insluiten van beweringen en het opsporen van fouten in Q# Program ma's. 

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

Hier geeft het sleutel woord `fail` aan dat de berekening niet moet worden voortgezet en wordt er een uitzonde ring gegenereerd op de doel computer waarop het programma wordt uitgevoerd Q# .
Op basis van de definitie kan een fout van dit soort niet worden waargenomen Q# , omdat de doel computer de code niet langer uitvoert Q# nadat een `fail` instructie is bereikt.
Daarom `PositivityFact` kunnen we er zeker van zijn dat de invoer van de gegevens positief is.

Houd er rekening mee dat we hetzelfde gedrag kunnen implementeren als `PositivityFact` het gebruik [`Fact`](xref:Microsoft.Quantum.Diagnostics.fact) van de functie uit de <xref:Microsoft.Quantum.Diagnostics> naam ruimte:

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

_Assertions * worden daarentegen op dezelfde manier gebruikt als voor waarden, maar dit kan afhankelijk zijn van de status van de doel computer. Ze worden dienovereenkomstig gedefinieerd als bewerkingen, terwijl feiten worden gedefinieerd als functies (zoals in het vorige voor beeld).
Voor een beter begrip van het onderscheid moet u rekening houden met het volgende gebruik van een feit binnen een bewering:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Hier gebruiken we de bewerking <xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse> voor het retour neren van het aantal beschik bare qubits dat kan worden gebruikt.
Zoals dit afhankelijk is van de algemene status van het programma en de uitvoerings omgeving, moet de definitie van `AssertQubitsAreAvailable` ook een bewerking zijn.
We kunnen die globale status echter gebruiken om een eenvoudige `Bool` waarde te leveren als invoer voor de `Fact` functie.

[De prelude](xref:microsoft.quantum.libraries.standard.prelude), die voortbouwt op deze ideeën, biedt twee bijzonder nuttige verklaringen <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> en <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> beide gemodelleerd als bewerkingen op `()` . Deze beweringen maken elk deel uit van een Pauli-operator die een bepaalde meet waarde beschrijft, een Quantum registratie waarop een meting wordt uitgevoerd en een hypothetisch resultaat.
Doel computers die door simulatie werken, zijn niet gebonden aan [het niet-klonen theorema](https://en.wikipedia.org/wiki/No-cloning_theorem)en kunnen dergelijke metingen uitvoeren zonder de kassa te verstoren die aan dergelijke bevestigingen wordt door gegeven.
Een Simulator kan vervolgens, net als bij de `PositivityFact` vorige functie, de berekening stoppen als het hypothetische resultaat in de praktijk niet wordt waargenomen:

```qsharp
using (register = Qubit()) 
{
    H(register);
    AssertMeasurement([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

In fysieke Quantum-hardware, waarbij het niet-klonen van theorema het onderzoek van een Quantum status voor komt, worden de `AssertMeasurement` en- `AssertMeasurementProbability` bewerkingen gewoon `()` zonder ander effect geretourneerd.

De <xref:Microsoft.Quantum.Diagnostics> naam ruimte bevat verschillende meer functies van de `Assert` familie, waarmee u meer geavanceerde voor waarden kunt controleren. 

## <a name="dump-functions"></a>Dump functies

Voor het oplossen van problemen met Quantum Program ma's <xref:Microsoft.Quantum.Diagnostics> biedt de naam ruimte twee functies die in een bestand de huidige status van de doel computer kunnen dumpen: <xref:Microsoft.Quantum.Diagnostics.DumpMachine> en <xref:Microsoft.Quantum.Diagnostics.DumpRegister> . De gegenereerde uitvoer van beide is afhankelijk van de doel computer.

### <a name="dumpmachine"></a>DumpMachine

De Full-State Quantum Simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [functie Wave](https://en.wikipedia.org/wiki/Wave_function) van het hele Quantum systeem, als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitude vormt van de kans op het meten van de berekenings basis status $ \ket{n} $, waarbij $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ voor bits $ \{ b_i \} $. Bijvoorbeeld, op een computer met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} , \end{align} $ $ aanroepen, wordt <xref:Microsoft.Quantum.Diagnostics.DumpMachine> deze uitvoer gegenereerd:

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

De eerste rij bevat een opmerking met de id's van de bijbehorende qubits in hun significante volg orde.
De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{n} $ in zowel Cartesisch als polaire indeling. Gedetailleerd voor de eerste rij:

* **`∣0❭:`** deze rij komt overeen met de status van de `0` reken kundige basis
* **`0.707107 +  0.000000 i`** : de waarschijnlijke amplitude in Cartesisch formaat.
* **` == `** : het `equal` teken scheidt beide equivalente verklaringen.
* **`**********  `** : Een grafische weer gave van de omvang, het aantal `*` is evenredig met de kans dat deze status vector wordt gemeten.
* **`[ 0.500000 ]`** : de numerieke waarde van de grootte
* **`    ---`** : Een grafische weer gave van de fase van de amplitude (Zie de volgende uitvoer).
* **`[ 0.0000 rad ]`** : de numerieke waarde van de fase (in radialen).

Zowel de grootte als de fase worden weer gegeven met een grafische weer gave. De weer gave met de grootte is direct vooruit: er wordt een balk van weer gegeven `*` , hoe groter de kans dat de balk groter wordt. Voor de fase worden de volgende symbolen weer gegeven die de hoek aangeven op basis van bereiken:

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

In de volgende voor beelden ziet u `DumpMachine` een aantal algemene statussen:

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
  > U kunt een Qubit-id in Visual Studio vinden door een onderbrekings punt in uw code te plaatsen en de waarde van een Qubit-variabele te controleren, bijvoorbeeld:
  > 
  > ![Qubit-id weer geven in Visual Studio](~/media/qubit_id.png)
  >
  > de Qubit met index `0` op `register2` heeft id = `3` , de Qubit met index `1` heeft id = `2` .

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > U kunt een Qubit-id vinden door de <xref:Microsoft.Quantum.Intrinsic.Message> functie te gebruiken en de variabele Qubit in het bericht door te geven, bijvoorbeeld:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > Dit kan deze uitvoer genereren:
  >```
  > 0=q:3; 1=q:2
  >```
  > Dit betekent dat de Qubit met index `0` op `register2` heeft id = `3` , de Qubit met index `1` heeft id = `2` .


**_

Aangezien <xref:Microsoft.Quantum.Diagnostics.DumpMachine> u een deel van de  <xref:Microsoft.Quantum.Diagnostics> naam ruimte hebt, moet u een `open` instructie toevoegen om deze te openen:

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

<xref:Microsoft.Quantum.Diagnostics.DumpRegister> werkt als <xref:Microsoft.Quantum.Diagnostics.DumpMachine> , behalve dat er ook een matrix met qubits wordt gebruikt om de hoeveelheid gegevens te beperken tot alleen die relevant voor de bijbehorende qubits.

Net als bij is <xref:Microsoft.Quantum.Diagnostics.DumpMachine> de informatie die door wordt gegenereerd, <xref:Microsoft.Quantum.Diagnostics.DumpRegister> afhankelijk van de doel computer. Voor de volle Quantum Simulator schrijft het naar het bestand met de functie Wave tot een globale fase van het Quantum subsysteem dat wordt gegenereerd door de geleverde qubits in dezelfde indeling als <xref:Microsoft.Quantum.Diagnostics.DumpMachine> .  Bijvoorbeeld: Voer een machine opnieuw uit met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} =-e ^ {-i \ Pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ aanroepen <xref:Microsoft.Quantum.Diagnostics.DumpRegister> voor `qubit[0]` genereert deze uitvoer:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     _******************* [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

en aanroepen <xref:Microsoft.Quantum.Diagnostics.DumpRegister> voor `qubit[1]` het genereren van deze uitvoer:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Over het algemeen is de status van een REGI ster dat Entangled met een ander REGI ster een gemengde status in plaats van een zuivere status. In dit geval <xref:Microsoft.Quantum.Diagnostics.DumpRegister> voert het volgende bericht uit:

```
Qubits provided (0;) are entangled with some other qubit.
```

In het volgende voor beeld ziet u hoe u zowel <xref:Microsoft.Quantum.Diagnostics.DumpRegister> als <xref:Microsoft.Quantum.Diagnostics.DumpMachine> in uw Q# code kunt gebruiken:

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

Onder `Assert` en `Dump` functions en Operations Q# ondersteunt een subset van de standaard functies voor het opsporen van fouten in Visual Studio: het [instellen van regel onderbrekingen](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), het [door lopen van code met behulp van F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)en het [inspecteren van de waarden van klassieke variabelen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) zijn allemaal mogelijk wanneer u uw code op de Simulator uitvoert.

Fout opsporing in Visual Studio code maakt gebruik van de mogelijkheden voor fout opsporing die worden geboden door de C# voor Visual Studio code-extensie die wordt ondersteund door OmniSharp en waarvoor de [nieuwste versie](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)moet worden geïnstalleerd. 
