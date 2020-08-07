---
title: Diagnostische gegevens in de Q# standaard bibliotheken
description: Meer informatie over de diagnostische functies en bewerkingen in de Q# standaard bibliotheken die worden gebruikt om fouten of fouten in Quantum Programma's te ondervangen.
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4a98795b2459adaa4e47c888751121fffdc70971
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868539"
---
# <a name="diagnostics"></a>Diagnostiek #

Net als bij de klassieke ontwikkeling is het belang rijk om fouten en fouten in Quantum Program ma's te kunnen onderzoeken.
De Q# standaard bibliotheken bieden verschillende manieren om de juistheid van Quantum Program ma's, zoals beschreven in, te garanderen <xref:microsoft.quantum.guide.testingdebugging> .
In het algemeen is deze ondersteuning beschikbaar in de vorm van functies en bewerkingen waarmee de doel computer aanvullende diagnostische gegevens kan leveren aan het hostprogramma of de ontwikkelaar, of die de juistheid van voor waarden en varianten afdwingt, uitgedrukt door de functie of de bewerkings aanroep.

## <a name="machine-diagnostics"></a>Machine diagnostiek ##

Diagnostische gegevens over klassieke waarden kunnen worden verkregen met behulp van de <xref:microsoft.quantum.intrinsic.message> functie om een bericht op een computer afhankelijke manier te registreren.
Standaard schrijft de teken reeks naar de-console.
Wordt gebruikt in combi natie met geïnterpoleerde teken reeksen en <xref:microsoft.quantum.intrinsic.message> maakt het eenvoudig om diagnostische gegevens over klassieke waarden te rapporteren:

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> `Message`een hand tekening heeft `(String -> Unit)` die opnieuw aangeeft dat een logboek bestand voor fout opsporing niet in acht kan worden genomen Q# .

De <xref:microsoft.quantum.diagnostics.dumpmachine> en <xref:microsoft.quantum.diagnostics.dumpregister> callables instrueren doel machines om diagnostische gegevens te verstrekken over alle momenteel toegewezen qubits of over een specifiek REGI ster van qubits.
Elke doel computer is afhankelijk van de diagnostische gegevens die worden verstrekt in reactie op een dump instructie.
De [Fully](xref:microsoft.quantum.machines.full-state-simulator) machine-doel computer, bijvoorbeeld, levert het hostprogramma met de status vector die intern wordt gebruikt om een REGI ster van qubits te vertegenwoordigen.
Ter vergelijking: de doel computer van de [Toffoli Simulator](xref:microsoft.quantum.machines.toffoli-simulator) biedt één klassieke bit voor elke qubit.

 [full state simulator's](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` Zie de sectie dump functies van het [artikel testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging#dump-functions)voor meer informatie over de volledige uitvoer van de status van de Simulator.


## <a name="facts-and-assertions"></a>Feiten en verklaringen ##

Zoals beschreven in [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging), een functie of bewerking met hand tekening `Unit -> Unit` of `Unit => Unit` respectievelijk kan worden gemarkeerd als een *eenheids test*.
Elke eenheids test bestaat doorgaans uit een klein Quantum programma, samen met een of meer voor waarden die de juistheid van het programma controleren.
Deze voor waarden kunnen worden opgenomen in de vorm van _feiten_, die de waarden van hun invoer (of _beweringen_) controleren, die de statussen controleren van een of meer qubits die worden door gegeven als invoer.

`EqualityFactI(1 + 1, 2, "1 + 1 != 2")`Geeft bijvoorbeeld het mathematische feit weer dat $1 + 1 = $2, terwijl `AssertQubit(One, qubit)` de voor waarde vertegenwoordigt die het meten `qubit` `One` van een met zekerheid retourneert.
In het eerste geval kunnen we controleren of de voor waarde juist is gegeven, maar in de laatste gevallen moeten we iets weten over de status van de Qubit om de bewering te kunnen evalueren.

De Q# standaard bibliotheken bieden verschillende functies voor het weer geven van feiten, waaronder:

- <xref:microsoft.quantum.diagnostics.fact>
- <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact>
- <xref:microsoft.quantum.diagnostics.nearequalityfactc>
- <xref:microsoft.quantum.diagnostics.equalityfacti>


### <a name="testing-qubit-states"></a>Qubit-statussen testen ###

In de praktijk zijn de beweringen afhankelijk van het feit dat klassieke simulaties van Quantum-garages de [theorema zonder klonen](https://arxiv.org/abs/quant-ph/9607018)niet hoeven te volgen, zodat we fysieke metingen en beweringen kunnen maken wanneer ze een simulator voor onze doel computer gebruiken.
Daarom kunnen we afzonderlijke bewerkingen op een klassieke Simulator testen voordat ze op hardware worden geïmplementeerd.
Op doel computers die geen bevestigingen kunnen evalueren, kunnen aanroepen naar <xref:microsoft.quantum.diagnostics.assertmeasurement> veilig worden genegeerd.

Meer in het algemeen is de <xref:microsoft.quantum.diagnostics.assertmeasurement> bewerkings verklaring dat de opgegeven qubits in de gegeven Pauli gebaseerd altijd het gegeven resultaat heeft.
Als de verklaring mislukt, wordt de uitvoering beëindigd door aan te roepen `fail` met het opgegeven bericht.
Deze bewerking is standaard niet geïmplementeerd. Simulatoren die IT kunnen ondersteunen, moeten een implementatie bieden die runtime-controle uitvoert.
`AssertMeasurement`heeft hand tekening `((Pauli[], Qubit[], Result, String) -> ())` .
Omdat `AssertMeasurement` een functie met een lege tuple als uitvoer type is, kan geen effect van het aangeroepen `AssertMeasurement` worden gezien in een Q# programma.

De <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> bewerkings functie beweringen die het opgegeven qubits in de gegeven Pauli-basis meten, hebben het gegeven resultaat met de opgegeven kans, binnen enkele tolerantie.
Tolerantie is additief (bijvoorbeeld `abs(expected-actual) < tol` ).
Als de verklaring mislukt, wordt de uitvoering beëindigd door aan te roepen `fail` met het opgegeven bericht.
Deze bewerking is standaard niet geïmplementeerd. Simulatoren die IT kunnen ondersteunen, moeten een implementatie bieden die runtime-controle uitvoert.
`AssertMeasurementProbability`heeft hand tekening `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)` . De eerste van de `Double` para meters geeft de gewenste kans op het resultaat en de tweede tolerantie.

We kunnen meer dan één meting uitvoeren, met behulp van de klassieke informatie die door een simulator wordt gebruikt om de interne status van een Qubit weer te geven. zo is het niet nodig om een meting uit te voeren om onze bewering te testen.
In het bijzonder kan dit redenen hebben om *incompatibele* metingen die niet mogelijk zijn op werkelijke hardware.

Stel dat `P : Qubit => Unit` een bewerking is bedoeld om de status $ \ket{\psi} $ voor te bereiden wanneer de invoer de status $ \ket {0} $ heeft.
Laat $ \ket{\psi '} $ de werkelijke status voor bereid door `P` .
$ \Ket{\psi} = \ket{\psi '} $ If en alleen als ' $ \ket{\psi '} $ wordt gemeten in de as die wordt beschreven door $ \ket{\psi} $ altijd retourneert `Zero` .
Dat wil zeggen, \begin{align} \ket{\psi} = \ket{\psi '} \Text{als en alleen if} \braket{\psi | \psi '} = 1.
\end{align} met behulp van de primitieve bewerkingen die zijn gedefinieerd in de prelude, kunnen we rechtstreeks een meting uitvoeren die wordt geretourneerd `Zero` als $ \ket{\psi} $ een eigenstate is van een van de Pauli-Opera tors.


De bewerking <xref:microsoft.quantum.diagnostics.assertqubit> biedt een bijzonder nuttige steno om dit te doen in het geval dat we de bewering $ \ket{\psi} = \ket $ willen testen {0} .
Dit is bijvoorbeeld gebruikelijk wanneer we niet zijn berekend om ancilla qubits te retour neren naar $ \ket {0} $ voordat ze worden vrijgegeven.
Het bevestigen van $ \ket {0} $ is ook handig wanneer u wilt voor komen dat twee status voorbereidingen `P` en `Q` -bewerkingen dezelfde status voor bereid hebben en wanneer deze worden `Q` ondersteund `Adjoint` .
Met name

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

Meer in het algemeen is er echter geen toegang tot beweringen over staten die niet samen vallen met eigenstates van Pauli-Opera tors.
Bijvoorbeeld: $ \ket{\psi} = (\ket {0} + e ^ {\pi/8} \ket {1} )/\sqrt {2} $ is geen Eigenstate van een Pauli-operator, zodat we niet kunnen gebruiken om te <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> bepalen of een status $ \ket{\psi '} $ gelijk is aan $ \ket{\psi} $.
In plaats daarvan moeten we de Assertion $ \ket{\psi} = \ket{\psi} $ afbreken in veronderstellingen die rechtstreeks kunnen worden getest met behulp van de primitieven die door onze Simulator worden ondersteund.
Als u dit wilt doen, laat u $ \ket{\psi} = \alpha \ket {0} + \beta \ket {1} $ voor complexe getallen $ \alpha = a \_ r + a \_ i $ en $ \beta $.
Houd er rekening mee dat deze expressie vier echte cijfers $ \{ a \_ r, a \_ i, b \_ r, b \_ i $ vereist om op te \} geven, aangezien elk complex getal kan worden uitgedrukt als de som van een reëel en imaginair deel.
Als gevolg van de globale fase kunnen we echter kiezen $a \_ i = $0, zodat we slechts drie echte cijfers nodig hebben om een unieke status van één Qubit op te geven.

Daarom moeten we drie beweringen opgeven die onafhankelijk van elkaar zijn, om de status te bevestigen die we verwachten.
We doen dit door de kans te vinden dat wordt geobserveerd `Zero` voor elke Pauli meting op $ \alpha $ en $ \beta $, en elk afzonderlijk te bevestigen.
Laat $x $, $y $ en $z $ waarden hebben `Result` voor Pauli $X $, $Y $ en respectievelijk $Z $-metingen.
Vervolgens gebruikt u de functie kans voor Quantum metingen, \begin{align} \Pr (x = \texttt{Zero} | \alpha, \beta) & = \frac12 + a \_ r b \_ r + a \_ i b \_ i \\ \\ \Pr (y = \texttt{Zero} | \alpha, \beta) & = \frac12 + a \_ r b \_ i-a \_ i b \_ r \\ \\ \Pr (z = \texttt{Zero} | \alpha, \beta) & = \frac12\left (1 + a \_ r ^ 2 + \_ \_ b \_ i ^ 2 \right).
\end{align}

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance>Met de bewerking worden deze verklaringen geïmplementeerd met de opgegeven representaties van $ \alpha $ en $ \beta $ als waarden van het type <xref:microsoft.quantum.math.complex> .
Dit is handig wanneer de verwachte status wiskundig kan worden berekend.

### <a name="asserting-equality-of-quantum-operations"></a>Gelijkheid van Quantum bewerkingen bevestigen ###

Tot nu toe hebben we de tests uitgevoerd die bedoeld zijn om bepaalde staten voor te bereiden.
Vaak is het echter belang rijk dat een bewerking wordt uitgevoerd voor wille keurige invoer in plaats van voor één vaste invoer.
Stel dat we een bewerking hebben geïmplementeerd `U : ((Double, Qubit[]) => () : Adjoint)` die overeenkomt met een familie van unitary-Opera tors $U (t) $ en een expliciet blok heeft gegeven `adjoint` in plaats van met `adjoint auto` .
We zijn mogelijk geïnteresseerd in het bevestigen dat $U ^ \dagger (t) = U (-t) $, zoals verwacht als $t $ een ontwikkelings tijd vertegenwoordigt.

Breed gepaard gesp roken zijn er twee verschillende strategieën die we kunnen volgen bij het maken van de bevestiging dat twee bewerkingen `U` en op `V` identieke wijze handelen.
Eerst kunnen we controleren dat `U(target); (Adjoint V)(target);` elke provincie in een bepaalde basis blijft behouden.
Ten tweede kunnen we controleren of `U(target); (Adjoint V)(target);` op de helft van een Entangled-status het entanglement wordt behouden.
Deze strategieën worden geïmplementeerd door de Canon <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> -bewerkingen en <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced> , respectievelijk.

> [!NOTE]
> De benaderende bevestigingen die hierboven worden beschreven, zijn gebaseerd op de [Choi – Jamiłkowski isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality), een wiskundig Framework waarmee de bewerkingen op $n $ qubits worden gekoppeld aan Entangled Staten op $2n $ qubits.
> Met name de identiteits bewerking op $n $ qubits wordt vertegenwoordigd door $n $ copies van de Entangled-status $ \ket{\ beta_ {00} } \mathrel{: =} (\ket {00} + \ket {11} )/\sqrt {2} $.
> Met <xref:microsoft.quantum.preparation.preparechoistate> deze bewerking wordt deze isomorphism geïmplementeerd, waarbij een status wordt voor bereid die een bepaalde bewerking vertegenwoordigt.

Deze strategieën worden ongeveer onderscheiden door een tijd-spatie balans.
Door elke invoer status te herhalen, neemt extra tijd in beslag, terwijl entanglement wordt gebruikt als referentie voor het opslaan van extra qubits.
In gevallen waarin een bewerking een omkeerbaar klassieke bewerking implementeert, zodat we alleen geïnteresseerd zijn in het gedrag van reken kundige statussen, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> testen de gelijkheid op deze beperkte set invoer.

> [!TIP]
> De iteratie over de invoer status wordt verwerkt door de inventarisatie bewerkingen <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> en <xref:microsoft.quantum.canon.iteratethroughcartesianpower> .
> Deze bewerkingen zijn in het algemeen nuttiger voor het Toep assen van een bewerking op elk element van het Cartesisch product tussen twee of meer sets.

Het is belang rijker dat de twee benaderingen echter verschillende eigenschappen testen van de bewerkingen die worden onderzocht.
Omdat de in-place bewering elke bewerking meerdere keren aanroept, kunnen wille keurige keuzes en meet resultaten worden gewijzigd tussen aanroepen, één keer per invoer status.
Daarentegen wordt elke bewerking exact één keer aangeroepen, zodat er wordt gecontroleerd of de bewerkingen *in één opname*gelijk zijn.
Beide tests zijn handig om de juistheid van Quantum Program ma's te garanderen.


## <a name="further-reading"></a>Meer informatie ##

- <xref:microsoft.quantum.guide.testingdebugging>
- <xref:microsoft.quantum.diagnostics>
