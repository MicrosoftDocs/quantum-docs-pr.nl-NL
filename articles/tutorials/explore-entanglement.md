---
title: Verken entanglement met Q#
description: Meer informatie over het schrijven van een Quantum programma in Q# . Een toepassing voor een Bell-toestand ontwikkelen met behulp van de Quantum Development Kit (QDK)
author: geduardo
ms.author: v-edsanc
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- Q#
- $$v
ms.openlocfilehash: 7a1a49e18ac9330ca6e3cc89b3e58c96eccb91db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691664"
---
# <a name="tutorial-explore-entanglement-with-q"></a>Zelfstudie: kennismaken met verstrengeling met Q#\#

In deze zelf studie laten we u zien hoe u een Q# programma schrijft dat qubits bewerkt en meet en de effecten van superpositie en entanglement toont.

U gaat een toepassing schrijven met de naam Bell om kwantumverstrengeling te demonstreren.
De naam Bell is een verwijzing naar de Bell-toestanden, wat specifieke kwantumtoestanden van twee qubits zijn die worden gebruikt om de eenvoudigste voorbeelden van superpositie en kwantumverstrengeling voor te stellen.

## <a name="pre-requisites"></a>Vereisten

Als u klaar bent om te gaan coderen, voert u deze stappen uit voordat u verdergaat: 

* [Installeer](xref:microsoft.quantum.install) de Quantum Development Kit met uw voorkeurs taal en-ontwikkelings omgeving.
* Als u de QDK al hebt geïnstalleerd, controleert u of uw versie is [bijgewerkt](xref:microsoft.quantum.update) naar de nieuwste versie

U kunt ook de oplossing volgen zonder de QDK te installeren en de overzichten van de Q# programmeer taal en de eerste concepten van quantum computing te bekijken.

## <a name="in-this-tutorial-youll-learn-how-to"></a>In deze zelfstudie leert u het volgende:

> [!div class="checklist"]
> * Bewerkingen in Q maken en combi neren\#
> * Maak bewerkingen om qubits toe te voegen aan de superpositie, entangle en meet ze te meten.
> * Laat Quantum Entanglement zien met een Q# programma dat in een simulator wordt uitgevoerd. 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a>Een demonstratie van het gedrag van Qubit met de QDK

Waar klassieke bits één binaire waarde bevatten, zoals een 0 of een 1, kan de toestand van een [qubit](xref:microsoft.quantum.glossary#qubit) in een **superpositie** zijn van 0 en 1.  In het algemeen kan de status van een Qubit worden beschouwd als een richting in een abstracte ruimte (ook wel een vector genoemd).  Een Qubit-status kan zich in een van de mogelijke richtingen bevindt. De twee **klassieke toestanden** zijn de twee richtingen, die een 100% kans vertegenwoordigen dat de meting 0 oplevert en een 100% kans dat de meting 1 oplevert.

De handeling van het meten produceert een binair resultaat en verandert de toestand van een qubit.
Meting resulteert in een binaire waarde, 0 of 1.  De qubit gaat over van de toestand van superpositie (willekeurige richting) in een van de klassieke toestanden.  Daarna levert herhaling van dezelfde meting zonder tussenliggende bewerkingen hetzelfde binaire resultaat op.  

Meerdere qubits kunnen worden [**verstrengeld**](xref:microsoft.quantum.glossary#entanglement).  Wanneer we een meting uitvoeren van één verstrengelde qubit, wordt onze kennis van de toestand van de andere qubit(s) ook bijgewerkt.

We zijn nu klaar om te laten zien hoe Q# Dit gedrag afspeelt.  U begint met het eenvoudigst mogelijke programma en bouwt dit op om kwantumsuperpositie en kwantumverstrengeling te demonstreren.

## <a name="creating-a-no-locq-project"></a>Een Q# project maken

Het eerste wat u moet doen, is het maken van een nieuw Q# project. In deze zelf studie gaan we de omgeving gebruiken op basis van [ Q# toepassingen met VS code](xref:microsoft.quantum.install.standalone).

In VS code kunt u een nieuw project maken: 

1. Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken** .
2. Klik op **Zelfstandige consoletoepassing** .
3. Ga naar de locatie waar het project moet worden opgeslagen en klik op **Project maken** .
4. Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.

In dit geval wordt het project genoemd `Bell` . Hiermee worden twee bestanden gegenereerd: `Bell.csproj` , het project bestand en `Program.qs` een sjabloon van een Q# toepassing die we gaan gebruiken om onze toepassing te schrijven. De inhoud van `Program.qs` moet het volgende zijn:

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a>De Q- \# toepassing schrijven
 
Ons doel is om twee qubits in een specifieke Quantum staat voor te bereiden en te demonstreren hoe u op qubits kunt rijden Q# om hun status te wijzigen en de effecten van superpositie en entanglement te demonstreren. We bouwen dit stuk per stuk om qubite Staten, bewerkingen en metingen uit te voeren.

### <a name="initialize-qubit-using-measurement"></a>Qubit initialiseren met meting

In het eerste code fragment hieronder ziet u hoe u met qubits kunt werken in Q# .  We voeren twee bewerkingen uit [`M`](xref:Microsoft.Quantum.Intrinsic.m) en zorgen [`X`](xref:Microsoft.Quantum.Intrinsic.X) dat de status van een Qubit wordt getransformeerd. In dit codefragment wordt een bewerking `SetQubitState` gedefinieerd die een qubit als parameter accepteert, evenals een andere parameter, `desired`, die de gewenste toestand van de qubit aangeeft.  Met de bewerking `SetQubitState` wordt een meting uitgevoerd op de qubit met behulp van de bewerking `M`.  In Q# retourneert een Qubit-meting altijd `Zero` of `One` .  Als de meting een waarde retourneert die niet gelijk is aan de gewenste waarde, `SetQubitState` ' spiegelt ' de Qubit; dat wil zeggen, wordt een bewerking uitgevoerd. `X` Hiermee wordt de Qubit-status gewijzigd in een nieuwe status waarin de waarschijnlijkheid van een meting `Zero` wordt geretourneerd en `One` omgekeerd. Op deze manier `SetQubitState` plaatst de doel-Qubit altijd de gewenste status.

Vervang de inhoud van `Program.qs` door de volgende code:


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

Deze bewerking kan nu worden aangeroepen om een qubit in te stellen op een klassieke toestand, met in 100% van de gevallen `Zero` of `One` als resultaat.
`Zero` en `One` zijn constanten die de enige twee mogelijke resultaten van een meting van een qubit vertegenwoordigen.

Met de bewerking `SetQubitState` wordt de qubit gemeten. Als de Qubit zich in de gewenste staat bevindt, `SetQubitState` laat u het zichzelf `X` ongewijzigd. Als u de bewerking uitvoert, veranderen we de status van Qubit in de gewenste status.

#### <a name="about-no-locq-operations"></a>Over Q# bewerkingen

Een Q# bewerking is een Quantum subroutine. Dat wil zeggen dat het een aanroep bare routine is die aanroepen naar andere Quantum bewerkingen bevat.

De argumenten voor een bewerking worden tussen haakjes opgegeven als een tupel.

Het retourtype van de bewerking wordt na een dubbele punt opgegeven. In dit geval heeft de `SetQubitState` bewerking geen retour type, zodat deze als retour waarde wordt gemarkeerd `Unit` . Dit is het Q# equivalent van `unit` in F #, wat ongeveer hetzelfde is als `void` in C# en een lege tuple in python ( `()` , vertegenwoordigd door de type hint `Tuple[()]` ).

U hebt twee Quantum bewerkingen gebruikt in uw eerste Q# bewerking:

* De [`M`](xref:Microsoft.Quantum.Intrinsic.m) bewerking, waarmee de status van de Qubit wordt gemeten
* De [`X`](xref:Microsoft.Quantum.Intrinsic.X) bewerking, die de status van een Qubit spiegelt

Een kwantumbewerking transformeert de toestand van een qubit. Soms worden kwantumbewerkingen ook wel kwantumpoorten genoemd, analoog aan klassieke logische poorten. Dit vindt zijn oorsprong in het begintijdperk van de kwantumcomputing, toen algoritmen niets meer waren dan een theoretische constructie en werden gevisualiseerd als schema's, vergelijkbaar met circuitschema's in klassieke computing.

### <a name="counting-measurement-outcomes"></a>Resultaten van de meting tellen

Om het effect van de bewerking `SetQubitState` te demonstreren, wordt er vervolgens een bewerking `TestBellState` toegevoegd. Deze bewerking krijgt als invoer een `Zero` of `One` en roept de bewerking `SetQubitState` een aantal keer aan met die invoer, en telt het aantal keren dat `Zero` het resultaat is van de meting van de qubit en het aantal keren dat `One` wordt geretourneerd. In deze eerste simulatie van de bewerking `TestBellState` verwachten we natuurlijk dat de uitvoer laat zien dat alle metingen van de qubit die is ingesteld met de parameterinvoer `Zero`, `Zero` oplevert en dat alle metingen van de qubit die is ingesteld met `One` als de parameterinvoer, `One` retourneert. Daarnaast voegen we code toe aan `TestBellState` om superpositie en entanglement te demonstreren.

Voeg na het einde van bewerking `SetQubitState` de volgende bewerking toe aan `Program.qs` bestand binnen de naamruimte:

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
Houd er rekening mee dat er een regel is toegevoegd voor het `return` afdrukken van een verklarend bericht in de-console met de functie ( `Message` ) [micro soft. Quantum. intrinsiek. Message]

Deze bewerking (`TestBellState`) wordt gedurende `count` iteraties als een lus uitgevoerd, er wordt een opgegeven `initial`-waarde voor een qubit gedefinieerd en vervolgens wordt het resultaat, (`M`), gemeten. Er worden statistieken verzameld over het aantal nullen en enen dat we hebben gemeten, waarna ze naar de aanroepende functie worden geretourneerd. Er wordt nog een andere noodzakelijke bewerking uitgevoerd. De qubit wordt opnieuw ingesteld op een bekende toestand (`Zero`) voordat deze wordt geretourneerd, zodat anderen deze qubit een bekende toestand kunnen toewijzen. Dit wordt door de instructie `using` vereist.

#### <a name="about-variables-in-q"></a>Over variabelen in Q\#

Variabelen in Q# zijn standaard onveranderbaar; hun waarde kan niet worden gewijzigd nadat ze zijn gebonden. Het sleutelwoord `let` wordt gebruikt om de binding van een onveranderlijke variabele aan te geven. Bewerkingsargumenten zijn altijd onveranderbaar.

Als u een variabele nodig hebt waarvan de waarde kan worden gewijzigd, zoals `numOnes` in het voorbeeld, kunt u de variabele declareren met het sleutelwoord `mutable`. De waarde van een veranderlijke variabele kan worden gewijzigd met behulp van een `set`-instructie.

In beide gevallen wordt het type variabele door de compiler afgeleid. Q# geen type annotaties voor variabelen vereist.

#### <a name="about-using-statements-in-q"></a>`using`Instructies in Q\#

De `using` instructie is ook speciaal voor Q# . Deze wordt gebruikt om qubits toe te wijzen voor gebruik in een codeblok. In Q# worden alle qubits dynamisch toegewezen en vrijgegeven, in plaats van dat er vaste resources zijn die voor de gehele levens duur van een complex algoritme zijn. Een `using`-instructie wijst aan het begin een set qubits toe en geeft deze qubits aan het einde van het blok vrij.

## <a name="run-the-code-from-the-command-prompt"></a>De code uitvoeren vanaf de opdracht prompt

Als u de code wilt uitvoeren, moet u aangeven *welke* compiler kan worden uitgevoerd wanneer de opdracht wordt aangeboden `dotnet run` . Dit wordt gedaan met een eenvoudige wijziging in het Q# bestand door een regel toe te voegen die de `@EntryPoint()` aanroepable direct voorafgaat: de `TestBellState` bewerking in dit geval. De volledige code moet zijn:

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

Als u het programma wilt uitvoeren, moet `count` u `initial` argumenten opgeven bij de opdracht prompt. Laten we de voor beelden `count = 1000` kiezen `initial = One` . Voer de volgende opdracht in:

```dotnetcli
dotnet run --count 1000 --initial One
```

En u moet rekening houden met de volgende uitvoer:

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

Als u probeert met `initial = Zero` het volgende te weten:

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a>Superpositie voorbereiden

Laten we nu eens kijken hoe Q# u qubits in superpositie plaatst.  Zoals eerder gezegd, kan de toestand van een qubit een superpositie zijn van 0 en 1.  We gaan de bewerking `Hadamard` gebruiken om dit te bereiken. Als de qubit zich in een van de klassieke toestanden bevindt (waarbij een meting altijd `Zero` of altijd `One` retourneert) wordt de qubit met de bewerking `Hadamard` of `H` in een toestand geplaatst waarin een meting van de qubit in 50% van de gevallen `Zero` retourneert en in 50% van de gevallen `One`.  Conceptueel gezien, kan de qubit worden beschouwd als halverwege tussen de `Zero` en `One`.  Als we nu de bewerking `TestBellState` simuleren, zien we dat de resultaten na meting ongeveer een gelijk aantal keren `Zero` en `One` bevatten.  

### <a name="x-flips-qubit-state"></a>`X` Hiermee wordt de status van Qubit gespiegeld

Eerst proberen we de Qubit te spie gelen (als de Qubit de status heeft, `Zero` wordt deze gespiegeld `One` en omgekeerd). Dit wordt bereikt door een bewerking `X` uit te voeren voordat we de qubit meten in `TestBellState`:

```qsharp
X(qubit);
let res = M(qubit);
```

De resultaten worden nu omgekeerd:

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

Laten we nu de Quantum eigenschappen van de qubits verkennen.

### <a name="h-prepares-superposition"></a>`H` voor bereiding van superpositie

We hoeven alleen maar de bewerking `X` uit het vorige voorbeeld te vervangen door een bewerking `H` of Hadamard. In plaats van de qubit te spiegelen van 0 naar 1, wordt deze slechts half gespiegeld. De vervangen regels in `TestBellState` zien er nu als volgt uit:

```qsharp
H(qubit);
let res = M(qubit);
```

De resultaten worden nu interessanter:

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

Telkens als we meten, vragen we om een klassieke waarde, maar de qubit bevindt zich halverwege tussen 0 en 1, zodat we de helft van de tijd (statistisch) 0 en de helft van de tijd 1 krijgen.
Dit staat bekend als **superpositie** en geeft ons de eerste echte blik op een kwantumtoestand.

## <a name="prepare-entanglement"></a>Verstrengeling voorbereiden

Laten we nu eens kijken hoe Q# u entangle qubits.
Eerst stellen we de eerste qubit in op de begintoestand en gebruiken we vervolgens de bewerking `H` om deze in superpositie te brengen.  Voordat we de eerste Qubit meten, gebruiken we vervolgens een nieuwe bewerking ( `CNOT` ), die staat voor *beheerd* .  Het resultaat van het uitvoeren van deze bewerking op twee qubits is het spie gelen van de tweede Qubit als de eerste Qubit is `One` .  Nu zijn de twee qubits verstrengeld.  Onze statistieken voor de eerste qubit zijn niet gewijzigd (kans van 50% op een `Zero` of `One` na meting), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ de uitkomst die voor de eerste qubit is gemeten. Onze `CNOT`-poort heeft de twee qubits verstrengeld, zodat wat er met de ene gebeurt, ook met de andere gebeurt. Als u de metingen omkeert (de tweede qubit vóór de eerste), zou zich hetzelfde voordoen. De eerste meting zal willekeurig zijn, waarna de tweede zich houdt aan wat voor de eerste is gedetecteerd.

Het eerste wat u moet doen, is twee qubits toewijzen in plaats van één in `TestBellState` :

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

Zo kunnen we een nieuwe bewerking (`CNOT`) toevoegen voordat we een meting (`M`) in `TestBellState` uitvoeren:

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

We hebben nog een andere `SetQubitState`-bewerking toegevoegd om de eerste qubit te initialiseren, zodat we zeker weten dat deze altijd in toestand `Zero` is wanneer we starten.

We moeten ook de tweede qubit opnieuw instellen voordat deze wordt vrijgegeven.

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

De volledige routine ziet er nu als volgt uit:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
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
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

In de nieuwe retourwaarde (`agree`) wordt telkens bijgehouden als de meting van de eerste qubit overeenkomt met de meting van de tweede qubit.

Het uitvoeren van de code die wij verkrijgen:

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

Zoals aangegeven in het overzicht, zijn onze statistieken voor de eerste qubit niet gewijzigd (kans van 50% op 0 of 1), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ dezelfde uitkomst als voor de eerste qubit, omdat ze namelijk verstrengeld zijn.

## <a name="next-steps"></a>Volgende stappen

In de [Zoek opdracht](xref:microsoft.quantum.quickstarts.search) in de zelf studie ziet u hoe u Grover Search kunt bouwen en uitvoeren, een van de meest populaire Quantum Computing-algoritmen en een goed voor beeld van een Q# programma kunt gebruiken dat kan worden gebruikt voor het oplossen van echte problemen met Quantum Computing.  

Aan [de slag met de Quantum Development Kit](xref:microsoft.quantum.welcome) raadt u aan meer manieren te leren Q# en Quantum Program meren.
