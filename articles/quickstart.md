---
title: Basisprincipes van het schrijven van kwantumprogramma's in Q#
description: Meer informatie over het schrijven van een kwantumprogramma in Q#. Een toepassing voor een Bell-toestand ontwikkelen met behulp van de Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 10/07/2019
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 8d3b2d7c8da39a961f4eedcc5989ad3a1e134ade
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906726"
---
# <a name="quantum-basics-with-q"></a>Basisprincipes van schrijven van kwantumprogramma's in Q#

In deze quickstart laten we u zien hoe u een Q#-programma schrijft dat qubits bewerkt en meet, en dat de effecten van superpositie en verstrengeling demonstreert.  U krijgt instructies voor het installeren van de QDK, het bouwen van het programma en het uitvoeren van dat programma op een kwantumsimulator.  

U gaat een toepassing schrijven met de naam Bell om kwantumverstrengeling te demonstreren.  De naam Bell is een verwijzing naar de Bell-toestanden, wat specifieke kwantumtoestanden van twee qubits zijn die worden gebruikt om de eenvoudigste voorbeelden van superpositie en kwantumverstrengeling voor te stellen. 

## <a name="pre-requisites"></a>Vereisten

Als u klaar bent om te gaan coderen, voert u deze stappen uit voordat u verdergaat: 

* [Installeer](xref:microsoft.quantum.install) de Quantum Development Kit met behulp van de taal en ontwikkelomgeving van uw voorkeur
* Als u de QDK al hebt geïnstalleerd, controleert u of uw versie is [bijgewerkt](xref:microsoft.quantum.update) naar de nieuwste versie

U kunt de instructies ook volgen zonder de QDK te installeren, om een beeld te krijgen van de Q#-programmeertaal en de basisconcepten van kwantumcomputing.

## <a name="demonstrating-qubit-behavior-with-q"></a>Gedrag van qubits demonstreren met Q#

Denk nog even terug aan onze eenvoudige [definitie van een qubit](xref:microsoft.quantum.overview.what#the-qubit).  Waar klassieke bits één binaire waarde bevatten, zoals een 0 of een 1, kan de toestand van een qubit in een **superpositie** zijn van gelijktijdig 0 en 1.  Conceptueel gezien kan een qubit worden gezien als een richting in de ruimte (ook wel een vector genoemd).  Een qubit kan zich in een van de mogelijke richtingen bevinden. De twee **klassieke toestanden** zijn de twee richtingen, die een 100% kans vertegenwoordigen dat de meting 0 oplevert en een 100% kans dat de meting 1 oplevert.  Deze voorstelling is ook formeel te visualiseren door de zogenaamde [Blochbol](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).


De handeling van het meten produceert een binair resultaat en verandert de toestand van een qubit. Meting resulteert in een binaire waarde, 0 of 1.  De qubit gaat over van de toestand van superpositie (willekeurige richting) in een van de klassieke toestanden.  Daarna levert herhaling van dezelfde meting zonder tussenliggende bewerkingen hetzelfde binaire resultaat op.  

Meerdere qubits kunnen worden **verstrengeld**. Wanneer we een meting uitvoeren van één verstrengelde qubit, wordt onze kennis van de toestand van de andere qubit(s) ook bijgewerkt.

We laten nu zien hoe dit gedrag wordt uitgedrukt in Q#.  U begint met het eenvoudigst mogelijke programma en bouwt dit op om kwantumsuperpositie en kwantumverstrengeling te demonstreren.

## <a name="setup"></a>Instellen

Toepassingen die zijn ontwikkeld met de Quantum Development Kit van Microsoft bestaan uit twee delen:

1. Een of meer kwantumalgoritmen, geïmplementeerd met behulp van de kwantumprogrammeertaal Q#.
1. Een hostprogramma, geïmplementeerd in een programmeertaal als Python of C#, die als het belangrijkste toegangspunt fungeert en Q#-bewerkingen aanroept om een kwantumalgoritme uit te voeren.

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Een locatie kiezen voor uw toepassing

1. Maak een bestand met de naam `Bell.qs`. Dit bestand bevat uw Q#-code.

1. Maak een bestand met de naam `host.py`. Dit bestand bevat uw Python-hostcode.

#### <a name="c-command-line"></a>[C#-opdrachtregel](#tab/tabid-csharp)

1. Een nieuw Q#-project maken:

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    Als het goed is, ziet u een `.csproj`-bestand, een Q#-bestand met de naam `Operations.qs` en een hostprogrammabestand met de naam `Driver.cs`

1. De naam van het Q#-bestand wijzigen

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. Een nieuw project maken

   * Open Visual Studio
   * Ga naar het menu **Bestand** en selecteer **Nieuw** -> **Project...**
   * Typ in de sjabloonverkenner `Q#` in het zoekveld en selecteer de sjabloon `Q# Application`
   * Geef uw project de naam `Bell`

1. De naam van het Q#-bestand wijzigen

   * Ga naar **Solution Explorer**
   * Klik met de rechter muisknop op bestand `Operations.qs`
   * Wijzig de naam in `Bell.qs`

* * *

## <a name="write-a-q-operation"></a>Een Q#-bewerking schrijven

We willen twee qubits voorbereiden in een specifieke kwantumtoestand om te laten zien hoe u met Q# bewerkingen kunt uitvoeren op qubits om hun toestand te wijzigen en om de effecten van superpositie en verstrengeling te demonstreren. Dit alles wordt stukje voor stukje opgebouwd om qubittoestanden, bewerkingen en metingen te demonstreren.

**Overzicht:**  In het eerste codevoorbeeld hieronder laten we u zien hoe u met qubits kunt werken in Q#.  We introduceren twee bewerkingen, `M` en `X`, die de toestand van een qubit transformeren. 

In dit codefragment wordt een bewerking `Set` gedefinieerd die een qubit als parameter accepteert, evenals een andere parameter, `desired`, die de gewenste toestand van de qubit aangeeft.  Met de bewerking `Set` wordt een meting uitgevoerd op de qubit met behulp van de bewerking `M`.  In Q# levert een qubitmeting altijd `Zero` of `One` op.  Als de meting een waarde oplevert die niet gelijk is aan een gewenste waarde, wordt de qubit 'gespiegeld' door Set. Dit houdt in dat er een bewerking `X` wordt uitgevoerd waardoor de toestand van de qubit wordt gewijzigd in een nieuwe toestand waarin de waarschijnlijkheid dat een meting `Zero` en `One` oplevert, wordt omgedraaid.  Om het effect van de bewerking `Set` te demonstreren, wordt er vervolgens een bewerking `TestBellState` toegevoegd.  Deze bewerking krijgt als invoer een `Zero` of `One` en roept de bewerking `Set` een aantal keer aan met die invoer, en telt het aantal keren dat `Zero` het resultaat is van de meting van de qubit en het aantal keren dat `One` wordt geretourneerd. In deze eerste simulatie van de bewerking `TestBellState` verwachten we natuurlijk dat de uitvoer laat zien dat alle metingen van de qubit die is ingesteld met de parameterinvoer `Zero`, `Zero` oplevert en dat alle metingen van de qubit die is ingesteld met `One` als de parameterinvoer, `One` retourneert.  Later voegen we code toe aan `TestBellState` om de concepten van superpositie en verstrengeling te demonstreren.


### <a name="q-operation-code"></a>Q#-bewerkingscode

1. Vervang de inhoud van het bestand Bell.qs door de volgende code:

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    Deze bewerking kan nu worden aangeroepen om een qubit in te stellen op een klassieke toestand, met in 100% van de gevallen `Zero` of `One` als resultaat.  `Zero` en `One` zijn constanten die de enige twee mogelijke resultaten van een meting van een qubit vertegenwoordigen.

    Met de bewerking `Set` wordt de qubit gemeten.
    Als de qubit zich in de gewenste toestand bevindt, wordt de toestand ongewijzigd gelaten door `Set`. Als dat niet zo is, wordt de toestand van de qubit gewijzigd in de gewenste toestand door het uitvoeren van de bewerking `X`.

### <a name="about-q-operations"></a>Q#-bewerkingen

Een Q#-bewerking is een kwantumsubroutine, ofwel een aanroepbare routine die kwantumbewerkingen bevat.

De argumenten voor een bewerking worden tussen haakjes opgegeven als een tupel.

Het retourtype van de bewerking wordt na een dubbele punt opgegeven. In dit geval heeft de bewerking `Set` geen retourwaarde, zodat deze is gemarkeerd als retourzending `Unit`. Dit is het Q#-equivalent van `unit` in F#, dat ongeveer analoog is met `void` in C#, en een lege tupel (`Tuple[()]`) in Python.

U hebt twee kwantumbewerkingen gebruikt in uw eerste Q#-bewerking:

* De bewerking [M](xref:microsoft.quantum.intrinsic.m), waarmee de toestand van de qubit wordt gemeten
* De bewerking [X](xref:microsoft.quantum.intrinsic.x), waarmee de toestand van een qubit wordt gespiegeld

Een kwantumbewerking transformeert de toestand van een qubit. Soms worden kwantumbewerkingen ook wel kwantumpoorten genoemd, analoog aan klassieke logische poorten. Dit vindt zijn oorsprong in het begintijdperk van de kwantumcomputing, toen algoritmen niets meer waren dan een theoretische constructie en werden gevisualiseerd als schema's, vergelijkbaar met circuitschema's in klassieke computing.

### <a name="add-q-test-code"></a>Q#-testcode toevoegen

1. Voeg na het einde van bewerking `Set` de volgende bewerking toe aan `Bell.qs` bestand binnen de naamruimte:

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    Deze bewerking (`TestBellState`) wordt gedurende `count` iteraties als een lus uitgevoerd, er wordt een opgegeven `initial`-waarde voor een qubit gedefinieerd en vervolgens wordt het resultaat, (`M`), gemeten. Er worden statistieken verzameld over het aantal nullen en enen dat we hebben gemeten, waarna ze naar de aanroepende functie worden geretourneerd. Er wordt nog een andere noodzakelijke bewerking uitgevoerd. De qubit wordt opnieuw ingesteld op een bekende toestand (`Zero`) voordat deze wordt geretourneerd, zodat anderen deze qubit een bekende toestand kunnen toewijzen. Dit wordt door de instructie `using` vereist.

### <a name="about-variables-in-q"></a>Variabelen in Q#

Standaard zijn variabelen in Q# niet meer te veranderen. De waarde kan niet worden gewijzigd als de variabele gebonden is. Het sleutelwoord `let` wordt gebruikt om de binding van een onveranderlijke variabele aan te geven. Bewerkingsargumenten zijn altijd onveranderbaar.

Als u een variabele nodig hebt waarvan de waarde kan worden gewijzigd, zoals `numOnes` in het voorbeeld, kunt u de variabele declareren met het sleutelwoord `mutable`. De waarde van een veranderlijke variabele kan worden gewijzigd met behulp van een `set`-instructie.

In beide gevallen wordt het type variabele door de compiler afgeleid. Voor Q# zijn geen typeannotaties vereist voor variabelen.

### <a name="about-using-statements-in-q"></a>`using`-instructies in Q#

De instructie `using` is ook speciaal in Q#. Deze wordt gebruikt om qubits toe te wijzen voor gebruik in een codeblok. In Q# worden alle qubits dynamisch toegewezen en vrijgegeven. Het zijn geen vaste resources die de gehele levensduur van een complex algoritme meegaan. Een `using`-instructie wijst aan het begin een set qubits toe en geeft deze qubits aan het einde van het blok vrij.

## <a name="create-the-host-application-code"></a>De code van de hosttoepassing maken

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Open bestand `host.py` en voeg de volgende code toe:

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

1. Vervang de inhoud van bestand `Driver.cs` door de volgende code:

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a>De code van de hosttoepassing

#### <a name="python"></a>[Python](#tab/tabid-python)

De Python-hosttoepassing kent drie onderdelen:

* Bereken de argumenten die vereist zijn voor het kwantumalgoritme. In het voorbeeld wordt `count` vastgezet op 1000 en `initial` is de beginwaarde van de qubit.
* Voer het kwantumalgoritme uit door methode `simulate()` van de geïmporteerde Q#-bewerking aan te roepen.
* Verwerk het resultaat van de bewerking. In het voorbeeld ontvangt `res` het resultaat van de bewerking. Hier is het resultaat een tupel van het aantal nullen (`num_zeros`) en het aantal enen (`num_ones`) dat door de simulator wordt gemeten. De tupel wordt gedeconstrueerd om de twee velden te krijgen en de resultaten worden afgedrukt.

#### <a name="c"></a>[C#](#tab/tabid-csharp)

De C#-hosttoepassing bestaat uit vier delen:

* Bouw een kwantumsimulator. In het voorbeeld is `qsim` de simulator.
* Bereken de argumenten die vereist zijn voor het kwantumalgoritme. In het voorbeeld wordt `count` vastgezet op 1000 en `initial` is de beginwaarde van de qubit.
* Voer het kwantumalgoritme uit. Elke Q#-bewerking genereert een C#-klasse met dezelfde naam. Deze klasse heeft een methode `Run` die de bewerking **asynchroon** uitvoert. De uitvoering is asynchroon, omdat de uitvoering op feitelijke hardware asynchroon is. Aangezien methode `Run` asynchroon is, wordt eigenschap `Result` opgehaald. Hiermee wordt de uitvoering geblokkeerd totdat de taak is voltooid en het resultaat synchroon wordt geretourneerd.
* Verwerk het resultaat van de bewerking. In het voorbeeld ontvangt `res` het resultaat van de bewerking. Hier is het resultaat een tupel van het aantal nullen (`numZeros`) en het aantal enen (`numOnes`) dat door de simulator wordt gemeten. Dit wordt geretourneerd als een ValueTuple in C#. De tupel wordt gedeconstrueerd om de twee velden te krijgen, de resultaten worden afgedrukt en er wordt gewacht op het indrukken van een toets.

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a>Bouwen en uitvoeren

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Voer de volgende opdracht uit via de terminal:

    ```
    python host.py
    ```

    Met deze opdracht wordt de hosttoepassing uitgevoerd, waarmee de Q#-bewerking wordt gesimuleerd.

De resultaten moeten zijn:

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[Opdrachtregel/Visual Studio Code](#tab/tabid-csharp)

1. Voer het volgende uit op de terminal:

    ```bash
    dotnet run
    ```

    Met deze opdracht worden alle vereiste pakketten automatisch gedownload, wordt de toepassing gebouwd en vervolgens uitgevoerd op de opdrachtregel.

1. U kunt ook op **F1** drukken om het opdrachtpalet te openen en **Fouten opsporen: starten zonder foutopsporing** te selecteren.
U wordt mogelijk gevraagd een nieuw bestand ``launch.json`` te maken waarin wordt beschreven hoe u het programma kunt starten.
Het standaardbestand ``launch.json`` moet voor de meeste toepassingen goed werken.

De resultaten moeten zijn:

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. Druk op `F5` om het programma te bouwen en uit te voeren.

De resultaten moeten zijn:

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

Het programma wordt afgesloten nadat u op een toets hebt gedrukt.

* * *

## <a name="prepare-superposition"></a>Superpositie voorbereiden

**Overzicht** Laten we nu eens kijken welke manieren beschikbaar zijn in Q# om qubits in superpositie te plaatsen.  Zoals eerder gezegd, kan de toestand van een qubit een superpositie zijn van 0 en 1.  We gaan de bewerking `Hadamard` gebruiken om dit te bereiken. Als de qubit zich in een van de klassieke toestanden bevindt (waarbij een meting altijd `Zero` of altijd `One` retourneert) wordt de qubit met de bewerking `Hadamard` of `H` in een toestand geplaatst waarin een meting van de qubit in 50% van de gevallen `Zero` retourneert en in 50% van de gevallen `One`.  Conceptueel gezien, kan de qubit worden beschouwd als halverwege tussen de `Zero` en `One`.  Als we nu de bewerking `TestBellState` simuleren, zien we dat de resultaten na meting ongeveer een gelijk aantal keren `Zero` en `One` bevatten.  

Eerst proberen we de qubit te spiegelen (als de qubit zich in de toestand `Zero` bevindt, wordt deze gespiegeld naar `One` en omgekeerd). Dit wordt bereikt door een bewerking `X` uit te voeren voordat we de qubit meten in `TestBellState`:

```qsharp
X(qubit);
let res = M(qubit);
```

De resultaten (nadat u op `F5` hebt gedrukt) worden nu omgedraaid:

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

Alles wat we tot nu toe hebben gezien, is echter klassiek. Laten we een kwantumresultaat ophalen. We hoeven alleen maar de bewerking `X` uit het vorige voorbeeld te vervangen door een bewerking `H` of Hadamard. In plaats van de qubit te spiegelen van 0 naar 1, wordt deze slechts half gespiegeld. De vervangen regels in `TestBellState` zien er nu als volgt uit:

```qsharp
H(qubit);
let res = M(qubit);
```

De resultaten worden nu interessanter:

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

Telkens als we meten, vragen we om een klassieke waarde, maar de qubit bevindt zich halverwege tussen 0 en 1, zodat we de helft van de tijd (statistisch) 0 en de helft van de tijd 1 krijgen. Dit staat bekend als __superpositie__ en geeft ons de eerste echte blik op een kwantumtoestand.

## <a name="prepare-entanglement"></a>Verstrengeling voorbereiden

**Overzicht:**  Laten we nu eens kijken welke manieren beschikbaar zijn in Q# om verstrengeling van qubits uit te drukken.  Eerst stellen we de eerste qubit in op de begintoestand en gebruiken we vervolgens de bewerking `H` om deze in superpositie te brengen.  Vervolgens gebruiken we, voordat we de eerste qubit gaan meten, een nieuwe bewerking (`CNOT`), die staat voor Controlled-Not.  Het resultaat van het uitvoeren van deze bewerking op twee qubits is het spiegelen van de tweede qubit als de eerste qubit `One` is.  Nu zijn de twee qubits verstrengeld.  Onze statistieken voor de eerste qubit zijn niet gewijzigd (kans van 50% op een `Zero` of `One` na meting), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ de uitkomst die voor de eerste qubit is gemeten. Onze `CNOT`-poort heeft de twee qubits verstrengeld, zodat wat er met de ene gebeurt, ook met de andere gebeurt. Als u de metingen omkeert (de tweede qubit vóór de eerste), zou zich hetzelfde voordoen. De eerste meting zal willekeurig zijn, waarna de tweede zich houdt aan wat voor de eerste is gedetecteerd.

Het eerste wat we nu moeten doen, is twee qubits toewijzen in plaats van één in `TestBellState`:

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

Zo kunnen we een nieuwe bewerking (`CNOT`) toevoegen voordat we een meting (`M`) in `TestBellState` uitvoeren:

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

We hebben nog een andere `Set`-bewerking toegevoegd om de eerste qubit te initialiseren, zodat we zeker weten dat deze altijd in toestand `Zero` is wanneer we starten.

We moeten ook de tweede qubit opnieuw instellen voordat deze wordt vrijgegeven.

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

De volledige routine ziet er nu als volgt uit:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

Als we deze uitvoeren, krijgen we precies hetzelfde 50-50-resultaat dat we eerder hadden. Het is echter belangrijk om te weten hoe de tweede qubit reageert op het meten van de eerste. We voegen deze statistiek toe met een nieuwe versie van de `TestBellState`-bewerking:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

In de nieuwe retourwaarde (`agree`) wordt telkens bijgehouden als de meting van de eerste qubit overeenkomt met de meting van de tweede qubit. We moeten ook de hosttoepassing dienovereenkomstig bijwerken:

#### <a name="python"></a>[Python](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

Wanneer we nu een uitvoering doen, krijgen we verbluffende uitkomst:

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

Zoals aangegeven in het overzicht, zijn onze statistieken voor de eerste qubit niet gewijzigd (kans van 50% op 0 of 1), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ dezelfde uitkomst als voor de eerste qubit, omdat ze namelijk verstrengeld zijn.

Gefeliciteerd, u hebt uw eerste kwantumprogramma geschreven.

## <a name="whats-next"></a>Volgende stappen

De quickstart [Zoekalgoritme van Grover](xref:microsoft.quantum.quickstarts.search) laat zien hoe u een zoekalgoritme van Grover kunt bouwen en uitvoeren, een van de populairste algoritmen uit de kwantumcomputing en een goed voorbeeld van een Q#-programma dat kan worden gebruikt voor het oplossen van echte problemen met kwantumcomputing.  

In [Aan de slag met de Quantum Development Kit](xref:microsoft.quantum.welcome) vindt u meer manieren om te leren werken met Q# en kwantumprogrammering.

