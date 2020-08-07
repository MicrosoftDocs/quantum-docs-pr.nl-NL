---
title: Program ma's op Qubit-niveau schrijven en simuleren inQ#
description: Stapsgewijze zelf studie voor het schrijven en simuleren van een Quantum programma dat op het individuele Qubit niveau werkt
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
no-loc:
- Q#
- $$v
ms.openlocfilehash: 22c79e4e01db1a0d0c291d0dcff81dbfa8df5cd3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869712"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a>Zelf studie: Program ma's op Qubit schrijven en simuleren in Q\#

Welkom bij de Quantum Development Kit-zelf studie over het schrijven en simuleren van een eenvoudig Quantum programma dat wordt uitgevoerd op afzonderlijke qubits. 

Hoewel Q# primair is gemaakt als een programmeer taal op hoog niveau voor grootschalige Quantum Program ma's, kan deze net zo eenvoudig worden gebruikt voor het verkennen van het lagere niveau van Quantum Program ma's: rechtstreeks adresseren van specifieke qubits.
Dankzij de flexibiliteit van Q# kunnen gebruikers een Quantum systeem van een dergelijk abstractie niveau benaderen, en in deze zelf studie gaan we in op de qubits zelf.
In het bijzonder kijken we naar de schermen van de [Quantum-Fourier-trans formatie](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), een subroutine die integraal is aan veel grotere Quantum algoritmen.

Houd er rekening mee dat deze weer gave op laag niveau van Quantum gegevens verwerking vaak wordt beschreven in termen van '[Quantum circuits](xref:microsoft.quantum.concepts.circuits)', die de sequentiële toepassing van poorten voor specifieke qubits van een systeem vertegenwoordigen.

Daarom kunnen de single-en multi-Qubit-bewerkingen die we opeenvolgend Toep assen, gemakkelijk worden weer gegeven in een circuit diagram.
In ons geval definieert Q# u een bewerking voor het uitvoeren van de volledige Qubit Quantum-Fourier-trans formatie, die de volgende representatie als een circuit heeft:

<br/>
<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a>Vereisten

* [Installeer](xref:microsoft.quantum.install) de Quantum Development Kit met uw voorkeurs taal en-ontwikkelings omgeving.
* Als u de QDK al hebt geïnstalleerd, controleert u of uw versie is [bijgewerkt](xref:microsoft.quantum.update) naar de nieuwste versie


## <a name="in-this-tutorial-youll-learn-how-to"></a>In deze zelfstudie leert u het volgende:

> [!div class="checklist"]
> * Quantum bewerkingen definiëren inQ#
> * Q#Bewerkingen rechtstreeks aanroepen vanaf de opdracht regel of met behulp van een klassiek host-programma
> * Een Quantum bewerking simuleren vanuit Qubit-toewijzing naar meting uitvoer
> * Bekijk hoe de gesimuleerde Wavefunction van het Quantum systeem tijdens de bewerking wordt ontwikkeld

Het uitvoeren van een Quantum programma met de Quantum Development Kit van micro soft bestaat meestal uit twee delen:
1. Het programma zelf, dat wordt geïmplementeerd met behulp van de Q# Quantum programmeer taal en vervolgens wordt aangeroepen om te worden uitgevoerd op een quantum computer of Quantum Simulator. Deze bestaan uit 
    - Q#bewerkingen: subroutines die optreden op Quantum registers en 
    - Q#functions: klassieke subroutines die worden gebruikt binnen het Quantum algoritme.
2. Het ingangs punt dat wordt gebruikt om het Quantum programma aan te roepen en de doel computer op te geven waarop het moet worden uitgevoerd.
    U kunt dit rechtstreeks doen via de opdracht regel of via een hostprogramma dat is geschreven in een klassieke programmeer taal, zoals python of C#.
    Deze zelf studie bevat instructies voor de methode die u wilt gebruiken.

## <a name="allocate-qubits-and-define-quantum-operations"></a>Qubits toewijzen en Quantum bewerkingen definiëren

Het eerste deel van deze zelf studie bestaat uit het definiëren van de Q# bewerking `Perform3qubitQFT` , waarmee de Quantum Fourier-trans formatie op drie qubits wordt uitgevoerd. 

Daarnaast gebruiken we de [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) functie om te zien hoe de gesimuleerde Wavefunction van ons drie Qubit systeem zich in de hele bewerking ontwikkelt.

De eerste stap is het Q# project en het bestand maken.
De stappen hiervoor zijn afhankelijk van de omgeving die u gebruikt om het programma aan te roepen, en u kunt de details vinden in de respectieve [installatie handleidingen](xref:microsoft.quantum.install).

De onderdelen van het bestand worden stapsgewijs door lopen, maar de code is ook beschikbaar als een volledige blok kering.

### <a name="namespaces-to-access-other-no-locq-operations"></a>Naam ruimten voor toegang tot andere Q# bewerkingen
In het bestand definieert u eerst de naam ruimte `NamespaceQFT` die wordt gebruikt door de compiler.
Voor de bewerking om gebruik te maken van bestaande Q# bewerkingen opent u de relevante `Microsoft.Quantum.<>` naam ruimten.

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a>Bewerkingen met argumenten definiëren en retour neren
Vervolgens definieert u de `Perform3qubitQFT` bewerking:

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

De bewerking heeft nu geen argumenten en retourneert niets---in dit geval schrijven we dat er een object wordt geretourneerd dat in `Unit` `void` C# of een lege tuple `Tuple[()]` in python is Akin.
Later gaan we deze wijzigen om een matrix met meet resultaten te retour neren, waarop het punt `Unit` wordt vervangen door `Result[]` . 

### <a name="allocate-qubits-with-using"></a>Qubits toewijzen aan`using`
In onze Q# bewerking wijzen we eerst een REGI ster van drie qubits toe met de `using` instructie:

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

Met `using` worden automatisch de qubits toegewezen in de status $ \ket {0} $. We kunnen dit controleren door te gebruiken [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) en [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , waarmee een teken reeks en de huidige status van het systeem naar de-console worden afgedrukt.

> [!NOTE]
> De `Message(<string>)` `DumpMachine()` functies en (van [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) en [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) ) worden beide rechtstreeks naar de console afgedrukt. Net als bij een echte Quantum berekening, staat Q# ons niet toe direct toegang te krijgen tot Qubit Staten.
> Als `DumpMachine` de huidige status van de doel computer afdrukt, kan dit echter waardevol inzicht geven in het gebruik van fouten in combi natie met de volledige status Simulator.


### <a name="applying-single-qubit-and-controlled-gates"></a>Single-Qubit en beheerde poorten Toep assen

Daarna passen we de Gates toe die de bewerking zelf vormen.
Q#bevat al veel eenvoudige Quantum poorten als bewerkingen in de [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) naam ruimte, en dit is geen uitzonde ring. 

Binnen een Q# bewerking worden de instructies die callables aanroepen, in sequentiële volg orde uitgevoerd.
Daarom is de eerste poort die moet worden toegepast, de [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) voor de eerste Qubit:

<br/>
<img src="../media/qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

Als u een bewerking wilt Toep assen op een specifieke Qubit van een REGI ster (dat wil zeggen een enkele `Qubit` van een matrix `Qubit[]` ), gebruiken we standaard index notatie.
Het Toep assen [`H`](xref:microsoft.quantum.intrinsic.h) van de op de eerste Qubit van de kassa `qs` heeft dus de volgende vorm:

```qsharp
            H(qs[0]);
```

Naast het Toep assen van de `H` (Hadamard)-poort op afzonderlijke qubits, bestaat het QFT-circuit voornamelijk uit beheerde [`R1`](xref:microsoft.quantum.intrinsic.r1) draaiingen.
Een `R1(θ, <qubit>)` bewerking in het algemeen laat het onderdeel $ \ket {0} $ van de Qubit ongewijzigd. tijdens het Toep assen van een rotatie van $e ^ {i\theta} $ naar het onderdeel $ \ket {1} $.

#### <a name="controlled-operations"></a>Beheerde bewerkingen

Q#maakt het zeer eenvoudig om een bewerking uit te voeren op een of meer besturings qubits.
Over het algemeen hebben we alleen de oproep met en `Controlled` de bewerkings argumenten gewijzigd als:

 `Op(<normal args>)`$ \to $ `Controlled Op([<control qubits>], (<normal args>))` .

Houd er rekening mee dat het besturings element qubits moet worden ingesteld als een matrix, zelfs als het een enkele Qubit is.

Na de hebben `H` we zien dat de volgende Gates de `R1` poorten op de eerste Qubit zijn (en beheerd door de tweede/derde):

<br/>
<img src="../media/qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

We noemen deze met

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

Houd er rekening mee dat we de [`PI()`](xref:microsoft.quantum.math.pi) functie van de [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) naam ruimte gebruiken om de rotaties in termen van pi radialen te definiëren.
Daarnaast delen we door een `Double` (bijvoorbeeld), `2.0` omdat het delen door een geheel getal `2` een type fout genereert. 

> [!TIP]
> `R1(π/2)`en `R1(π/4)` zijn gelijk aan de- `S` en- `T` bewerkingen (ook in `Microsoft.Quantum.Intrinsic` ).


Na het Toep assen van de relevante `H` bewerkingen en de beheerde draaiingen naar de tweede en derde qubits:

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

We hoeven alleen een [`SWAP`](xref:microsoft.quantum.intrinsic.swap) Gate toe te passen om het circuit te volt ooien:

```qsharp
            SWAP(qs[2], qs[0]);
```

Dit is nodig omdat de aard van de Quantum Fourier-trans formatie de qubits in omgekeerde volg orde uitvoert, zodat de wissels een naadloze integratie van de subroutine tot grotere algoritmen mogelijk maakt.

Daarom is het schrijven van de Qubit van de Quantum Fourier-trans formatie in onze Q# bewerking voltooid:

<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

We kunnen de service echter nog maar een dag aanroepen.
Onze qubits stond in de status $ \ket {0} $ toen we ze hebben toegewezen, en in het geval van leven, moeten we op Q# dezelfde manier op dezelfde wijze worden gevonden als we ze hebben aangetroffen (of beter!).

### <a name="deallocate-qubits"></a>Toewijzing qubits ongedaan maken

We bellen [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) opnieuw om de status na bewerking weer te geven en zijn [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) van toepassing op het Qubit-REGI ster om de qubits opnieuw in te stellen op $ \ket {0} $ voordat u de bewerking voltooit:

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

Als u wilt dat alle niet-toegewezen qubits expliciet worden ingesteld op $ \ket {0} $ is een basis functie van Q# , omdat het mogelijk is dat andere bewerkingen hun status nauw keurig kennen wanneer ze dezelfde qubits (een schaarse resource) gaan gebruiken.
Bovendien zorgt dit ervoor dat ze niet Entangled zijn met andere qubits in het systeem.
Als het opnieuw instellen niet wordt uitgevoerd aan het einde van een `using` toewijzings blok, wordt een runtime-fout gegenereerd.

Het volledige Q# bestand moet er nu als volgt uitzien:

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


Het Q# bestand en de bewerking zijn voltooid, maar ons Quantum programma kan worden aangeroepen en gesimuleerd.

## <a name="execute-the-program"></a>Het programma uitvoeren

Q#Als u de bewerking in een `.qs` bestand hebt gedefinieerd, moet u deze bewerking nu aanroepen en de geretourneerde klassieke gegevens bekijken.
Er wordt nu niets geretourneerd (intrekken dat de hierboven gedefinieerde bewerking is geretourneerd `Unit` ), maar wanneer we de bewerking later wijzigen Q# om een matrix met meet resultaten te retour neren ( `Result[]` ), zullen we dit aanpakken.

Terwijl het Q# programma wordt alomtegenwoordige in de omgevingen die worden gebruikt om het te aanroepen, is de manier waarop u dit kunt doen, afhankelijk van elkaar. Volg de instructies in het tabblad dat overeenkomt met uw installatie: werken vanuit de Q# opdracht regel toepassing of een host-programma in Python of C#.

#### <a name="command-line"></a>[Opdrachtregel](#tab/tabid-cmdline)

Voor het uitvoeren Q# van het programma vanaf de opdracht regel is slechts een kleine wijziging in het Q# bestand vereist.

Voeg simpelweg toe `@EntryPoint()` aan een regel voor de bewerkings definitie:

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

Als u het programma wilt uitvoeren, opent u de terminal in de map van het project en voert u

```dotnetcli
dotnet run
```

Na de uitvoering ziet u de `Message` onderstaande en `DumpMachine` afgedrukte uitvoer in uw-console.


#### <a name="python"></a>[Python](#tab/tabid-python)

Een python-hostbestand maken: `host.py` .

Het hostbestand is als volgt samengesteld: 
1. Eerst importeren we de `qsharp` module, die de module lader registreert voor Q# interoperabiliteit. 
    Op deze manier kunnen Q# naam ruimten (zoals de `NamespaceQFT` in ons Q# bestand gedefinieerde) worden weer gegeven als python-modules, waaruit we bewerkingen kunnen importeren Q# .
2. Importeer vervolgens de Q# bewerkingen die in dit geval direct---worden aangeroepen `Perform3qubitQFT` .
    We hoeven het toegangs punt alleen in een programma te importeren Q# (dat wil zeggen _geen_ bewerkingen zoals `H` en `R1` , die worden aangeroepen door andere Q# bewerkingen, maar nooit door de klassieke host).
3. In het simuleren van Q# bewerkingen of functies gebruikt u het formulier `<Q#callable>.simulate(<args>)` om ze op de doel computer uit te voeren `QuantumSimulator()` . 

> [!NOTE]
> Als we de bewerking willen aanroepen op een andere computer, bijvoorbeeld de `ResourceEstimator()` , zou u gewoon gebruiken `<Q#callable>.estimate_resources(<args>)` .
> Q#Over het algemeen worden de bewerkingen uitgevoerd op de computers waarop ze zijn gestart, maar sommige functies, zoals `DumpMachine` mogelijk, kunnen zich anders gedragen.

4. Bij het uitvoeren van de simulatie retourneert de bewerkings aanroep waarden die zijn gedefinieerd in het Q# bestand.
    Er wordt op dit moment niets geretourneerd, maar er wordt later een voor beeld weer gegeven van het toewijzen en verwerken van deze waarden.
    Met de resulterende gegevens in onze handen en volledig klassiek kunnen we alles doen wat we graag doen.

Het volledige `host.py` bestand moet dit zijn:

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

Voer het python-bestand uit en druk af in uw-console. Hieronder ziet u de `Message` onderstaande en- `DumpMachine` uitvoer. 


#### <a name="c"></a>[C#](#tab/tabid-csharp)

Volg de instructies in de [installatie handleiding](xref:microsoft.quantum.install.cs)om een C#-hostbestand te maken en de naam ervan te wijzigen in `host.cs` .

De C#-host heeft vier onderdelen:
1. Bouw een kwantumsimulator.
    In de onderstaande code is dit de variabele `qsim` .
2. Bereken de argumenten die vereist zijn voor het kwantumalgoritme.
    Er zijn geen in dit voor beeld.
3. Voer het kwantumalgoritme uit. 
    Elke Q# bewerking genereert een C#-klasse met dezelfde naam. 
    Deze klasse heeft een methode `Run` die de bewerking **asynchroon** uitvoert.
    De uitvoering is asynchroon, omdat de uitvoering op feitelijke hardware asynchroon is. 
    Omdat de `Run` methode asynchroon is, wordt de `Wait()` methode aangeroepen. Hiermee wordt de uitvoering geblokkeerd totdat de taak is voltooid en het resultaat synchroon wordt geretourneerd. 
4. Het geretourneerde resultaat van de bewerking verwerken.
    Voor nu retourneert de bewerking niets.


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
Voer de toepassing uit en de uitvoer moet overeenkomen met die hieronder.
Het programma wordt afgesloten nadat u op een toets hebt gedrukt.
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

Wanneer de Full-State Simulator wordt aangeroepen, `DumpMachine()` biedt deze Multiple-representaties van de Wavefunction van de Quantum status. De mogelijke statussen van een $n $-Qubit-systeem kunnen worden voorgesteld door $2 ^ n $ Computation-basis statussen, elk met een bijbehorende complexe coëfficiënt (gewoon een amplitude en een fase).
De reken kundige basis statussen komen overeen met alle mogelijke binaire teken reeksen van de lengte $n $---dat wil zeggen alle mogelijke combi Naties van Qubit Staten $ \ket {0} $ en $ \ket {1} $, waarbij elk binair cijfer overeenkomt met een afzonderlijke Qubit.

De eerste rij bevat een opmerking met de Id's van de bijbehorende qubits in hun significante volg orde.
Qubit is `2` de ' meest significante ' betekent dat u in de binaire weer gave van basis status vector $ \ket{i} $ de status Qubit `2` overeenkomt met het meest linkse cijfer. Bijvoorbeeld: $ \ket {6} = \ket {110} $ omvat qubits `2` en `1` beide in $ \ket {1} $ en Qubit `0` in $ \ket {0} $.


De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{i} $ in zowel Cartesisch als polaire indeling.
Gedetailleerd voor de eerste rij van de invoer status $ \ket {000} $:
* **`|0>:`** deze rij komt overeen met de verwerkings `0` status van de berekening (op voor hand dat onze initiële status post-Allocation $ \ket {000} $ is. dit wordt verwacht dat dit de enige status met een waarschijnlijkheids amplitude op dit punt is).
* **`1.000000 +  0.000000 i`**: de waarschijnlijke amplitude in Cartesisch formaat.
* **` == `**: het `equal` teken scheidt beide equivalente verklaringen.
* **`********************`**: Een grafische weer gave van de omvang, het aantal `*` is evenredig met de kans dat deze status vector wordt gemeten. 
* **`[ 1.000000 ]`**: de numerieke waarde van de grootte
* **`    ---`**: Een grafische weer gave van de fase van de amplitude.
* **`[ 0.0000 rad ]`**: de numerieke waarde van de fase (in radialen).

Zowel de grootte als de fase worden weer gegeven met een grafische weer gave. De weer gave met de grootte is eenvoudig: er wordt een balk van weer gegeven `*` , en hoe hoger de kans, hoe groter de balk is. Zie voor de fase [testen en fout opsporing: dump functies](xref:microsoft.quantum.guide.testingdebugging#dump-functions) voor de mogelijke symbool representaties op basis van een hoek bereik.


De gedrukte uitvoer illustreert dus dat onze geprogrammeerde Gates onze staat hebben getransformeerd van

$ $ \ket{\psi} \_ {begin} = \ket {000} $ $

in 

$ $ \begin{align} \ket{\psi} \_ {Final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $

Dit is precies het gedrag van de 3-qubite Fourier-trans formatie. 

Als u wilt weten hoe andere invoer Staten worden beïnvloed, raden we u aan om te spelen met het Toep assen van Qubit-bewerkingen vóór de trans formatie.

## <a name="adding-measurements"></a>Metingen toevoegen

Helaas vertelt een hoek steen van Quantum monteurs dat een echt Quantum systeem een dergelijke functie niet kan hebben `DumpMachine` . In plaats daarvan worden gegevens geëxtraheerd door middel van metingen, wat in het algemeen niet alleen de volledige Quantum status biedt, maar kan het systeem zelf ook drastisch wijzigen.
Er zijn veel sorteringen van Quantum metingen, maar we richten ons op het meest Basic: uitstekende metingen op één qubits.
Bij meting in een gegeven (bijvoorbeeld de berekening van de verrekenings wijze $ \{ \ket {0} , \ket {1} \} $), wordt de status van het Qubit geprojecteerd op basis van de geschatte status, hetgeen wordt gemeten---, waardoor een wille keurige positie tussen de twee wordt vernietigd.

Als u metingen binnen een Q# programma wilt implementeren, gebruiken we de `M` bewerking (uit `Microsoft.Quantum.Intrinsic` ), die een `Result` type retourneert.

Eerst wijzigen we onze `Perform3QubitQFT` bewerking om een matrix met meet resultaten te retour neren, `Result[]` in plaats van `Unit` .

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a>Matrix definiëren en initialiseren `Result[]`

Voordat u qubits (bijvoorbeeld vóór de instructie) toewijst `using` , declareren en verbindt u deze lengte-3 matrix (één `Result` voor elke qubit): 

```qsharp
        mutable resultArray = new Result[3];
```

`mutable`Met het tref woord `resultArray` wordt de variabele naar een later tijdstip in de code---afhankelijk van het toevoegen van onze meet resultaten.

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a>Metingen uitvoeren in een `for` lus en resultaten toevoegen aan een matrix

Na de Fourier-transformatie bewerkingen binnen het `using` blok voert u de volgende code in:

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
De [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) functie die wordt aangeroepen in een matrix (bijvoorbeeld onze matrix van qubits `qs` ) retourneert een bereik over de indices van de matrix. Hier gebruiken we dit in onze `for` lus om elke qubit achtereenvolgens te meten met behulp van de- `M(qs[i])` instructie.
Elk gemeten `Result` type ( `Zero` of `One` ) wordt vervolgens toegevoegd aan de bijbehorende index positie in `resultArray` met een update-en-reassign-instructie.

> [!NOTE]
> De syntaxis van deze instructie is uniek voor Q# , maar komt overeen met de nieuwe hertoewijzing van een variabele die `resultArray[i] <- M(qs[i])` in andere talen wordt weer gegeven, zoals F # en R.

Het sleutel woord `set` wordt altijd gebruikt voor het opnieuw toewijzen van variabelen die zijn gekoppeld met `mutable` .

#### <a name="return-resultarray"></a>Opvragen`resultArray`

Met alle drie qubits gemeten en de resultaten die worden toegevoegd aan `resultArray` , kunnen we de qubits als voorheen opnieuw instellen en de toewijzing ervan ongedaan maken.
Invoegen nadat de `using` blok kering is gesloten

```qsharp
        return resultArray;
```
uiteindelijk de uitvoer van de bewerking te retour neren. 

### <a name="understanding-the-effects-of-measurement"></a>Meer informatie over de gevolgen van meting

Laten we de plaatsing van onze `DumpMachine` functies wijzigen zodat de status wordt uitgevoerd vóór en na de metingen.
De uiteindelijke bewerkings code moet er als volgt uitzien: 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

Als u vanaf de opdracht regel werkt, wordt de geretourneerde matrix gewoon direct naar de console afgedrukt aan het einde van de uitvoering.
Werk anders uw host-programma bij om de geretourneerde matrix te verwerken.

#### <a name="command-line"></a>[Opdrachtregel](#tab/tabid-cmdline)

Om meer te weten te komen over de geretourneerde matrix die in de-console zal worden afgedrukt, kunnen we een andere `Message` in het bestand invoegen, Q# net vóór de `return` instructie:

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

Voer het project uit en de uitvoer moet er ongeveer als volgt uitzien:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[Python](#tab/tabid-python)

Werk uw python-programma bij naar het volgende:

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

Voer het bestand uit en de uitvoer moet er ongeveer als volgt uitzien:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

Nu de bewerking een resultaat retourneert, vervangt u de methode aanroep door `Wait()` de eigenschap op te halen `Result` . Dit heeft nog steeds hetzelfde Synchronicity dat eerder is besproken en we kunnen deze waarde rechtstreeks aan de variabele binden `measurementResult` .

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

Voer het project uit en de uitvoer moet er ongeveer als volgt uitzien:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

In deze uitvoer ziet u een aantal verschillende dingen:
1. Als vergelijking van het geretourneerde resultaat naar de voor meting `DumpMachine` , illustreert het duidelijk _niet_ de post-QFT-positie boven basis status.
    Een meting retourneert slechts één basis status, met een waarschijnlijkheid die is bepaald door de amplitude van die staat in de Wavefunction van het systeem.
2. Vanuit de post-meting `DumpMachine` zien we dat de status zelf wordt _gewijzigd_ en dat deze wordt geprojecteerd van de oorspronkelijke superpositie in de basis status en de enkelvoudige basis staat die overeenkomt met de gemeten waarde.

Als we deze bewerking meermaals moeten herhalen, zien we dat de resultaat statistieken beginnen met de gelijkmatig gewogen superpositie van de post-QFT-status, die resulteert in een wille keurig resultaat op elke afbeelding.
Afgezien van inefficiënte en nog niet-perfecte, zou dit _echter_toch alleen de relatieve amplitudes van de basis status, niet de relatieve fasen ertussen, reproduceren.
In dit voor beeld is dit geen probleem, maar we zien dat relatieve fasen worden weer gegeven als een complexere invoer wordt gegeven aan de QFT dan $ \ket {000} $.

#### <a name="partial-measurements"></a>Gedeeltelijke metingen 
Als u wilt weten hoe alleen bepaalde qubits van de kassa van invloed kunnen zijn op de status van het systeem, voegt u het volgende toe in de `for` lus, na de meet lijn:
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

Houd er rekening mee dat `IntAsString` u toegang hebt tot de functie die u moet toevoegen 
```qsharp
    open Microsoft.Quantum.Convert;
```
met de rest van de naam ruimte- `open` instructies.

In de resulterende uitvoer ziet u de geleidelijke projectie in subruimten wanneer elke qubit wordt gemeten.


## <a name="use-the-no-locq-libraries"></a>De Q# bibliotheken gebruiken
Zoals in de inleiding werd vermeld, is veel van de kracht van de Q# stroom in het voor deel dat u de zorgen over van het verwerken van afzonderlijke qubits kunt samen stellen.
Als u de juiste, toepasselijke Quantum Program ma's wilt ontwikkelen, moet u er wel voor zorgen dat een bewerking wordt uitgevoerd `H` vóór of na een bepaalde rotatie. 

De Q# bibliotheken bevatten de [QFT](xref:microsoft.quantum.canon.qft) -bewerking, die u gewoon kunt uitvoeren en Toep assen voor een wille keurig aantal qubits.
Om het een try-out te geven, definieert u een nieuwe bewerking in het Q# bestand met dezelfde inhoud `Perform3QubitQFT` , maar met alles van de eerste `H` tot de `SWAP` vervangen door twee eenvoudige lijnen:
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
De eerste regel maakt simpelweg een [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expressie van de toegewezen matrix van qubits, `qs` die de [QFT](xref:microsoft.quantum.canon.qft) -bewerking als argument gebruikt.
Dit komt overeen met de index volgorde van de qubits in het REGI ster.

Als u toegang wilt hebben tot deze bewerkingen, voegt u `open` instructies toe voor de bijbehorende naam ruimten aan het begin van het Q# bestand:
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

Pas nu uw hostprogramma aan om de naam van uw nieuwe bewerking aan te roepen (bijvoorbeeld `PerformIntrinsicQFT` ) en geef het een uitproberen.

Als u het werkelijke voor deel van het gebruik van de Q# bibliotheek bewerkingen wilt zien, wijzigt u het aantal qubits in een andere waarde dan `3` :
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
U kunt de juiste QFT voor elk gegeven aantal qubits Toep assen, zonder dat u zich zorgen hoeft te maken over de rommel van nieuwe `H` bewerkingen en draaiingen op elke qubit.

Houd er rekening mee dat de Quantum Simulator meer tijd in beslag neemt, omdat u het aantal qubits nauw keuriger kunt verg Roten---om precies te kijken wat er gebeurt.













