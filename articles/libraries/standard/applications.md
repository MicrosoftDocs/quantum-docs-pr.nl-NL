---
title: 'V # standaard bibliotheken-toepassingen | Microsoft Docs'
description: 'Q # standaard bibliotheken'
author: QuantumWriter
uid: microsoft.quantum.libraries.applications
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: e6eca45dd67b3566340c2a2a4fded0f6e7c3c5c3
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185168"
---
# <a name="applications"></a>Applicaties #

## <a name="hamiltonian-simulation"></a>Hamiltonian simulatie ##

De simulatie van Quantum systemen is een van de meest interessante toepassingen van Quantum berekeningen.
Op een klassieke computer, de moeite van het simuleren van Quantum-garages, in het algemeen, wordt geschaald met de dimensie $N $ van de weer gave van de status vector.
Aangezien deze weer gave exponentieel toeneemt met het aantal $n $ qubits $N = 2 ^ n $, een Trait die ook wel bekend staat als de term [dimensionaliteit](xref:microsoft.quantum.concepts.multiple-qubits), kan de Quantum simulatie op klassieke hardware ongemoeid zijn.

De situatie kan echter zeer verschillen op Quantum hardware. De meest voorkomende variatie van de Quantum simulatie wordt het tijd onafhankelijke Hamiltonian simulatie probleem genoemd. Er wordt een beschrijving gegeven van het systeem Hamiltonian $H $, een Hermitian-matrix en een initiële Quantum status $ \ket{\psi (0)} $ die in een bepaalde basis is gecodeerd op $n $ qubits op een quantum computer. Als Quantum statussen in gesloten systemen ontwikkelen onder de Schrödinger-vergelijking $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = H \ket{\psi (t)}, \end{align} $ $ het doel is om de unitary time-evolutie operator te implementeren $U (t) = e ^ {-iHt} $ op een bepaalde vaste tijd $t $ , waarbij $ \ket{\psi (t)} = U (t) \ket{\psi (0)} $ de vergelijking van Schrödinger opgelost.
Vergelijkbaar met het tijdgebonden Hamiltonian simulatie probleem wordt dezelfde vergelijking opgelost, maar met $H (t) $ nu een functie van tijd.

Hamiltonian simulatie is een belang rijk onderdeel van vele andere Quantum simulatie problemen en oplossingen voor het simulatie probleem van Hamiltonian zijn algoritmen die een reeks primitieve Quantum-Gates beschrijven voor het maken van een unitary $ \tilde{U} $ met de fout $\\| \tilde{U}-U (t)\\| \le \epsilon $ in de [Spectral-norm](xref:microsoft.quantum.concepts.matrix-advanced). De complexiteit van deze algoritmen is sterk afhankelijk van de manier waarop een quantum computer toegang heeft tot een beschrijving van de Hamiltonian van de interesses. Als $H $ op $n $ qubits moet worden aangeboden als een lijst met $2 ^ n \times 2 ^ n $ cijfers, één voor elk matrix element, zou de gegevens echter al exponentiële tijd nodig hebben, bijvoorbeeld in het ergste geval. In het beste geval kan een van de voor keur uitgaan van de toegang tot een Black Box-unitary die $O \ket{t}\ket{\psi (0)} = \ket{t}U (t) \ket{\psi (0)} $ het probleem op een pase manier oplost. Geen van deze invoer modellen is bijzonder interessant, omdat het niet beter is dan klassieke benaderingen, en de laatste als zwarte doos de primitieve poort complexiteit van de implementatie verbergen. Dit kan exponentieel zijn in het aantal qubits.

### <a name="descriptions-of-hamiltonians"></a>Beschrijvingen van Hamiltonians ###

Aanvullende veronderstellingen van de indeling van de invoer zijn daarom vereist. Er moet een nauw keurige balans zijn tussen invoer modellen die voldoende beschrijvend zijn om interessante Hamiltonians te omvatten, zoals die voor realistische fysieke systemen of interessante verwerkings problemen, en invoer modellen die voldoende beperkend zijn efficiënt te implementeren op een quantum computer. Er is mogelijk een verscheidenheid aan niet-trivial invoer model gevonden in de literatuur en het bereik is van Quantum tot klassiek. 

Als voor beelden van Quantum invoer modellen, wordt in de [Hamiltonian-simulatie op basis](http://www.nature.com/articles/s41534-017-0013-7) van een voor beeld uitgegaan van Black-Box-toegang tot Quantum bewerkingen die kopieën van een dichtheids matrix $ \rho $ maken, die de Hamiltonian $H $ zijn. In het [unitary-toegangs model](https://arxiv.org/abs/1202.5822) wordt ervan uitgegaan dat de Hamiltonian in plaats daarvan wordt opgeteld in een som van unitaries $ $ \begin{align} H & = \sum ^ {d-1}\_{j = 0} a\_j \hat{U}\_j, \end{align} $ $ waar $a\_j > 0 $ coëfficiënten zijn en $ \hat{U}\_j $ zijn unitaries. Er wordt van uitgegaan dat één Black-Box-toegang heeft tot de unitary Oracle $V = \sum ^ {d-1}\_{j = 0} \ket{j}\bra{j}\otimes \hat{U}\_j $ waarmee de gewenste $ \hat{U}-\_j $ wordt geselecteerd en de Oracle $A \ket{0}= \sum ^ {d-1}\_{ j = 0} \sqrt{a\_j/\ Sum ^ {d-1}\_{k = 0} \alpha\_j} \ket{j} $ waarmee een Quantum status wordt gemaakt, zijn deze coëfficiënten. In het geval van een [sparse Hamiltoniane-simulatie](https://arxiv.org/abs/quant-ph/0301023)wordt ervan uitgegaan dat de Hamiltonian een Sparse matrix is met alleen $d = \mathcal{O} (\Text{polylog} (N)) $ niet-nul-element in elke rij. Daarnaast wordt ervan uitgegaan dat het bestaan van efficiënte Quantum circuits die de locatie van deze niet-nul elementen, en de waarden ervan, worden uitgevoerd. De complexiteit van [Hamiltonian-simulatie algoritmen](xref:microsoft.quantum.more-information) wordt geëvalueerd in termen van het aantal query's naar deze zwarte vakjes en de primitieve poort complexiteit is dan afhankelijk van de moeilijkheids graad van de implementatie van deze zwarte vakken.

> [!NOTE]
> De Big-O-notatie wordt meestal gebruikt voor het beschrijven van de complexiteits schaal van algoritmen. Als er twee echte functies $f, g $, de expressie $g (x) = \mathcal{O} (f (x)) $ betekent dat er een absolute positieve constante is $x\_0, c > 0 $ zodanig dat $g (x) \le c f (x) $ voor alle $x \ge x\_$0. 

In de meeste praktische toepassingen die op een quantum computer moeten worden geïmplementeerd, moeten deze zwarte vakken efficiënt kunnen worden geïmplementeerd, dat wil zeggen met $ \mathcal{O} (\Text{polylog} (N)) $ primitieve Quantum-poorten. Een sterkere, efficiëntere simulable Hamiltonians moet een voldoende sparse klassieke beschrijving hebben. In een dergelijke formulering wordt ervan uitgegaan dat de Hamiltonian een samen stelling van een som van Hermitian-onderdelen $ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} H_j.
\end{align} $ $ er wordt van uitgegaan dat elk deel, een Hamiltonian $H\_j $, gemakkelijk te simuleren is. Dit betekent dat de unitary $e ^ {-iH\_j t} $ voor elke tijd $t $ kan worden geïmplementeerd met $ \mathcal{O} (1) $ primitieve Quantum Gates. Dit geldt bijvoorbeeld in het speciale geval waarbij elke $H\_j $ lokale Pauli-Opera Tors is, wat inhoudt dat ze van tensor-producten van $ \mathcal{O} (1) $ niet-identiteits Pauli Opera tors die op ruimtelijke dichte qubits handelen. Dit model is met name van toepassing op fysieke systemen met een begrensde en lokale interactie, omdat het aantal voor waarden is $d = \mathcal{O} (\Text{polylog} (N)) $ en mogelijk duidelijk kan worden geschreven, d.w.z. in een polynoom.

> [!TIP]
> Hamiltonians die in een som van delen afbreken, kunnen worden beschreven met behulp van de Dynamical Generator representatie bibliotheek. Zie de sectie weer gave van dynamische generator in [gegevens structuren](xref:microsoft.quantum.libraries.data-structures)voor meer informatie.

### <a name="simulation-algorithms"></a>Simulatie algoritmen ###

Een Quantum simulatie algoritme zet een opgegeven beschrijving van een Hamiltonian om in een reeks primitieve Quantum-poorten die als geheel een tijdige evolutie van Hamiltonian.

In het speciale geval waarbij de Hamiltonian wordt ontsteld in een som van Hermitian-onderdelen, is de Trotter-Suzuki-ontleding een bijzonder eenvoudig en intuïtief algoritme voor het simuleren van Hamiltonians die een som van Hermitian onderdelen afbreken. Een first-order integrator van deze familie heeft bijvoorbeeld ongeveer $ $ \begin{align} U (t) & = \left (e ^ {-iH\_0 t/r} e ^ {-iH\_1 t/r} \cdots e ^ {-iH\_{d-1} t/r} \right) ^ {r} + \mathcal{O} (d ^ 2 \max_j\\| H\_j\\| ^ 2 t ^ 2/r), \end{align} $ $ met behulp van een product van $r d $-voor waarden. 

> [!TIP]
> Toepassingen van het simulatie algoritme Trotter-Suzuki worden in de voor beelden besproken.
> Zie het [ **SimpleIsing** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/SimpleIsing)-voor beeld voor het Ising-model met alleen de intrinsieke bewerkingen van elke doel computer.
> Raadpleeg het [ **IsingTrotter** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/IsingTrotterEvolution)-voor beeld voor het Ising-model met behulp van de Trotter-Suzuki.
> Zie het [ **simulatie** voorbeeld](https://github.com/Microsoft/Quantum/tree/master/Samples/src/H2SimulationCmdLine)van de Trotter-Suzuki voor moleculaire water stof met behulp van de beheer structuur van de bibliotheek.

In veel gevallen willen we het simulatie algoritme implementeren, maar zijn ze niet geïnteresseerd in de details van de implementatie. Bijvoorbeeld, de tweede order integrator benadert $ $ \begin{align} U (t) & = \left (e ^ {-iH\_0 t/2R} e ^ {-iH\_1 t/2R} \cdots e ^ {-iH\_{d-1} t/2R} e ^ {-iH\_{d-1}} t/2R} \cdots e ^ {-iH\_1 t/2R} e ^ {- iH\_0 t/2R} \right) ^ {r} + \mathcal{O} (d ^ 3 \max_j\\| H\_j\\| ^ 3 t ^ 3/r ^ 2), \end{align} $ $ met behulp van een product van $2rd $-voor waarden. Grotere orders hebben zelfs nog meer voor waarden en geoptimaliseerde varianten kunnen een zeer niet-oplopende volg orde van de exponentiëlen vereisen. Andere geavanceerde algoritmen kunnen ook het gebruik van ancilla qubits in tussenliggende stappen omvatten. Daarom kunnen simulatie algoritmen in de Canon worden gepakketd als het door de gebruiker gedefinieerde type

```qsharp
newtype SimulationAlgorithm = ((Double, EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl);
```

De eerste para meter `Double` is de tijd van simulatie, de tweede para meter `EvolutionGenerator`, die in de sectie Dynamicisatie generator wordt weer [gegeven](xref:microsoft.quantum.libraries.data-structures), is een klassieke beschrijving van een tijdgebonden Hamiltonian die is verpakt met instructies over hoe elke term in de Hamiltonian kan worden gesimuleerd met een Quantum circuit. De typen van dit formulier benaderen de unitary-bewerking $e ^ {-iHt} $ op de derde para meter `Qubit[]`. Dit is de kassa waarin de Quantum status van het gesimuleerde systeem wordt opgeslagen. Net als de tijds afhankelijke case definiëren we een door de gebruiker gedefinieerd type met een `EvolutionSchedule` type, dat een klassieke beschrijving is van een tijdgebonden Hamiltonian.

```qsharp
newtype TimeDependentSimulationAlgorithm = ((Double, EvolutionSchedule, Qubit[]) => Unit : Adjoint, Controlled);
```

Als voor beeld kan de ontleding van de Trotter-Suzuki worden aangeroepen met behulp van de volgende Canon-functies, met para meters `trotterStepSize` de duur van simulatie in elke exponentiële waarde te wijzigen en `trotterOrder` voor de volg orde van de gewenste integrator.

```qsharp
function TrotterSimulationAlgorithm(
    trotterStepSize: Double, 
    trotterOrder: Int) 
    : SimulationAlgorithm {
    ...
}
function TimeDependentTrotterSimulationAlgorithm(
    trotterStepSize: Double, 
    trotterOrder: Int) 
    : TimeDependentSimulationAlgorithm {
    ...
}
```

> [!TIP]
> Toepassingen van de simulatie bibliotheek worden in de voor beelden besproken. Zie het [ **IsingPhaseEstimation** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/IsingPhaseEstimation)-voor beeld voor een fase-schatting in het Ising-model met behulp van `SimulationAlgorithm`.
> Raadpleeg het [ **AdiabaticIsing** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/AdiabaticIsing)-voor beeld voor Adiabatic-status voorbereiding in het Ising-model met behulp van `TimeDependentSimulationAlgorithm`.


### <a name="adiabatic-state-preparation--phase-estimation"></a>Schatting van Adiabatic-status voorbereiding & fase ###

Een gemeen schappelijke toepassing van Hamiltonian simulatie is Adiabatic status voorbereiding. Hier wordt een van de twee Hamiltonians-$H\_{\Text{start}} $ en $H\_{\Text{end}} $, en een Quantum status $ \ket{\psi (0)} $ die een grond staat is van de start Hamiltonian $H\_{\Text{start}} $. Normaal gesp roken wordt $H\_{\Text{start}} $ gekozen, waardoor $ \ket{\psi (0)} $ gemakkelijk kan worden voor bereid op basis van een reken kundige status $ \ket{0\cdots 0} $. Door interpolatie tussen deze Hamiltonians in het tijdgebonden simulatie probleem voldoende traag te maken, is het mogelijk om, met een hoge waarschijnlijkheid, in de grond staat van de uiteindelijke Hamiltonian $H\_{\Text{end}} $. Het voorbereiden van een goede benadering van Hamiltonian-grond staat kan op deze manier door gaan door op tijd afhankelijke Hamiltonian simulatie algoritmen als subroutine aan te roepen, andere conceptuele verschillende benaderingen zoals de variatie van de Quantum eigensolver zijn mogelijk.

Maar een andere toepassing alomtegenwoordige in quantum chemie is het schatten van de bodem status energie van Hamiltonians die de tussenliggende stappen van chemische reactie vertegenwoordigen. Een dergelijke regeling kan bijvoorbeeld afhankelijk zijn van de voor bereiding van de Adiabatic-status om de bodem status te maken en vervolgens een tijdgebonden Hamiltonian-simulatie op te nemen als een subroutine in Phase-schattings karakteisatie om deze energie te extra heren met een beperkte fout en de kans op geslaagde pogingen. 

Bij het samen stellen van simulatie algoritmen als de door de gebruiker gedefinieerde typen `SimulationAlgorithm` en `TimeDependentSimulationAlgorithm` kunnen we hun functionaliteit in meer geavanceerde Quantum algoritmen opnemen. Hiermee wordt u gewend om hetzelfde te doen voor deze veelgebruikte subroutines.

We definiëren daarom de handige functie

```qsharp
function InterpolatedEvolution(
        interpolationTime: Double, 
        evolutionGeneratorStart: EvolutionGenerator,
        evolutionGeneratorEnd: EvolutionGenerator,
        timeDependentSimulationAlgorithm: TimeDependentSimulationAlgorithm)
        : (Qubit[] => Unit is Adj + Ctl) {
        ...
}
 
```

Hiermee wordt een unitary-bewerking geretourneerd waarmee alle stappen van de voor bereiding van Adiabatic-status worden geïmplementeerd. De eerste para meter `interpolatedTime` definieert het tijdstip waarop we lineair interpoleren tussen de start Hamiltonian die worden beschreven door de tweede para meter `evolutionGeneratorStart` en de end Hamiltonian die wordt beschreven door de derde para meter `evolutionGeneratorEnd`. Met de vierde para meter `timeDependentSimulationAlgorithm` wordt de keuze van simulatie algoritme gemaakt. Houd er rekening mee dat als `interpolatedTime` lang genoeg is, een aanvankelijke toestand van de Hamiltonian gedurende de gehele duur van een tijdgebonden simulatie een onmiddellijke bodem status heeft en eindigt op de bodem status van de eind Hamiltonian.

We definiëren ook een nuttige bewerking die automatisch alle stappen van een typische quantum chemie-experiment uitvoert. We hebben bijvoorbeeld het volgende, waarmee een energie schatting wordt geretourneerd van de status die is geproduceerd door de voor bereiding van de Adiabatic-status:

```qsharp
operation AdiabaticStateEnergyEstimate( 
    nQubits : Int, 
    statePrepUnitary: (Qubit[] => Unit),
    adiabaticUnitary: (Qubit[] => Unit),
    qpeUnitary: (Qubit[] => Unit is Adj + Ctl),
    phaseEstAlgorithm : ((DiscreteOracle, Qubit[]) => Double)) 
    : Double {
...
}
```

`nQubits` is het aantal qubits dat wordt gebruikt om de initiële Quantum status te coderen. `statePrepUnitary` bereidt de start status voor op basis van de berekening $ \ket{0\cdots 0} $. `adiabaticUnitary` is de unitary-bewerking die de voor bereiding van Adiabatic-status implementeert, zoals geproduceerd door de functie `InterpolatedEvolution`. `qpeUnitary` is de unitary-bewerking die wordt gebruikt voor het uitvoeren van een fase schatting voor de resulterende Quantum status. `phaseEstAlgorithm` is ons keuze-algoritme voor fase schatting.

> [!TIP]
> Toepassingen van de Adiabatic-status voorbereiding worden behandeld in de voor beelden. Raadpleeg het [ **AdiabaticIsing** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/AdiabaticIsing)-voor beeld voor het Ising-model met behulp van een hand matige implementatie van Adiabatic-status voorbereiding versus het gebruik van de functie `AdiabaticEvolution`.
> Raadpleeg het [ **IsingPhaseEstimation** ](https://github.com/Microsoft/Quantum/tree/master/Samples/src/IsingPhaseEstimation)-voor beeld voor fase schatting en Adiabatic-status voorbereiding in het Ising-model.

> [!TIP]
> De [simulatie van moleculaire water stof](https://github.com/Microsoft/Quantum/tree/master/Samples/src/H2SimulationCmdLine) is een interessant en beknopt voor beeld. De model-en experimentele resultaten die in [O'Malley et. al](https://arxiv.org/abs/1512.06860) zijn gerapporteerd. vereist alleen Pauli-matrices en heeft de vorm $ \hat H = g\_{0}I\_0I\_1 + g\_1 {Z\_0} + g\_2 {Z\_1} + g\_3 {Z\_0} {Z\_1} + g\_4 {Y\_0} {Y\_1} + g\_5 {X\_0} {X\_1} $. Dit is een effectief Hamiltonian waarvoor slechts 2 qubits nodig is, waarbij de constanten $g $ worden berekend op basis van de afstand $R $ tussen de twee water stof atomen. Met Canon functions worden de Paul-functies geconverteerd naar unitaries en vervolgens over korte Peri Oden gegroeid met behulp van de Trotter-Suzuki-ontleding. Een goede benadering van $H de _2 $ aarde kan worden gemaakt zonder gebruik te maken van Adiabatic-status voorbereiding, waardoor de grond staats energie direct kan worden gevonden door de fase-schatting van de Canon te gebruiken.

## <a name="shors-algorithm"></a>Algoritme van Shor ##
Het Shor-algoritme is een van de belangrijkste ontwikkelingen in de Quantum Computing, omdat blijkt dat quantum computers kunnen worden gebruikt voor het oplossen van belang rijke, op dit moment klassieke problemen.
Het Shor-algoritme biedt een snelle manier om grote getallen te vermenigvuldigen met behulp van een quantum computer, een probleem met de naam *factoring*.
De beveiliging van veel aanwezige dagen cryptosystems is gebaseerd op de veronderstelling dat er geen snelle algoritme bestaat voor factories.
Het algoritme van Shor heeft een progevonden effect gehad op hoe we de beveiliging in een post-Quantum wereld denken.

Het Shor-algoritme kan worden beschouwd als een hybride algoritme.
De quantum computer wordt gebruikt voor het uitvoeren van een reken kundige vaste taak die bekend staat als periode zoeken.
De resultaten van de periode zoeken worden vervolgens klassiek verwerkt om de factoren te schatten.
Deze twee stappen worden hieronder besproken.

### <a name="period-finding"></a>Periode zoeken ###

Gezien hoe de Quantum Fourier-trans formatie en fase schatting werken (Zie [Quantum algoritmen](xref:microsoft.quantum.libraries.standard.algorithms)), kunnen we deze hulpprogram ma's gebruiken om een klassiek probleem op te lossen dat de *periode bevindt*.  In de volgende sectie wordt beschreven hoe u de periode voor het zoeken kunt Toep assen op factor.

Als er twee gehele getallen zijn $a $ en $N $, waarbij $a < N $, het doel van het vinden van de periode, ook wel het vinden van orders genoemd, het vinden van de _volg orde_ $r $ van $a $ modulo $N $, waarbij $r $ is gedefinieerd als het minst positieve gehele getal zodat $a ^ r \equiv 1 \Text{mod} N $.  

Als u de order wilt zoeken met behulp van een quantum computer, kunnen we het Phase-schattings algoritme gebruiken dat wordt toegepast op de volgende unitary-operator $U _a $: $ $ U_a\ket {x} \equiv \ket{(AX) \Text{mod} N}. $ $ de eigenvectors van $U _a $ zijn voor geheel getal $s $ en $0 \ Leq s \leq r-$1 , $ $ \ket{x_s} \equiv 1/\sqrt{r} \sum\_{k = 0} ^ {r-1} e ^ {\frac{-2\pi i SK} {r}} \ket{a ^ k\text {mod} N}, $ $ zijn _eigenstates_ van $U _a $.
De eigenvalues van $U _a $ zijn $ $ U\_een \ket{x\_s} = e ^ {2 \ Pi i s/r} \ket{x\_s}. $$

In de fase-schatting wordt de eigenvalues $e ^ {2 \ Pi i s/r} uitgevoerd, waarbij $r $ op efficiënte wijze kan worden geleerd met behulp van [vervolg breuken](https://en.wikipedia.org/wiki/Continued_fraction) uit $s/r $.

Het circuit diagram voor het zoeken naar een Quantum periode is:

![](./../../media/QPE.svg)

Hier $2n $ qubits worden geïnitialiseerd op $ \ket{0}$ en $n $ qubits worden geïnitialiseerd op $ \ket{1}$.
De lezer kan u opnieuw vragen waarom het Quantum REGI ster voor de eigenstates wordt geïnitialiseerd op $ \ket{1}$.
Als één de volg orde niet kent $r $ vooraf, kunnen we $ \ket{x_s} $-Staten niet rechtstreeks voorbereiden.
Gelukkig is dat $1/\ SQRT {r} \sum\_{s = 0} ^ {r-1} \ket{x\_s} = \ket{1}$.
$ \Ket{x} $! wordt niet daad werkelijk voor bereid.
We hebben gewoon een Quantum register van $n $ qubits in status $ \ket{1}$ voor bereid. 

Het circuit bevat de QFT en verschillende bewaakte Gates.
De QFT-Gate is [eerder](xref:microsoft.quantum.libraries.standard.algorithms)beschreven.
De Controlled-$U _a $ Gate Maps $ \ket{x} $ to $ \ket{(AX) \Text{mod} N} $ als het besturings element Qubit $ \ket{1}$ is en wijst $ \ket{x} $ toe aan $ \ket{x} $ anders.

Om $ (a ^ NX) \Text{mod} N $ toe te passen, kunnen we een beheerde $U _ {a ^ N} $ Toep assen, waar we $a ^ N \Text{mod} N $ op klassieke wijze berekenen om in het Quantum circuit aan te sluiten.  
De circuits om dergelijke modulaire reken kundige berekeningen te realiseren, zijn beschreven in de [Quantum reken kundige documentatie](./algorithms.md#arithmetic). er is met name een modulair exponent circuit nodig om de beheerde $U\_{a ^ i} $ bewerkingen te implementeren.

Hoewel het circuit hierboven overeenkomt met de [Quantum fase-schatting](xref:microsoft.quantum.characterization.quantumphaseestimation) en expliciet het zoeken van bestellingen mogelijk maakt, kunnen we het aantal qubits beperken dat nodig is. We kunnen de Beauregard-methode voor het vinden van orders volgen, zoals beschreven [op pagina 8 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8), of een van de fase-schattings routines gebruiken die beschikbaar zijn in micro soft. Quantum. Canon. Een voor beeld van een [Robust Phase-schatting](xref:microsoft.quantum.characterization.robustphaseestimation) maakt bijvoorbeeld ook gebruik van één extra Qubit.
 
### <a name="factoring"></a>Waarbij ###
Het doel van factoren is het bepalen van de twee Prime factoren van het gehele getal $N $, waarbij $N $ een $n $-bit-nummer is.  
Factoring bestaat uit de stappen die hieronder worden beschreven. De stappen zijn onderverdeeld in drie delen: een klassieke preverwerkings routine (1-4); een quantum computing-routine om de volg orde van $a \Text{mod} te vinden, N $ (5); en een klassieke postprocessing-routine voor het afleiden van de Prime factoren uit de bestelling (6-9).

De klassieke preverwerkings routine bestaat uit de volgende stappen:
1. Als $N $ even is, geeft u de Prime factor $2 $ als resultaat.
2. Als $N = p ^ q $ voor $p \geq1 $, $q \geq2 $, geeft u de Prime factor $p $ als resultaat.  Deze stap wordt klassiek uitgevoerd.
3. Kies een wille keurig getal $a $ zodanig dat $1 < een < N-$1.
4. Als $ \Text{GCD} (a, N) > 1 $, wordt de Prime factor $ \Text{GCD} (a, N) $ geretourneerd. Deze stap wordt berekend met behulp van het algoritme van Euclid.
Als er geen Prime factor is geretourneerd, gaan we verder met de Quantum-routine:
5. Roep het algoritme voor het zoeken naar de Quantum periode aan om de volg orde $r $ van $a \Text{mod} N $ te berekenen. Gebruik $r $ in de klassieke postprocessing-routine om de Prime factoren te bepalen:
6. Als $r $ oneven is, gaat u terug naar stap voor voor verwerking (3).
7. Als $r $ even is en $a ^ {r/2} =-1 \ tekst {mod} N $, gaat u terug naar stap voor voor verwerking (3).
8. Als $ \Text{GCD} (a ^ {r/2} + 1, N) $ een niet-triviaische factor van $N $ is, retourneert $ \Text{GCD} (a ^ {r/2} + 1, N) $.
9. Als $ \Text{GCD} (a ^ {r/2}-1, N) $ een niet-triviaische factor van $N $ is, retourneert $ \Text{GCD} (a ^ {r/2}-1, N) $.


De factoring-algoritme is Probabilistic: deze kan worden weer gegeven met een waarschijnlijkheid van ten minste één helft $r $ en $a ^ {r/2} \neq-1 \Text{mod} N $, waardoor er een prime factor wordt geproduceerd.  (Zie [het oorspronkelijke document van Shor](https://doi.org/10.1109/SFCS.1994.365700) voor meer informatie of een van de basis teksten van *Quantum Computing* in [voor meer gegevens](xref:microsoft.quantum.more-information)).
Als er geen Prime factor wordt geretourneerd, herhaalt u de algoritme gewoon uit stap (1).  Na $n $ probeert, is de kans dat elke poging is mislukt Maxi maal $2 ^ {-n} $.
Na het herhalen van het algoritme is het echter een klein aantal keren dat succes is gegarandeerd.