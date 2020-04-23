---
title: Q#-programma's testen en debuggen
description: Leer hoe u eenheidstests, feiten en beweringen gebruiken en hoe u kwantumprogramma's testen en debuggen.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030579"
---
# <a name="testing-and-debugging"></a>Testen en debuggen

Net als bij de klassieke programmering, is het essentieel om te kunnen controleren of quantum programma's handelen zoals bedoeld, en in staat zijn om een quantum programma dat onjuist is diagnosticeren.
In deze sectie behandelen we de tools die Q# biedt voor het testen en debuggen van kwantumprogramma's.

## <a name="unit-tests"></a>Eenheidstests

Een veel voorkomende benadering van het testen van klassieke programma's is het schrijven van kleine programma's genaamd *unit tests* die code uitvoeren in een bibliotheek en de output te vergelijken met een aantal verwachte output.
Bijvoorbeeld, kunnen we willen `Square(2)` ervoor `4`zorgen dat rendementen, omdat we weten *a priori* dat $ 2 ^ 2 = 4 $.

Q# ondersteunt het maken van eenheidstests voor quantumprogramma's en die kunnen worden uitgevoerd als tests binnen het [testkader van](https://xunit.github.io/) de xUnit-eenheid.

### <a name="creating-a-test-project"></a>Een testproject maken

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Open Visual Studio 2019. Ga naar `File` het `New`  >  `Project...`menu en selecteer .
Zoek in de rechterbovenhoek `Q#`naar en `Q# Test Project` selecteer de sjabloon.

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

Voer vanaf uw favoriete opdrachtregel de volgende opdracht uit:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Uw nieuwe project heeft `Tests.qs`één bestand, dat een handige plek biedt om nieuwe Q#-eenheidstests te definiëren.
In eerste instantie bevat dit `AllocateQubit` bestand een voorbeeldeenheidstest die controleert of{0}een nieuw toegewezen qubit zich in de $\ket $ staat bevindt en een bericht afdrukt:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:nieuw: elke Q#-bewerking of -functie `Unit` die `Unit` een argument van type `@Test("...")` en retouren gebruikt, kan worden gemarkeerd als een eenheidstest via het kenmerk. Het argument van `"QuantumSimulator"` dat kenmerk geeft hierboven het doel aan waarop de test wordt uitgevoerd. Eén test kan op meerdere doelen worden uitgevoerd. Voeg bijvoorbeeld een `@Test("ResourcesEstimator")` kenmerk `AllocateQubit`toe boven . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Sla het bestand op en voer alle tests uit. Er moeten nu twee unit tests, een waar AssignQubit wordt uitgevoerd op de QuantumSimulator, en een waar het wordt uitgevoerd in de ResourceEstimator. 

De Q# compiler herkent de ingebouwde doelen "QuantumSimulator", "ToffoliSimulator" en "ResourcesEstimator" als geldige uitvoeringsdoelen voor eenheidstests. Het is ook mogelijk om een volledig gekwalificeerde naam op te geven om een aangepaste uitvoeringsdoelstelling te definiëren. 

### <a name="running-q-unit-tests"></a>Q#-eenheidstests uitvoeren

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Ga als een malige installatie per `Test` oplossing naar `Test Settings`  >  `Default Processor Architecture`  >  `X64`het menu en selecteer .

> [!TIP]
> De standaardinstelling voor processorarchitectuur voor Visual Studio`.suo`wordt opgeslagen in het bestand () voor elke oplossing ( ) bestand.
> Als u dit bestand verwijdert, moet `X64` u opnieuw als uw processorarchitectuur selecteren.

Bouw het project, `Test` ga naar `Windows`  >  `Test Explorer`het menu en selecteer . `AllocateQubit`wordt weergegeven in de lijst `Not Run Tests` met tests in de groep. Selecteer `Run All` of voer deze individuele test uit, en het moet slagen!

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

Als u tests wilt uitvoeren, navigeert `Tests.csproj`u naar de projectmap (de map die bevat) en voert u de opdracht uit:

```bash
$ dotnet restore
$ dotnet test
```

U moet uitvoer krijgen die vergelijkbaar is met het volgende:

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

Eenheidstests kunnen worden gefilterd op basis van hun naam en/of het uitvoeringsdoel:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

De intrinsieke <xref:microsoft.quantum.intrinsic.message> `(String -> Unit)` functie heeft type en maakt het mogelijk diagnostische berichten te maken.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nadat u een test hebt uitgevoerd in Test Explorer en op de test hebt geklikt, verschijnt er een paneel met informatie over de uitvoering van de test: Geslaagd/Mislukt-status, verstreken tijd en een koppeling 'Uitvoer'. Als u op de koppeling 'Uitvoer' klikt, wordt de testuitvoer in een nieuw venster geopend.

![testuitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

De pass/fail-status voor elke test `dotnet test`wordt op de console afgedrukt door .
Voor falende tests worden de uitgangen ook afgedrukt op de console om de fout te diagnosticeren.

***

## <a name="facts-and-assertions"></a>Feiten en beweringen

Omdat functies in Q# geen _logische_ bijwerkingen hebben, kunnen _andere soorten_ effecten van het `()` uitvoeren van een functie waarvan het uitvoertype de lege tuple is, nooit worden waargenomen vanuit een Q#-programma.
Dat wil zeggen, een doelmachine kan ervoor `()` kiezen om geen functie uit te voeren die terugkeert met de garantie dat deze omissie het gedrag van een volgende Q#-code niet zal wijzigen.
Dit maakt `()` functies die terugkeren `Unit`(d.w.z. ) een handig hulpmiddel voor het insluiten van beweringen en het debuggen van logica in Q#-programma's. 

Laten we eens kijken naar een eenvoudig voorbeeld:

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

Hier geeft `fail` het trefwoord aan dat de berekening niet door mag gaan, waardoor een uitzondering wordt gemaakt in de doelmachine waarop het Q#-programma wordt uitgevoerd.
Per definitie kan een dergelijke fout niet worden waargenomen vanuit Q#, omdat `fail` er geen nieuwe Q#-code wordt uitgevoerd nadat een instructie is bereikt.
Dus, als we verder `PositivityFact`gaan dan een oproep aan , kunnen we worden verzekerd door dat de input positief was.

Houd er rekening mee dat `PositivityFact` we [`Fact`](xref:microsoft.quantum.diagnostics.fact) hetzelfde <xref:microsoft.quantum.diagnostics> gedrag kunnen implementeren als het gebruik van de functie vanuit de naamruimte:

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

*Beweringen worden daarentegen*op dezelfde manier gebruikt als feiten, maar kunnen afhankelijk zijn van de toestand van de doelmachine. Overeenkomstig worden ze gedefinieerd als bewerkingen, terwijl feiten worden gedefinieerd als functies (zoals hierboven).
Om het onderscheid te begrijpen, overweeg dan het volgende gebruik van een feit in een bewering:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Hier gebruiken we de <xref:microsoft.quantum.environment.getqubitsavailabletouse> bewerking om het aantal qubits dat beschikbaar is voor gebruik terug te geven.
Aangezien dit duidelijk afhangt van de wereldwijde toestand van het `AssertQubitsAreAvailable` programma en de uitvoeringsomgeving, moet onze definitie van een operatie ook zijn.
We kunnen die globale status echter `Bool` gebruiken om een `Fact` eenvoudige waarde te leveren als input voor de functie.

Voortbouwend op deze ideeën, [de prelude](xref:microsoft.quantum.libraries.standard.prelude) <xref:microsoft.quantum.intrinsic.assert> biedt <xref:microsoft.quantum.intrinsic.assertprob> twee bijzonder nuttige `()`beweringen, en beide gemodelleerd als operaties op . Deze beweringen nemen elk een Exploitant Pauli die een bepaalde meting van belang beschrijft, een quantumregister waarop een meting moet worden uitgevoerd, en een hypothetischresultaat.
Op doelmachines die werken door simulatie, zijn we niet gebonden aan [de stelling zonder klonen](https://en.wikipedia.org/wiki/No-cloning_theorem), en kunnen dergelijke metingen uitvoeren zonder het register te verstoren dat aan dergelijke beweringen wordt doorgegeven.
Een simulator kan dan, `PositivityFact` vergelijkbaar met de bovenstaande functie, de berekening afbreken als de hypothetische uitkomst in de praktijk niet zou worden waargenomen:

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

Op fysieke kwantumhardware, waar de stelling zonder klonen onderzoek `Assert` van `AssertProb` kwantumtoestand `()` verhindert, keren de en operaties gewoon zonder ander effect terug.

De <xref:microsoft.quantum.diagnostics> naamruimte biedt nog `Assert` een aantal functies van de familie die ons in staat stellen om meer geavanceerde voorwaarden te controleren. 

## <a name="dump-functions"></a>Dumpfuncties

Om quantumprogramma's <xref:microsoft.quantum.diagnostics> voor problemen op te lossen, biedt de naamruimte twee <xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics.dumpregister>functies die in een bestand de huidige status van de doelmachine kunnen dumpen: en . De gegenereerde output van elk is afhankelijk van de doelmachine.

### <a name="dumpmachine"></a>DumpMachine

De full-state quantum simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [golffunctie](https://en.wikipedia.org/wiki/Wave_function) van het hele kwantumsysteem, als een eendimensionale array van complexe getallen, waarin elk element vertegenwoordigt de amplitude van de waarschijnlijkheid van het meten van de computationele basis staat $\ket{n}$, waar $\ket{n} = \ket{b_{n-1}... b_1b_0 voor bits\{b_i\}$. Bijvoorbeeld, op een machine met slechts twee qubits toegewezen en in de quantum staat $${1}\begin{align} \ket{\psi} = \frac {\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ bellen <xref:microsoft.quantum.diagnostics.dumpmachine> genereert deze output:

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

De eerste rij geeft een opmerking met de id's van de bijbehorende qubits in hun significante volgorde.
De rest van de rijen beschrijven de waarschijnlijkheidsamplitude van het meten van de basisstatusvector $\ket{n}$ in zowel Cartesiaanse als polaire formaten. In detail voor de eerste rij:

* **`∣0❭:`** deze rij komt `0` overeen met de computationele basisstatus
* **`0.707107 +  0.000000 i`**: de waarschijnlijkheidsamplitude in Cartesiaans formaat.
* **` == `**: `equal` het teken scheidt beide gelijkwaardige voorstellingen.
* **`**********  `**: Een grafische weergave van de `*` omvang, het aantal is evenredig aan de waarschijnlijkheid van het meten van deze staat vector.
* **`[ 0.500000 ]`**: de numerieke waarde van de magnitude
* **`    ---`**: Een grafische weergave van de fase van de amplitude (zie hieronder).
* **`[ 0.0000 rad ]`**: de numerieke waarde van de fase (in radialen).

Zowel de omvang als de fase worden weergegeven met een grafische weergave. De magnitude representatie is rechttoe rechtaan: het toont een balk van `*`, hoe groter de kans hoe groter de bar zal zijn. Voor de fase tonen we de volgende symbolen om de hoek weer te geven op basis van bereiken:

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

De volgende voorbeelden `DumpMachine` tonen voor sommige gemeenschappelijke staten:

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
  > De id van een qubit wordt toegewezen tijdens runtime en is niet noodzakelijkerwijs afgestemd op de volgorde waarin de qubit is toegewezen of zijn positie binnen een qubit-register.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > U een qubit-id in Visual Studio achterhalen door een breekpunt in uw code te plaatsen en de waarde van een qubit-variabele te inspecteren, bijvoorbeeld:
  > 
  > ![qubit-id weergeven in Visual Studio](~/media/qubit_id.png)
  >
  > de qubit `0` met `register2` index`3`op heeft id= `1` ,`2`de qubit met index heeft id= .

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > U een qubit-id <xref:microsoft.quantum.intrinsic.message> achterhalen met behulp van de functie en de qubit-variabele in het bericht doorgeven, bijvoorbeeld:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > die deze output zou kunnen genereren:
  >```
  > 0=q:3; 1=q:2
  >```
  > dit betekent dat de `0` qubit met index `register2` op id=`3`heeft, de qubit met index `1` id=`2`heeft.


***

<xref:microsoft.quantum.diagnostics.dumpmachine>maakt deel <xref:microsoft.quantum.diagnostics> uit van de naamruimte, dus om `open` deze te gebruiken moet u een instructie toevoegen:

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

<xref:microsoft.quantum.diagnostics.dumpregister>werkt <xref:microsoft.quantum.diagnostics.dumpmachine>als , behalve dat er ook een array van qubits nodig is om de hoeveelheid informatie te beperken tot alleen die relevant zijn voor de bijbehorende qubits.

Net <xref:microsoft.quantum.diagnostics.dumpmachine>als bij , <xref:microsoft.quantum.diagnostics.dumpregister> de informatie gegenereerd door is afhankelijk van de doelmachine. Voor de full-state quantum simulator schrijft in het bestand de golf functie tot een globale fase van de <xref:microsoft.quantum.diagnostics.dumpmachine>quantum sub-systeem gegenereerd door de verstrekte qubits in hetzelfde formaat als .  Bijvoorbeeld, neem opnieuw een machine met slechts twee{1}qubits toegewezen en in de quantum staat $$ \begin{align}{2}\ket{\psi} = \frac {\sqrt } \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ({1}(\frac {\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ oproep <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[0]` genereert deze output:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

en <xref:microsoft.quantum.diagnostics.dumpregister> het `qubit[1]` vragen om genereert deze output:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

In het algemeen is de toestand van een register dat is verstrengeld met een ander register een gemengde staat in plaats van een zuivere staat. In dit <xref:microsoft.quantum.diagnostics.dumpregister> geval wordt het volgende bericht weergegeven:

```
Qubits provided (0;) are entangled with some other qubit.
```

In het volgende voorbeeld ziet <xref:microsoft.quantum.diagnostics.dumpregister> u <xref:microsoft.quantum.diagnostics.dumpmachine> hoe u beide gebruiken en in uw Q#-code:

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

`Assert` Naast en `Dump` functies en bewerkingen ondersteunt Q# een subset van standaard Visual Studio-foutopsporingsmogelijkheden: [lijnbreekpunten instellen,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [code doorlopen met F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) en het inspecteren van waarden van klassieke [variabelen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) zijn allemaal mogelijk tijdens codeuitvoering op de simulator.

Foutopsporing in Visual Studio Code maakt gebruik van de foutopsporingsmogelijkheden die worden geboden door de C#for Visual Studio Code-extensie aangedreven door OmniSharp en vereist het installeren van de [nieuwste versie.](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) 
