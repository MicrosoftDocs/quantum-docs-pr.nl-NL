---
title: 'Diagnostische gegevens in de standaard bibliotheken van Q #'
description: "Meer informatie over de diagnostische functies en bewerkingen in de standaard bibliotheken van Q # die worden gebruikt om fouten of fouten in Quantum Program ma's te ondervangen."
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: ba2f248327bb3db4ee895f8e65ea31c17e42b5f4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906233"
---
# <a name="diagnostics"></a>Diagnostiek #

Net als bij de klassieke ontwikkeling is het belang rijk om fouten en fouten in Quantum Program ma's te kunnen onderzoeken.
De standaard bibliotheken van Q # bieden verschillende manieren om de juistheid van Quantum Program ma's, zoals beschreven in <xref:microsoft.quantum.techniques.testing-and-debugging>, te garanderen.
In het algemeen is deze ondersteuning beschikbaar in de vorm van functies en bewerkingen waarmee de doel computer aanvullende diagnostische gegevens kan leveren aan het hostprogramma of de ontwikkelaar, of die de juistheid van voor waarden en varianten afdwingt door de functie-of bewerkings aanroep.

## <a name="machine-diagnostics"></a>Machine diagnostiek ##

Diagnostische gegevens over klassieke waarden kunnen worden verkregen met behulp van de functie <xref:microsoft.quantum.intrinsic.message> om een bericht op een computer afhankelijke manier te registreren.
Standaard schrijft de teken reeks naar de-console.
<xref:microsoft.quantum.intrinsic.message> wordt gebruikt in combi natie met geïnterpoleerde teken reeksen en maakt het eenvoudig om diagnostische gegevens over klassieke waarden te rapporteren:

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> `Message` heeft hand tekening `(String -> Unit)`, wat aangeeft dat een logboek bestand voor fout opsporing niet kan worden waargenomen vanuit Q #.

De <xref:microsoft.quantum.diagnostics.dumpmachine>-en <xref:microsoft.quantum.diagnostics.dumpregister> callables instrueren doel machines om diagnostische gegevens te verstrekken over alle momenteel toegewezen qubits of over een specifiek REGI ster van qubits.
Elke doel computer is afhankelijk van de diagnostische gegevens die worden verstrekt in reactie op een dump instructie.
De [Fully](xref:microsoft.quantum.machines.full-state-simulator) machine-doel computer, bijvoorbeeld, levert het hostprogramma met de status vector die intern wordt gebruikt om een REGI ster van qubits te vertegenwoordigen.
Ter vergelijking: de doel computer van de [Toffoli Simulator](xref:microsoft.quantum.machines.toffoli-simulator) biedt één klassieke bit voor elke qubit.

 Zie de sectie dump functies van het [artikel testen en fout opsporing](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions)voor meer informatie over de `DumpMachine` uitvoer van de [volledige status Simulator](xref:microsoft.quantum.machines.full-state-simulator) .


## <a name="facts-and-assertions"></a>Feiten en verklaringen ##

Zoals beschreven in [testen en fout opsporing](xref:microsoft.quantum.techniques.testing-and-debugging), kan een functie of bewerking met hand tekening `Unit -> Unit` of `Unit => Unit`, respectievelijk als een *eenheids test*worden gemarkeerd.
Elke eenheids test bestaat doorgaans uit een klein Quantum programma, samen met een of meer voor waarden die de juistheid van het programma controleren.
Deze voor waarden kunnen worden opgenomen in de vorm van _feiten_, die de waarden van hun invoer (of _beweringen_) controleren, die de statussen controleren van een of meer qubits die worden door gegeven als invoer.

`EqualityFactI(1 + 1, 2, "1 + 1 != 2")` bijvoorbeeld staat voor het mathematische feit dat $1 + 1 = $2, terwijl `AssertQubit(One, qubit)` de voor waarde vertegenwoordigt waarmee `qubit` een `One` retourneert met zekerheid.
In het eerste geval kunnen we controleren of de voor waarde juist is gegeven, maar in de laatste gevallen moeten we iets weten over de status van de Qubit om de bewering te kunnen evalueren.

De standaard bibliotheken van Q # bieden verschillende functies voor het weer geven van feiten, waaronder:

- <xref:microsoft.quantum.diagnostics.fact>
- <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact>
- <xref:microsoft.quantum.diagnostics.nearequalityfactc>
- <xref:microsoft.quantum.diagnostics.equalityfacti>


### <a name="testing-qubit-states"></a>Qubit-statussen testen ###

In de praktijk zijn de beweringen afhankelijk van het feit dat klassieke simulaties van Quantum-garages de [theorema zonder klonen](https://arxiv.org/abs/quant-ph/9607018)niet hoeven te volgen, zodat we fysieke metingen en beweringen kunnen maken wanneer ze een simulator voor onze doel computer gebruiken.
Daarom kunnen we afzonderlijke bewerkingen op een klassieke Simulator testen voordat ze op hardware worden geïmplementeerd.
Op doel computers die geen bevestigingen kunnen evalueren, kunnen aanroepen naar <xref:microsoft.quantum.intrinsic.assert> veilig worden genegeerd.

Meer in het algemeen, de <xref:microsoft.quantum.intrinsic.assert> bewerking beweringen dat het opgegeven qubits in het opgegeven Pauli-basis punt altijd het gegeven resultaat heeft.
Als de verklaring mislukt, wordt de uitvoering beëindigd door `fail` aan te roepen met het opgegeven bericht.
Deze bewerking is standaard niet geïmplementeerd. Simulatoren die IT kunnen ondersteunen, moeten een implementatie bieden die runtime-controle uitvoert.
`Assert` heeft hand tekening `((Pauli[], Qubit[], Result, String) -> ())`.
Omdat `Assert` is een functie met een lege tuple als uitvoer type, zijn er geen effecten van het aanroepen van `Assert` waarneembaar binnen een Q #-programma.

De functie voor <xref:microsoft.quantum.intrinsic.assertprob> bewerkings functies beweringen dat het opgegeven qubits in de gegeven Pauli basis het gegeven resultaat krijgt met de opgegeven kans, binnen een aantal toleranties.
Tolerantie is additief (bijvoorbeeld `abs(expected-actual) < tol`).
Als de verklaring mislukt, wordt de uitvoering beëindigd door `fail` aan te roepen met het opgegeven bericht.
Deze bewerking is standaard niet geïmplementeerd. Simulatoren die IT kunnen ondersteunen, moeten een implementatie bieden die runtime-controle uitvoert.
`AssertProb` heeft hand tekening `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)`. De eerste van `Double` para meters geeft de gewenste kans op het resultaat en de tweede tolerantie.

We kunnen meer dan één meting uitvoeren, met behulp van de klassieke informatie die door een simulator wordt gebruikt om de interne status van een Qubit weer te geven. zo is het niet nodig om een meting uit te voeren om onze bewering te testen.
In het bijzonder kan dit redenen hebben om *incompatibele* metingen die niet mogelijk zijn op werkelijke hardware.

Stel dat `P : Qubit => Unit` een bewerking is die is bedoeld om de status $ \ket{\psi} $ voor te bereiden wanneer de invoer de status $ \ket{0}$ heeft.
Laat $ \ket{\psi '} $ de werkelijke status voor bereid door `P`.
$ \Ket{\psi} = \ket{\psi '} $ If en alleen als de meting $ \ket{\psi '} $ in de as die wordt beschreven door $ \ket{\psi} $ altijd `Zero`retourneert.
Dat wil zeggen, \begin{align} \ket{\psi} = \ket{\psi '} \Text{als en alleen if} \braket{\psi | \psi '} = 1.
\end{align} met behulp van de primitieve bewerkingen die zijn gedefinieerd in de prelude, kunnen we rechtstreeks een meting uitvoeren die `Zero` retourneert als $ \ket{\psi} $ een eigenstate is van een van de Pauli-Opera tors.


De bewerking <xref:microsoft.quantum.diagnostics.assertqubit> biedt een bijzonder nuttige steno om dit te doen in het geval dat we de bewering $ \ket{\psi} = \ket{0}$ willen testen.
Dit is bijvoorbeeld gebruikelijk wanneer we niet zijn berekend om ancilla qubits te retour neren naar $ \ket{0}$ voordat ze worden vrijgegeven.
Het bevestigen van $ \ket{0}$ is ook nuttig wanneer u wilt voor komen dat twee status voorbereidings `P` en `Q` bewerkingen zowel de status voor bereid hebben als `Q` `Adjoint`ondersteunt.
Met name

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

Meer in het algemeen is er echter geen toegang tot beweringen over staten die niet samen vallen met eigenstates van Pauli-Opera tors.
Bijvoorbeeld: $ \ket{\psi} = (\ket{0} + e ^ {i \pi/8} \ket{1})/\sqrt{2}$ is geen eigenstate van een Pauli-operator, zodat we <xref:microsoft.quantum.intrinsic.assertprob> niet kunnen gebruiken om op unieke wijze te bepalen of een status $ \ket{\psi '} $ gelijk is aan $ \ket{\psi} $.
In plaats daarvan moeten we de Assertion $ \ket{\psi} = \ket{\psi} $ afbreken in veronderstellingen die rechtstreeks kunnen worden getest met behulp van de primitieven die door onze Simulator worden ondersteund.
Als u dit wilt doen, laat u $ \ket{\psi} = \alpha \ket{0} + \beta \ket{1}$ voor complexe getallen $ \alpha = a\_r + a\_i $ en $ \beta $.
Houd er rekening mee dat deze expressie vier reële cijfers $\{een\_r, een\_i, b\_r, b\_ik\}$ moet opgeven, omdat elk complex getal kan worden uitgedrukt als de som van een reëel en imaginair deel.
Als gevolg van de globale fase kunnen we echter kiezen $a\_i = $0, zodat we slechts drie echte cijfers nodig hebben om een afzonderlijke Qubit-status op te geven.

Daarom moeten we drie beweringen opgeven die onafhankelijk van elkaar zijn, om de status te bevestigen die we verwachten.
We doen dit door de kans te vinden dat `Zero` wordt geobserveerd voor elke Pauli meting op $ \alpha $ en $ \beta $, en elk afzonderlijk te bevestigen.
Laat $x $, $y $, en $z $ `Result` waarden voor Pauli $X $, $Y $ en $Z $-metingen.
Vervolgens gebruikt u de functie kans voor Quantum metingen, \begin{align} \Pr (x = \texttt{Zero} | \alpha, \beta) & = \frac12 + a\_r b\_r + a\_i b\_ik \\\\ \Pr (y = \texttt{Zero} | \alpha, \beta) & = \frac12 + a\_r b\_i-a\_i b\_r \\\\ \Pr (z = \texttt{Zero} | \alpha, \beta) & = \frac12\left (1 + a\_r ^ 2 + a\_i ^ 2 + b\_r ^ 2 + b\_i ^ 2 \right).
\end{align}

Met de <xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance>-bewerking worden deze verklaringen geïmplementeerd met de representaties van $ \alpha $ en $ \beta $ als waarden van het type <xref:microsoft.quantum.math.complex>.
Dit is handig wanneer de verwachte status wiskundig kan worden berekend.

### <a name="asserting-equality-of-quantum-operations"></a>Gelijkheid van Quantum bewerkingen bevestigen ###

Tot nu toe hebben we de tests uitgevoerd die bedoeld zijn om bepaalde staten voor te bereiden.
Vaak is het echter belang rijk dat een bewerking wordt uitgevoerd voor wille keurige invoer in plaats van voor één vaste invoer.
Stel dat we een bewerking hebben geïmplementeerd `U : ((Double, Qubit[]) => () : Adjoint)` die overeenkomt met een familie van unitary-Opera tors $U (t) $ en een expliciet `adjoint` blok hebben gegeven in plaats van `adjoint auto`te gebruiken.
We zijn mogelijk geïnteresseerd in het bevestigen dat $U ^ \dagger (t) = U (-t) $, zoals verwacht als $t $ een ontwikkelings tijd vertegenwoordigt.

Breed gepaard gesp roken zijn er twee verschillende strategieën die we kunnen volgen bij het maken van de bewering dat twee bewerkingen `U` en `V` identiek handelen.
Eerst kunnen we controleren of `U(target); (Adjoint V)(target);` elke status in een bepaalde basis behoudt.
Ten tweede kunnen we controleren dat `U(target); (Adjoint V)(target);` op de helft van een Entangled-status, die entanglement behouden.
Deze strategieën worden respectievelijk geïmplementeerd door de Canon Operations <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> en <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced>.

> [!NOTE]
> De benaderende bevestigingen die hierboven worden beschreven, zijn gebaseerd op de [Choi – Jamiłkowski isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality), een wiskundig Framework waarmee de bewerkingen op $n $ qubits worden gekoppeld aan Entangled Staten op $2n $ qubits.
> Met name de identiteits bewerking op $n $ qubits wordt vertegenwoordigd door $n $ copies van de Entangled-status $ \ket{\ beta_{00}} \mathrel{: =} (\ket{00} + \ket{11})/\sqrt{2}$.
> Met de bewerking <xref:microsoft.quantum.preparation.preparechoistate> deze isomorphism geïmplementeerd, waarbij een status wordt voor bereid die een bepaalde bewerking vertegenwoordigt.

Deze strategieën worden ongeveer onderscheiden door een tijd-spatie balans.
Door elke invoer status te herhalen, neemt extra tijd in beslag, terwijl entanglement wordt gebruikt als referentie voor het opslaan van extra qubits.
In gevallen waarin een bewerking een omkeer bare klassieke bewerking implementeert, zodat we alleen geïnteresseerd zijn in het gedrag van reken kundige statussen, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> tests op basis van deze beperkte serie invoer testen.

> [!TIP]
> De iteratie over invoer statussen wordt verwerkt door de inventarisatie bewerkingen <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> en <xref:microsoft.quantum.canon.iteratethroughcartesianpower>.
> Deze bewerkingen zijn in het algemeen nuttiger voor het Toep assen van een bewerking op elk element van het Cartesisch product tussen twee of meer sets.

Het is belang rijker dat de twee benaderingen echter verschillende eigenschappen testen van de bewerkingen die worden onderzocht.
Omdat de in-place bewering elke bewerking meerdere keren aanroept, kunnen wille keurige keuzes en meet resultaten worden gewijzigd tussen aanroepen, één keer per invoer status.
Daarentegen wordt elke bewerking exact één keer aangeroepen, zodat er wordt gecontroleerd of de bewerkingen *in één opname*gelijk zijn.
Beide tests zijn handig om de juistheid van Quantum Program ma's te garanderen.


## <a name="further-reading"></a>Meer lezen ##

- <xref:microsoft.quantum.techniques.testing-and-debugging>
- <xref:microsoft.quantum.diagnostics>
