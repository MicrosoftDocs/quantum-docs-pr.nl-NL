---
title: 'Q # standaard bibliotheken: karakte Rise ring | Microsoft Docs'
description: 'Q # standaard bibliotheken: karakte Rise ring'
author: QuantumWriter
uid: microsoft.quantum.libraries.characterization
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: d77085aa8aa83c18858056bab1858d990efdb36e
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185559"
---
# <a name="quantum-characterization-and-statistics"></a>Quantum karakte Rise ring en statistieken #

Het is essentieel dat u de gevolgen van bewerkingen kunt kenmerken om nuttige Quantum algoritmen te ontwikkelen.
Dit is lastig omdat elke meting van een Quantum systeem Maxi maal één stukje informatie oplevert.
Als u een eigenvalue wilt leren, kunt u alleen een Quantum status, de resultaten van een groot aantal metingen samen voegen, zodat de gebruiker de vele informatie die nodig is om deze concepten weer te geven, kan beschikken.
De Quantum statussen zijn vooral complexe omdat de [theorema geen](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) enkele manier is om een wille keurige Quantum status te leren kennen uit één exemplaar van de status, omdat u hierdoor kopieën van de status kunt maken.
Deze afspiegeling van de Quantum status van de gebruiker wordt weer gegeven in het feit dat Q # niet beschikbaar is of zelfs definieert wat een staat *is* voor Quantum Program ma's.
We gaan de Quantum karakte Rise ring ook behandelen door bewerkingen en Staten als Black Box uit te dienen. Deze benadering heeft veel gang bare aandelen met de experimentele praktijk van Quantum karakte Rise ring, verificatie en validatie (QCVV).

Karakte Rise ring is verschillend van de vele andere bibliotheken die eerder zijn besproken.
Het doel is hier minder te weten te komen over de klassieke informatie over het systeem, in plaats van een unitary-trans formatie uit te voeren op een status vector.
Deze bibliotheken moeten daarom zowel de klassieke als de Quantum gegevens verwerking overvloeien.


## <a name="iterative-phase-estimation"></a>Schatting van iteratieve fase ##

Het weer geven van Quantum-Program ma's in termen van de Quantum karakte Rise ring stelt een nuttig alternatief voor de Quantum-fase schatting voor.
Dat wil zeggen, in plaats van een $n $-Qubit-REGI ster te maken dat een binaire weer gave van de fase bevat zoals in de Quantum Phase-schatting, kunnen we de fase schatting bekijken als het proces waarmee een *klassieke* agent de eigenschappen van een Quantum systeem leert door meten.
We gaan in de Quantum case door gebruik te maken van Phase kickback om toepassingen van een Black Box-bewerking te scha kelen in draaiingen met een onbekende hoek, maar de ancilla Qubit te meten die we tijdens elke stap direct na de draaiing draaien.
Dit heeft het voor deel dat er slechts één extra Qubit is vereist voor het uitvoeren van de fase kickback die wordt beschreven in de Quantum case, aangezien we de fase van de meet resultaten tijdens elke stap op een iteratieve manier leren.  
Elk van de hieronder voorgestelde methoden gebruikt een andere strategie voor het ontwerpen van experimenten en verschillende methoden voor gegevens verwerking om de fase te leren.  Ze hebben allemaal een uniek voor deel, variërend van het gebruik van strikte fout grenzen, de mogelijkheden voor het opnemen van eerdere informatie, het verdragen van fouten of het uitvoeren van geheugen limitted klassieke computers.

In het bespreken van iteratieve fase-schattingen wordt een unitary-$U $ gegeven als een Black-Box-bewerking.
Zoals beschreven in de sectie over Oracle in [gegevens structuren](xref:microsoft.quantum.libraries.data-structures), kan de Q # Canon dergelijke bewerkingen door het door de <xref:microsoft.quantum.oracles.discreteoracle> door de gebruiker gedefinieerde type gedefinieerd door het type tuple `((Int, Qubit[]) => Unit : Adjoint, Controlled)`.
Als `U : DiscreteOracle`, dan implementeert `U(m)` $U ^ m $ voor `m : Int`.

Bij deze definitie wordt elke stap van een iteratieve fase schatting uitgevoerd door een auxillary-Qubit in de status $ \ket{+} $ voor te bereiden, samen met de aanvankelijke status $ \ket{\phi} $, wordt ervan uitgegaan dat er een [eigenvector](xref:microsoft.quantum.concepts.matrix-advanced) is van $U (m) $, dat wil zeggen $U (m) \ket{\phi} = e ^ {im\phi} \ket{\phi} $.  
Er wordt vervolgens een beheerde toepassing van `U(m)` gebruikt waarbij de status $ \left (R\_1 (m \phi) \ket{+} \right) \ket{\phi} $ wordt voor bereid.
Net als in het Quantum geval is het effect van een beheerde toepassing van de Oracle-`U(m)` precies hetzelfde als het effect van het Toep assen van $R _1 $ voor de onbekende fase op $ \ket{+} $, zodat we de effecten van $U $ op deze eenvoudigere manier kunnen beschrijven.
Zo kunt u met het algoritme het besturings element Qubit draaien door $R _1 (-m\theta) $ toe te passen om een status te verkrijgen $ \ket{\psi} = \left (R\_1 (m [\phi-\theta]) \ket{+} \right) \ket{\phi} $ $.
De auxillary-Qubit die als besturings element voor `U(m)` wordt gebruikt, wordt vervolgens in de $X $-basis gemeten om één klassieke `Result`te verkrijgen.

Op dit moment is het opnieuw samen stellen van de fase van de `Result` waarden die zijn verkregen via een iteratieve fase schatting een klassiek statistisch probleem.
Het vinden van de waarde van $m $ waarmee de opgedane informatie wordt gemaximaliseerd op basis van een vaste methode voor het afwijzen van een afwijzen, is gewoon een probleem met statistieken.
We benadrukken dit door een korte beschrijving te geven van de iteratieve fase schatting op theoretisch niveau in de Bayesiaanse para meter schatting formeelheid voordat u doorgaat met het beschrijven van de statistische algoritmen die zijn opgenomen in de Q # Canon voor het oplossen van deze klassieke interferentie fout.

### <a name="iterative-phase-estimation-without-eigenstates"></a>Schatting van iteratieve fase zonder Eigenstates ###

Als er een invoer status wordt opgegeven die geen eigenstate is, dat wil zeggen dat als $U (m) \ket{\phi\_j} = e ^ {im\phi\_j} $, wordt de Quantum status door het proces van de fase niet-deterministisch omgeleid naar een enkele energie eigenstate.  De eigenstate waarmee deze uiteindelijk wordt geconvergeerd, is de eigenstate die de waargenomen `Result`waarschijnlijk produceert.

In het bijzonder voert één stap van PE de volgende niet-unitary-trans formatie uit voor een status \begin{align} \sum_j \sqrt{\Pr (\phi\_j)} \ket{\phi\_j} \mapsto \sum\_j\frac {\ SQRT {\ PR (\phi\_j)} \sqrt{\Pr (\text{Result} | \ Phi\_j)} \ket{\phi\_j}} {\sqrt{\Pr (\phi\_j) \sum\_j \Pr (\text{Result} | \phi\_j)}}.
\end{align} omdat dit proces wordt herhaald over meerdere `Result` waarden, eigenstates die geen maximale waarden hebben van $ \prod_k\Pr (\text{Result}\_k | \phi\_j) $ wordt exponentieel onderdrukt.
Als gevolg hiervan wordt het debehandelings proces meestal geconvergeerd aan statussen met één eigenvalue als de experimenten goed worden gekozen.

Bayes ' theorema heeft verder gesuggereerd dat de status van de fase schatting wordt geschreven in de vorm \begin{align} \frac{\sqrt{\Pr (\phi\_j)} \sqrt{\Pr (\text{Result} | \phi\_j)} \ket{\phi\_j}} {\sqrt{\Pr (\phi\_j) \sum\_j \Pr (\text{Result} | \phi\_j)}} = \sum_j \sqrt{\Pr (\phi\_j | \text{Result})} \ket{\phi\_j}.
\end{align} hier $ \Pr (\phi\_j | \text{Result}) $ kan interpretted zijn als de waarschijnlijkheid dat de kans op elke hypo these over de eigenstates wordt gegeven:

1. kennis van de Quantum status voordat deze wordt gemeten;
2. kennis van de eigenstates van $U $ en,
3. kennis van de eigenvalues van $U $.

Het leren van deze drie dingen is vaak exponentieel hard op een klassieke computer.
Het hulp programma voor de fase schatting treedt, in geen enkele mate, van het feit dat het een dergelijke Quantum lerende taak kan uitvoeren zonder dat ze daar kennis van hebben.
De fase-schatting voor deze reden wordt weer gegeven in een aantal Quantum algoritmen die exponentiële speedups bieden.

### <a name="bayesian-phase-estimation"></a>Schatting van de Bayesiaanse-fase ###

> [!TIP]
> Zie het [**PhaseEstimation**](https://github.com/Microsoft/Quantum/tree/master/Samples/src/PhaseEstimation) -voor beeld voor meer informatie over de Bayesiaanse-fase schatting in de praktijk.

Het idee van een schatting van de Bayesiaanse-fase is eenvoudig.
U verzamelt meting statistieken vanuit het fase-schattings protocol en vervolgens verwerkt u de resultaten met behulp van Bayesiaanse deinterferentie en geeft u een schatting van de para meter op.
Deze verwerking geeft u een schatting van de eigenvalue en de onzekerheid in die schatting.
U kunt hiermee ook adaptieve experimenten uitvoeren en eerdere gegevens gebruiken.
Het nadeel van de methoden is dat deze reken kracht zwaarder wordt.

Als u wilt weten hoe dit Bayesiaanse wordt gebruikt, kunt u het beste een enkel `Zero` resultaat verwerken.
Houd er rekening mee dat $X = \ket{+} \bra{+}-\ket{-}\bra{-}$, waardoor $ \ket{+} $ de enige positieve eigenstate is van $X $ die overeenkomt met `Zero`.
De waarschijnlijkheid van het observeren van `Zero` voor een [`PauliX` meting](xref:microsoft.quantum.concepts.pauli) op de eerste Qubit op basis van een invoer status $ \ket{\psi}\ket{\phi} $ is \begin{Equation} \Pr (\texttt{Zero} | \psi) = \left | \braket{+ | \psi} \right | ^ 2.
\end{equation} in het geval van een iteratie fase-schatting hebben we dat $ \ket{\psi} = R_1 (m [\phi-\theta]) \ket{+} $, waardoor \begin{align} \Pr (\texttt{Zero} | \phi; m, \theta) & = \left | \braket{+ | R_1 (m [\phi-\theta]) | +} \right | ^ 2 \\\\ & = \left | \frac12 \left (\bra{0} + \bra{1} \right) \left (\ket{0} + e ^ {i m [\phi-\theta]} \ket{1} \right) \right | ^ 2 \\\\ & = \left | \frac{1 + e ^ {i m [\phi-\theta]}}{2} \right | ^ 2 \\\\ & = \cos ^ 2 (m [\phi-\theta]/2) \tag{★} \label{EQ: fase-est-kans}.
\end{align} dat wil zeggen de schatting van de iteratie fase bestaat uit het leren van de trillings frequentie van een sinusoidal-functie, gezien de mogelijkheid om een munt te spie gelen met een afwijking van die sinusoid.
De volgende traditionele klassieke terminologie noemen we $ \eqref{EQ: phase-est-kans.} $ de *waarschijnlijke functie* voor schatting van iteratieve fase.

Nadat u een `Result` hebt waargenomen van de waarschijnlijke functie schatting van iteratieve fase, kunnen we Bayes-regel gebruiken om te bepalen wat de fase ervan moet zijn om deze waarneming te volgen.
Betonief, \begin{Equation} \Pr (\phi | d) = \frac{\Pr (d | \phi) \Pr (\phi)} {\int \Pr (d | \phi) \Pr (\phi) {\mathrm d} \phi} \Pr (\phi), \end{Equation} waarbij $d \in \\{\texttt{Zero}, \texttt{One}\\} $ een `Result`is en waarbij $ \Pr (\phi) $ Hierin wordt onze eerdere opvattingen over $ \phi $ beschreven.
Vervolgens wordt de herhaalde aard van de iteratieve fase schatting expliciet gemaakt, omdat de posterior-distributie $ \Pr (\phi | d) $ de opvattingen onmiddellijk benadert om onze waarneming van de volgende `Result`.

Op elk gewenst moment tijdens deze procedure kunnen we de fase $ \hat{\phi} $, zoals \begin{Equation} \hat{\phi} \mathrel{: =} \expect [\phi | \Text{data}] = \int \phi \Pr (\phi | \Text{data}) {\mathrm d} \phi, \end{Equation}, waarbij $ \ de tekst {data} $ staat voor de gehele record van alle `Result` waarden die zijn verkregen.

De exacte Bayesiaanse-deinterferentie is in de praktijk onbepaald.
Om dit voor stel te zien, willen we een $n $-bit-variabele $x $ leren.
De vorige distributie $ \Pr (x) $ heeft ondersteuning voor meer dan $2 ^ n $ hypothetische waarden van $x $.
Dit betekent dat als er een zeer nauw keurige schatting van $x $, de schatting van de Bayesiaanse-fase mogelijk een verboden geheugen en verwerkings tijd nodig heeft.
Hoewel voor sommige toepassingen, zoals Quantum simulatie, de nauw keurigheid van de limitted niet van toepassing is op andere toepassingen, zoals het algoritme van Shor, kunt u geen gebruik maken van de exacte Bayesiaanse-afleiding binnen de fase-schattings stap.  Daarom bieden we ook implementaties voor het benaderen van Bayesiaanse-methoden, zoals een [wille keurige Walkie fase schatting (RWPE)](xref:microsoft.quantum.research.randomwalkphaseestimation.randomwalkphaseestimation) en ook niet-Bayesiaanse benaderingen zoals een [robuuste fase schatting](xref:microsoft.quantum.characterization.robustphaseestimation).

### <a name="robust-phase-estimation"></a>Robuuste fase schatting ###

Een Bayesiaanse-reconstructie van een fase in het ergste geval is een periode van een schatting van *het aantal meet* resultaten. De meeste praktische schattings algoritmen nemen voor de reconstructie enige kwaliteit mee in de wederopbouw, in ruil voor een hoeveelheid klassieke naverwerking die in plaats daarvan met het aantal gemaakte metingen wordt geschaald.

Een voor beeld van een efficiënte, klassieke, verwerkings stap is het algoritme voor het schatten van de [robuuste fase](https://arxiv.org/abs/1502.02677), met de hand tekening en de invoer hierboven beschreven. Hierbij wordt ervan uitgegaan dat de invoer unitary Black-vakken $U $ worden verpakt als `DiscreteOracle` type en daarom alleen query's op gehele getallen van het bestuurd-$U $ worden uitgevoerd. Als de invoer status in het `Qubit[]` REGI ster een eigenstate is $U \ket{\psi} = e ^ {i\phi} \ Ket {\ psi} $, retourneert het algoritme voor het schatten van de robuuste fase een schatting $ \hat{\phi}\in [-\pi, \pi) $ van $ \phi $ als `Double`.

De belangrijkste functie van een robuuste fase schatting, die wordt gedeeld met de meeste andere nuttige varianten, is dat de reconstructie kwaliteit van $ \hat{\phi} $ in een bepaalde zin Heisenberg-Limited is. Dit betekent dat als de afwijking van $ \hat{\phi} $ van de werkelijke waarde $ \sigma $ is, $ \sigma $ inversisch wordt geschaald in verhouding tot het totale aantal query's $Q $ is gemaakt naar Controlled-$U $, d.w.z. $ \sigma = \mathcal{O} (1/Q) $. Nu is de definitie van afwijking afhankelijk van verschillende schattings algoritmen. In sommige gevallen kan het betekenen dat er ten minste $ \mathcal{O} (1) $ waarschijnlijk is, de schattings fout $ | \hat{\phi}-\phi |\_\circ\le \sigma $ op een van de ronde maat eenheden $ \circ $. Voor een Robust Phase-schatting is de afwijking gelijk aan de variantie $ \sigma ^ 2 = \mathbb{E}\_\hat{\phi} [(\mod\_{2 \ PI} (\hat{\phi}-\phi + \pi)-\pi) ^ 2] $ als de periodieke fasen worden uitgepakt op een enkel eindig interval $ (-\pi, \pi] $. Nauw keuriger is de standaard afwijking in de robuuste fase schatting van de ongelijke waarde $ $ \begin{align} 2,0 \pi/Q \le \sigma \le 2 \ pi/2 ^ {n} \le 10.7 \ Pi/Q, \end{align} $ $ waarbij de ondergrens is bereikt in de grens van de Maxi maal asymptotische grootte $Q $ en de bovenste gebonden is zelfs gegarandeerd voor kleine steek proeven.  Houd er rekening mee dat $n $ geselecteerd door de `bitsPrecision`-invoer, die impliciet $Q $ definieert.

Andere relevante gegevens zijn onder meer de geringe overhead van $1 $ ancilla Qubit, of de procedure is niet-adaptief, wat inhoudt dat de vereiste reeks Quantum experimenten onafhankelijk is van de tussenliggende meet resultaten. In deze en komende voor beelden, waarbij de keuze van het algoritme voor fase schatting belang rijk is, moet één van beide verwijzen naar de documentatie, zoals @"microsoft.quantum.canon.robustphaseestimation", en naar de publicaties waarnaar wordt verwezen voor meer informatie en voor de implementatie ervan.

> [!TIP]
> Er zijn veel voor beelden van het gebruik van robuuste fase schatting. Zie het [ **simulatie** voorbeeld](https://github.com/Microsoft/Quantum/tree/master/Samples/src/H2SimulationCmdLine), het [ **SimpleIsing** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/SimpleIsing)-voor beeld en het [ **Hubbard model** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/HubbardSimulation)-voor beeld, voor een schatting van de fase bij het extra heren van de grond energie van het verschillende fysieke systeem.


### <a name="continuous-oracles"></a>Continue Oracle ###

We kunnen ook generaliseren vanuit het Oracle-model dat hierboven wordt gebruikt om te zorgen voor continue time-Oracle, gemodelleerd door het Canon-type <xref:microsoft.quantum.oracles.continuousoracle>.
Houd er rekening mee dat in plaats van één unitary-operator $U $ een familie van unitary-Opera tors $U (t) $ voor $t \in \mathbb{R} $, $U (t) U (s) $ = $U (t + s) $.
Dit is een zwakkere instructie dan in de afzonderlijke situatie, omdat we een <xref:microsoft.quantum.oracles.discreteoracle> kunnen maken door $t = m\,\delta t $ te beperken voor sommige vaste $ \delta t $.
De [theorema van stenen](https://en.wikipedia.org/wiki/Stone%27s_theorem_on_one-parameter_unitary_groups), $U (t) = \exp (i H t) $ voor een bepaalde operator $H $, waarbij $ \exp $ de matrix exponentiële is, zoals beschreven in [Geavanceerde matrices](xref:microsoft.quantum.concepts.matrix-advanced).
Een eigenstate $ \ket{\phi} $ van $H $ zodanig dat $H \ket{\phi} = \phi \ket{\phi} $ is dan ook een eigenstate van $U (t) $ voor alle $t $, \begin{Equation} U (t) \ket{\phi} = e ^ {i \phi t} \ket{\phi}.
\end{equation}

De nauw keurige analyse die wordt besproken voor de schatting van de [Bayesiaanse fase](#bayesian-phase-estimation) kan worden toegepast en de waarschijnlijke functie is precies hetzelfde als voor dit algemenere Oracle-model: $ $ \Pr (\texttt{Zero} | \phi; t, \theta) = \cos ^ 2 \ Left (\frac{t [\phi-\theta]} @no__ t_1_ \right).
$ $ Bovendien, als $U $ een simulatie is van een dynamische generator, zoals het geval is voor [Hamiltonian-simulatie](xref:microsoft.quantum.libraries.applications#hamiltonian-simulation), interpreteert $ \phi $ als energie.
Met het gebruik van een fase-schatting met doorlopende query's kunnen we het gesimuleerde [Energy-spectrum van moleculen](https://arxiv.org/abs/quant-ph/0604193), [materialen](https://arxiv.org/abs/1510.03859) of [veld theoriesen](https://arxiv.org/abs/1111.3633v2) , zonder dat we de keuze van experimenten moeten doen, omdat $t $ een geheel getal moet zijn.

### <a name="random-walk-phase-estimation"></a>Schatting wille keurige Walkie fase ###

Q # biedt een handige benadering van de schatting van de Bayesiaanse-fase, ontworpen voor het gebruik van close-to-Quantum apparaten.
Deze methode is zowel adaptief als volledig deterministisch, waardoor bijna optimaal kan worden geschaald in de geschatte fase $ \hat{\phi} $ met weinig geheugen overhead.

In het protocol wordt gebruikgemaakt van een geschatte methode voor het afwijzen van Bayesiaanse die ervan uitgaat dat de eerdere distributie Gaussiaans is.
Met deze Gaussiaanse veronderstelling kunnen we een analytische formule voor het experiment gebruiken waarmee de posterior variantie wordt geminimaliseerd.
Op basis van het resultaat van het experiment, verschuift de schatting van $ \phi $ naar links of rechts met een vooraf bepaalde hoeveelheid en wordt de afwijking met een vooraf bepaalde hoeveelheid verkleind.
Dit gemiddelde en deze afwijking geven alle informatie die nodig is voor het opgeven van een Gaussiaans vóór $ \phi $ voor het volgende experiment.
Onverwachte metings fouten of het resultaat van de werkelijke waarde is de staart van de eerste, kan ervoor zorgen dat deze methode mislukt.
Er wordt van uitgegaan van een fout door experimenten uit te voeren om te testen of het huidige gemiddelde en de standaard afwijking geschikt zijn voor het systeem.
Als dat niet het geval is, voert het algoritme een omgekeerde stap van de Walk uit en wordt het proces voortgezet.
Met de mogelijkheid om achterwaarts op te stappen, kan de algoritme ook worden achterhaald, zelfs als de initiële voor gaande standaard afwijking inapropriately klein is.

## <a name="calling-phase-estimation-algorithms"></a>Algoritmen voor fase schatting aanroepen ##

Elke fase-schattings bewerking die is opgegeven met Q # Canon, neemt een andere set invoer parameterizing de kwaliteit op die we nodig hebben voor de laatste schatting $ \hat{\phi} $.
Deze verschillende invoer, maar alle gemeen schappelijke invoer delen, zoals een gedeeltelijke toepassing die de kwaliteits parameters overschrijdt, resulteert in een algemene hand tekening.
De <xref:microsoft.quantum.characterization.robustphaseestimation> bewerking die in de volgende sectie wordt besproken, heeft bijvoorbeeld de volgende hand tekening:

```qsharp
operation RobustPhaseEstimation(bitsPrecision : Int, oracle : DiscreteOracle, eigenstate : Qubit[])  : Double
```

De `bitsPrecision` invoer is uniek voor `RobustPhaseEstimation`, terwijl `oracle` en `eigenstate` gemeen schappelijk zijn.
Zo kan een bewerking, zoals gezien in **H2Sample**, een iteratieve fase schattings algoritme accepteren met een invoer van het formulier `(DiscreteOracle, Qubit[]) => Unit` zodat een gebruiker wille keurige fase schattings algoritmen kan opgeven:

```qsharp
operation H2EstimateEnergy(
    idxBondLength : Int, 
    trotterStepSize : Double,
    phaseEstAlgorithm : ((DiscreteOracle, Qubit[]) => Double)) 
: Double
```

Deze talloze fase schattings algoritmen zijn geoptimaliseerd voor verschillende eigenschappen en invoer parameters, die moeten worden begrepen om de beste keuze voor de doel toepassing te maken. Zo zijn sommige fase schattings algoritmen adaptief, wat betekent dat toekomstige stappen klassiek worden beheerd door de meet resultaten van de vorige stappen. In sommige gevallen is het de mogelijkheid om de exponentiate van de Black Box unitary Oracle door wille keurige echte bevoegdheden te laten opdoen, en andere hebben alleen geheeltallige bevoegdheden nodig, maar kunnen alleen een fase schatting modulo $2 \ Pi $ omzetten. Enkele vereisen veel auxillary-qubits en andere vereisen er slechts één.

Op dezelfde manier wordt de schatting van de wille keurige Walk-fase op ongeveer dezelfde wijze uitgevoerd als voor andere algoritmen die bij de Canon worden gebruikt:

```qsharp
operation ExampleOracle(eigenphase : Double, time : Double, register : Qubit[]) : Unit
is Adj + Ctl {
    Rz(2.0 * eigenphase * time, register[0]);
}

operation BayesianPhaseEstimationCanonSample(eigenphase : Double) : Double {

    let oracle = ContinuousOracle(ExampleOracle(eigenphase, _, _));
    using (eigenstate = Qubit()) {
        X(eigenstate);
        // The additional inputs here specify the mean and variance of the prior, the number of
        // iterations to perform, how many iterations to perform as a maximum, and how many
        // steps to roll back on an approximation failure.
        let est = RandomWalkPhaseEstimation(0.0, 1.0, 61, 100000, 1, oracle, [eigenstate]);
        Reset(eigenstate);
        return est;
    }
}
```
