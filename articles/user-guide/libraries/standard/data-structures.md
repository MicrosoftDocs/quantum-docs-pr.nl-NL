---
title: Gegevens structuren in de Q# standaard bibliotheken
description: Meer informatie over gegevens structuren, Oracle en dynamische generatoren in de micro soft- Q# standaard bibliotheken.
author: QuantumWriter
uid: microsoft.quantum.libraries.data-structures
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: e9b593ba69ed41a9fb3c1298b5b945a4cbe43d5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858336"
---
# <a name="data-structures-and-modeling"></a>Gegevens structuren en model lering #

## <a name="classical-data-structures"></a>Klassieke gegevens structuren ##

Naast door de gebruiker gedefinieerde typen voor het weer geven van Quantum concepten, biedt Canon ook bewerkingen, functies en typen voor het werken met klassieke gegevens die worden gebruikt in het beheer van Quantum systemen.
De <xref:Microsoft.Quantum.Arrays.Reversed> functie neemt bijvoorbeeld een matrix als invoer en retourneert dezelfde matrix in omgekeerde volg orde.
Dit kan vervolgens worden gebruikt voor een matrix van het type `Qubit[]` om te voor komen dat overbodige $ \operatorname{swap} $ Gates worden toegepast bij de conversie tussen Quantum representaties van gehele getallen.
We hebben in de vorige sectie gezien dat typen van het formulier `(Int, Int -> T)` handig kunnen zijn voor het weer geven van wille keurige toegangs verzamelingen <xref:Microsoft.Quantum.Arrays.LookupFunction> . de functie biedt daarom een handige manier om dergelijke typen van matrix typen samen te stellen.

### <a name="pairs"></a>Paarsgewijs ###

De Canon ondersteunt de functionele stijl notatie voor paren, een aanvulling op de toegang tot Tuples door het ontbouwen:

```qsharp
let pair = (PauliZ, register); // type (Pauli, Qubit[])
ApplyToEach(H, Snd(pair)); // No need to deconstruct to access the register.
```

### <a name="arrays"></a>Matrices ###

De Canon biedt verschillende functies voor het bewerken van matrices.
Deze functies zijn van het type para meters en kunnen dus worden gebruikt met matrices van elk Q# type.
De <xref:Microsoft.Quantum.Arrays.Reversed> functie retourneert bijvoorbeeld een nieuwe matrix waarvan de elementen in omgekeerde volg orde van de invoer worden weer gegeven.
Dit kan worden gebruikt om te wijzigen hoe een Quantum register wordt weer gegeven bij het aanroepen van bewerkingen:

```qsharp
let leRegister = LittleEndian(register);
// QFT expects a BigEndian, so we can reverse before calling.
QFT(BigEndian(Reversed(leRegister!)));
// This is how the LittleEndianAsBigEndian function is implemented:
QFT(LittleEndianAsBigEndian(leRegister));
```

De <xref:Microsoft.Quantum.Arrays.Subarray> functie kan ook worden gebruikt om de volg orde van de elementen van een matrix te wijzigen of er subsets van te maken:

```qsharp
// Applies H to qubits 2 and 5.
ApplyToEach(H, Subarray([2, 5], register));
```

In combi natie met Datatransport besturing kunnen matrix manipulatie functies, zoals, <xref:Microsoft.Quantum.Arrays.Zipped> een krachtige manier bieden om Quantum Program ma's uit te voeren:

```qsharp
// Applies X₃ Y₁ Z₇ to a register of any size.
ApplyToEach(
    ApplyPauli(_, register),
    Map(
        EmbedPauli(_, _, Length(register)),
        Zipped([PauliX, PauliY, PauliZ], [3, 1, 7])
    )
);
```

## <a name="oracles"></a>Oracle ##

In de [fase schatting](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm) en [amplitude versterking](https://en.wikipedia.org/wiki/Amplitude_amplification) wordt het concept van een Oracle regel matig weer gegeven.
Hier verwijst de term Oracle naar een Quantum subroutine die op een set qubits reageert en het antwoord als een fase retourneert.
Deze subroutine kan vaak worden beschouwd als een invoer voor een Quantum algoritme die de Oracle accepteert, naast enkele andere para meters, en past een reeks Quantum bewerkingen toe en behandelt een aanroep naar deze Quantum subroutine alsof het een fundamenteel poort is.
Uiteraard moet, om het grotere algoritme te implementeren, een concreet ontbinding van de Oracle in fundamentele Gates worden gegeven, maar een dergelijke ontbinding is niet nodig om inzicht te krijgen in het algoritme dat de Oracle aanroept.
In Q# wordt deze abstractie vertegenwoordigd door gebruik te maken van die bewerkingen waarden voor de eerste klasse, zodat de bewerkingen kunnen worden door gegeven aan implementaties van Quantum algoritmen in een Black Box-vorm.
Daarnaast worden door de gebruiker gedefinieerde typen gebruikt voor het labelen van de verschillende Oracle-representaties op een type veilige manier, waardoor het moeilijk is om verschillende soorten Black Box-bewerkingen per ongeluk te verkleinen.

Dergelijke Oracle worden weer gegeven in een aantal verschillende contexten, waaronder beroemde-voor beelden zoals de zoek-en Quantum-simulatie algoritmen [van Grover](https://en.wikipedia.org/wiki/Grover%27s_algorithm) .
Hier richten we ons op de Oracle die nodig zijn voor slechts twee toepassingen: amplitude versterking en fase schatting.
We bespreken eerst amplitude versterking van Oracle, voordat u verdergaat met de fase schatting.

### <a name="amplitude-amplification-oracles"></a>Met amplitude verhogen Oracle ###

Het proces van de amplitude versterking strekt ertoe een rotatie uit te voeren tussen een initiële staat en een eind status door een reeks reflecties van de staat toe te passen.
Om het algoritme te laten functioneren, moet deze beide statussen worden opgegeven.
Deze specificaties worden gegeven door twee Oracle.
Deze Oracle werken door de invoer in twee spaties, een ' doel-' subruimte en een ' eerste ' subruimte te breken.
De Oracle-producten identificeren dergelijke subruimten, vergelijkbaar met de manier waarop Pauli-Opera tors twee ruimten identificeren, door een $ \pm $1-fase op deze ruimten toe te passen.
Het belangrijkste verschil is dat deze ruimten geen halve ruimte in deze toepassing hoeven te zijn.
Houd er ook rekening mee dat deze twee subruimten meestal niet wederzijds worden exclusief: er zijn vectoren die lid zijn van beide spaties.
Als dat niet het geval is, zou de amplitude versterking geen effect hebben, zodat de eerste subruimte niet-nul overlapt met de doel-subruimte.

We zullen de eerste Oracle aanduiden die we nodig hebben voor een amplitude versterking van $P \_ $0, gedefinieerd om de volgende actie te kunnen ondernemen.  Voor alle statussen $ \ket{x} $ in de "eerste" subruimte $P \_ 0 \ket{x} =-\ket{x} $ en voor alle staten $ \ket{y} $ die zich niet in deze subruimte bevinden, hebben we $P \_ 0 \ket{y} = \ket{y} $.
De Oracle die de doel-subruimte markeert, $P _1 $ heeft precies hetzelfde formulier.
Voor alle statussen $ \ket{x} $ in de doel-subruimte (bijvoorbeeld voor alle statussen die u wilt laten uitvoeren), $P _1 \ Ket {x} =-\ket{x} $.
Op dezelfde manier geldt dat voor alle staten $ \ket{y} $ die zich niet in de doel ruimte bevinden $P _1 \ Ket {y} = \ket{y} $.
Deze twee reflecties worden vervolgens gecombineerd om een operator te vormen die één stap van de amplitude versterking aanneemt, $Q =-P_0 P_1 $, waarbij het totale minteken alleen belang rijk is om te overwegen in beheerde toepassingen.
De versterkings versterking van de amplitude gaat vervolgens door een initiële status, $ \ket{\psi} $, die zich in de eerste subruimte bevindt en voert vervolgens $ \ket{\psi} \mapsto Q ^ m \ket{\psi} $ uit.
Het uitvoeren van een dergelijke iteratie garandeert dat als er een begin status is die overlap $ \sin ^ 2 (\theta) $ met de gemarkeerde ruimte bevat en na $m $ iteraties deze overlap ping wordt $ \sin ^ 2 ([2 min. + 1] \theta) $.
Daarom wilt u $m $ kiezen als een gratis para meter, zodat $ [2 min. + 1] \theta = \ pi/2 $; dergelijke stijve keuzes zijn echter niet zo belang rijk voor sommige vormen van amplitude versterking, zoals het verhogen van een amplitude van het vaste punt.
Met dit proces kan ons een status voorbereiden in de gemarkeerde subruimte met behulp van quadratically minder query's naar de Mark-functie en de status voorbereidings functie dan zou kunnen worden uitgevoerd op een strikt klassiek apparaat.
Daarom is amplitude versterking een belang rijke bouw steen voor veel toepassingen van Quantum Computing.

Om inzicht te krijgen in hoe u het algoritme kunt gebruiken, is het handig om een voor beeld te bieden dat een constructie van de Oracle biedt.  Overweeg het uitvoeren van de Grover-algoritme voor het zoeken naar data bases in deze instelling.
In de zoek opdracht van Grover is het doel om de status te transformeren $ \ket{+} ^ {\otimes n} = H ^ {\otimes n} \ket {0} $ in een van (mogelijk) veel gemarkeerde statussen.
Om verder te vereenvoudigen, laten we eens kijken naar het geval waarin de enige status is ingesteld op $ \ket {0} $.
Vervolgens zijn er twee Oracle-ontwerpen: een die alleen de initiële status $ \ket{+} ^ {\otimes n} $ markeert met een minteken en een andere die de gemarkeerde status $ \ket $ markeert {0} met een minteken.
De laatste Gate kan worden geïmplementeerd met behulp van de volgende proces bewerking, met behulp van de controle stroom bewerkingen in de Canon:

```qsharp
operation ReflectAboutAllZeros(register : Qubit[]) : Unit 
is Adj + Ctl {

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);

    // Apply an $n-1$ controlled $Z$-gate to the $n^{\text{th}}$ qubit.
    // This gate will lead to a sign flip if and only if every qubit is
    // $1$, which happens only if each of the qubits were $0$ before step 1.
    Controlled Z(Most(register), Tail(register));

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);
}
```

Deze Oracle is vervolgens een speciaal geval van de <xref:Microsoft.Quantum.Canon.RAll1> bewerking, waardoor het mogelijk is om te roteren met een wille keurige fase in plaats van de reflectie Case $ \phi = \pi $.
In dit geval `RAll1` is de <xref:Microsoft.Quantum.Intrinsic.R1> prelude-bewerking vergelijkbaar met het draaien van $ \ket{11\cdots1} $ in plaats van de single-Qubit status $ \ket {1} $.

De Oracle die de eerste subruimte markeert, kan op dezelfde manier worden samengesteld.
In pseudocode:

1. $H $ Gates op elke qubit Toep assen.
2. $X $ Gates op elke qubit Toep assen.
3. Pas een door $n $1 beheerde $Z $-Gate toe op de $n ^ {\Text{th}} $ Qubit.
4. $X $ Gates op elke qubit Toep assen.
5. $H $ Gates op elke qubit Toep assen.

Deze keer worden ook gedemonstreerd met <xref:Microsoft.Quantum.Canon.ApplyWith> de <xref:Microsoft.Quantum.Canon.RAll1> bewerking die hierboven wordt beschreven:

```qsharp
operation ReflectAboutInitial(register : Qubit[]) : Unit
is Adj + Ctl {
    ApplyWithCA(ApplyToEach(H, _), ApplyWith(ApplyToEach(X, _), RAll1(_, PI()), _), register);
}
```

We kunnen deze twee Oracle vervolgens samen combi neren om te roteren tussen de twee staten en deterministischly transformeren $ \ket{+} ^ {\otimes n} $ to $ \ket {0} $ met behulp van een aantal lagen van Hadamard-Gates dat proportioneel is aan $ \sqrt{2 ^ n} $ (ie $m \propto \sqrt{2 ^ n} $) ten opzichte van de ongeveer $2 ^ n $ lagen die nodig zouden zijn voor het niet-deterministisch voorbereiden van de $ \ket {0} $-status door de eerste toestand voor te bereiden en te meten, totdat het resultaat $0 $ wordt waargenomen.

### <a name="phase-estimation-oracles"></a>Fase schatting Oracle ###

Voor een gefaseerde schatting zijn de Oracle enigszins natuurlijk iets meer.
De beoogde fase schatting is het ontwerpen van een subroutine die kan worden gesampling van de eigenvalues van een unitary-matrix.
Deze methode is onmisbaar in de Quantum simulatie omdat voor veel fysieke problemen in schei-en materiaal wetenschappen deze eigenvalues de grond staat Energies van Quantum systemen, die ons waardevolle informatie biedt over de fase diagrammen van materialen en reactie dynamiek voor moleculen.
Elk soort fase schatting heeft een invoer unitary nodig.
Deze unitary wordt standaard beschreven door een van de twee typen Oracle.

> [!TIP]
> Beide Oracle-typen die hieronder worden beschreven, zijn opgenomen in de voor beelden.
> Zie het [ **PhaseEstimation**](https://github.com/microsoft/Quantum/tree/main/samples/characterization/phase-estimation)-voor beeld voor meer informatie over continue query Oracle.
> Zie het [ **IsingPhaseEstimation**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/phase-estimation)-voor beeld voor meer informatie over discrete query-Oracle.

Het eerste type Oracle, waarmee we een discrete query Oracle aanroepen en met het door de gebruiker gedefinieerde type vertegenwoordigen <xref:Microsoft.Quantum.Oracles.DiscreteOracle> , bestaat uit een unitary matrix.
Als $U $ de unitary is waarvan de eigenvalues een schatting wil maken, is de Oracle voor $U $ gewoon een standaard voor een subroutine waarmee $U $ wordt geïmplementeerd.
Een voor beeld: het kan $U $ nemen als de hierboven gedefinieerde Oracle-$Q $ voor de schatting van de amplitude.
De eigenvalues van deze matrix kan worden gebruikt om de overlap ping te ramen tussen de eerste en de doel status, $ \sin ^ 2 (\theta) $, met behulp van quadratically minder steek proeven dan het enige wat zou nodig zouden zijn.
Dit verdient de toepassing van de fase schatting met behulp van de Grover Oracle $Q $ als invoer van de moniker van de amplitude schatting.
Een andere algemene toepassing, veel gebruikt in Quantum-metrologies, is een schatting van een kleine draai hoek.
Met andere woorden, we willen $ \theta $ schatten voor een onbekende rotatie poort van het formulier $R _z (\theta) $.
In dergelijke gevallen zou de subroutine waarmee we werken om deze vaste waarde van $ \theta $ voor de poort te leren kennen, $ $ \begin{align} U & = R_z (\theta) \\ \\ & = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {i \ theta/2} \end{bmatrix}.
\end{align} $ $

Het tweede type Oracle dat in fase schatting wordt gebruikt, is de continue query Oracle, vertegenwoordigd door het <xref:Microsoft.Quantum.Oracles.ContinuousOracle> type.
Een continue query in Oracle voor fase schatting neemt de vorm $U (t) $ waarbij $t $ een klassiek bekend reëel getal is.
Als we $U $ een vast unitary hebben, neemt de doorlopende query Oracle het formulier $U (t) = U ^ t $.
Hierdoor kunnen we matrixen opvragen, zoals $ \sqrt{U} $, die niet rechtstreeks in het discrete query model kunnen worden geïmplementeerd.

Dit type Oracle is waardevol wanneer u een bepaalde unitary niet doorzoekt, maar de eigenschappen van de generator van de unitary wilt weten.
In een dynamische Quantum simulatie is het doel bijvoorbeeld om Quantum circuits te ontwikkelen die nauw $U (t) = e ^ {-i H t} $ voor een Hermitian matrix $H $ en ontwikkelings tijd $t $.
De eigenvalues van $U (t) $ zijn direct gerelateerd aan de eigenvalues van $H $.
Als u dit wilt zien, kunt u een eigenvector van $H $: $H \ket{E} = E\ket {E} $ overwegen. het is eenvoudig om te zien van de definitie van de matrix exponentieel dat $U (t) \ket{E} = e ^ {i\phi} \ Ket {E} = e ^ {-iEt} \ket{E} $.
Door de eigenphase van $U (t) $ te schatten, geeft u de eigenvalue $E $ op, ervan uitgaande dat de eigenvector $ \ket{E} $ wordt ingevoerd in het fase schattings algoritme.
In dit geval kan de waarde $t $ echter worden gekozen op basis van de keuze van de gebruiker, omdat voor een voldoende kleine waarde van $t $ de eigenvalue $E $ kan worden teruggedraaid via $E =-\ Phi/t $.
Aangezien Quantum simulatie methoden de mogelijkheid bieden om een gedeeltelijke evolutie uit te voeren, is dit een extra vrijheid bij het uitvoeren van een query op de unitary, met name hoewel het discrete query model alleen unitaries van het formulier toestaat $U ^ j $ voor het Toep assen van een geheel getal $j $ de continue query in Oracle kan unitaries van het formulier benaderen $U ^ t $ voor echte waarden $t $.
Dit is belang rijk voor het samen voegen van elke laatste ounce van efficiëntie voor de fase schattings algoritmen, omdat hiermee precies het experiment kan worden gekozen waarmee de meeste informatie over $E $; de methoden op basis van discrete query's moeten in het gedrang komen door het beste gehele aantal query's in het algoritme te kiezen.

Als concreet voor beeld moet u rekening houden met het probleem bij het schatten van de draai hoek van een Gate, maar de verwerkings frequentie van een Roteer Quantum systeem.
De unitary die een dergelijke Quantum dynamiek beschrijft, is $U (t) = R_z (2 \ Omega t) $ voor ontwikkelings tijd $t $ en onbekende frequentie $ \omega $.
In deze context kunnen we $U (t) $ voor elke $t $ simuleren met behulp van één $R _z-Gate en zo dat zelf niet hoeft te worden beperkt tot afzonderlijke query's voor de unitary.
Een dergelijk doorlopende model heeft ook de eigenschap die de frequenties groter dan $2 \ PI $ kan worden geleerd van fase schattings processen die doorlopende query's gebruiken omdat de fase-informatie die anders zou worden gemaskeerd door de vertakking van de functie logaritme kan worden onthuld op basis van de resultaten van experimenten die worden uitgevoerd op niet-proportionele waarden van $t $.
Daarom zijn problemen zoals deze continue query modellen voor de fase schatting Oracle niet alleen geschikt, maar ook de voor keur voor het discrete query model.
Daarom Q# heeft de functionaliteit voor beide vormen van query's en kan deze door de gebruiker worden afgestemd op een fase schattings algoritme om te voldoen aan de behoeften en het type Oracle dat beschikbaar is.

## <a name="dynamical-generator-modeling"></a>Model lering van dynamische generator ##

Generatoren van tijd-ontwikkeling beschrijven hoe statussen door de tijd worden ontwikkeld. Zo wordt de dynamiek van een Quantum status $ \ket{\psi} $ geregeld door de Schrödinger-vergelijking $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = H \ket{\psi (t)}, \end{align} $ $ met een Hermitian matrix $H $, de Hamiltonian, als de generator van bewegingen. Op basis van een initiële status $ \ket{\psi (0)} $ op tijdstip $t = $0, de formele oplossing voor deze vergelijking op het moment $t $ kan zijn: in principe, geschreven $ $ \begin{align} \ket{\psi (t)} = U (t) \ket{\psi (0)}, \end{align} $ $, waarbij de matrix exponentiële $U (t) = e ^ {-i H t} $ wordt aangeduid als de operator unitary time-evolutie. Hoewel we ons richten op de genera tors van dit formulier, is het belang rijk dat het concept uitgebreid van toepassing is, zoals voor de simulatie van open Quantum systemen, of op meer abstracte differentiële vergelijkingen.

Een primair doel van dynamische simulatie is het implementeren van de operator voor tijd ontwikkeling op een versleutelde Quantum status in qubits van een quantum computer.  In veel gevallen kan de Hamiltonian worden opgesplitst in een som van enkele $d $ gecompliceerde termen

$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} H_j, \end{align} $ $

Wanneer tijd-ontwikkeling per term eenvoudig is om op een quantum computer te implementeren. Als $H _j $ bijvoorbeeld een Pauli is $X _1X_2 $-operator die wordt uitgevoerd op de eerste en 2e elementen van het Qubit `qubits` -REGI ster, kan de tijd worden gepasseerd voor elke tijd $t $ kan eenvoudigweg worden geïmplementeerd door de bewerking `Exp([PauliX,PauliX], t, qubits[1..2])` aan te roepen, die hand tekening heeft `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` . Zoals verderop in Hamiltonian simulatie wordt beschreven, is één oplossing een benadering van de tijd evolutie van $H $ met een reeks eenvoudige bewerkingen

$ $ \begin{align} U (t) & = \left (e ^ {-iH \_ 0 t/r} e ^ {-IH \_ 1 t/r} \cdots e ^ {-IH \_ {d-1} t/r} \right) ^ {r} + \mathcal{O} (d ^ 2 \ max_j \\ | H \_ j \\ | ^ 2 t ^ 2/r), \end{align} $ $

waarbij het gehele getal $r > $0 de aanpassings fout bepaalt.

De model bibliotheek voor dynamische Generator biedt een framework voor het systematisch coderen van gecompliceerde generators in termen van eenvoudigere Generators. Een dergelijke beschrijving kan vervolgens worden door gegeven aan de simulatie bibliotheek voor het implementeren van tijd evolutie door een simulatie algoritme van keuze, waarbij veel details automatisch worden verwerkt.

> [!TIP]
> De dynamische Generator bibliotheek die hieronder wordt beschreven, is opgenomen in de voor beelden. Voor een voor beeld op basis van het Ising-model raadpleegt u het [ **IsingGenerators**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/generators)-voor beeld.
> Voor een voor beeld op basis van moleculaire water stof raadpleegt u de voor beelden van [**H2SimulationCmdLine**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/command-line) en [**H2SimulationGUI**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/gui) .

### <a name="complete-description-of-a-generator"></a>Volledige beschrijving van een generator ###

Op het hoogste niveau bevindt zich een volledige beschrijving van een Hamiltonian in het door de `EvolutionGenerator` gebruiker gedefinieerde type dat twee onderdelen heeft.:

```qsharp
newtype EvolutionGenerator = (EvolutionSet, GeneratorSystem);
```

Het door de `GeneratorSystem` gebruiker gedefinieerde type is een klassieke beschrijving van de Hamiltonian.

```qsharp
newtype GeneratorSystem = (Int, (Int -> GeneratorIndex));
```

Het eerste element `Int` van de tuple slaat het aantal termen $d $ op in de Hamiltonian, en het tweede element `(Int -> GeneratorIndex)` is een functie die een gehele index in $ \{ 0, 1,..., d-1 $ toewijst \} aan een door de `GeneratorIndex` gebruiker gedefinieerd type waarmee elke primitieve term in de Hamiltonian uniek wordt geïdentificeerd. Houd er rekening mee dat door het verzamelen van voor waarden in de Hamiltonian als een functie in plaats van een matrix `GeneratorIndex[]` te gebruiken, dit de mogelijkheid biedt om op basis van de `GeneratorIndex` waarde die het meest geschikt is bij het beschrijven van Hamiltonians met een groot aantal voor waarden.

Het is van cruciaal belang dat we geen conventies opleggen voor de primitieve termen die zijn geïdentificeerd door de `GeneratorIndex` eenvoudige simulatie. Primitieve termen kunnen bijvoorbeeld worden Pauli Opera tors zoals hierboven beschreven, maar ze kunnen ook Fermionic Annihilation zijn en Opera tors maken die vaak worden gebruikt in de vorm van quantum chemie. Op zichzelf is een ' `GeneratorIndex` Onwaar ', wat betekent dat er niet wordt beschreven hoe tijd-evolutie door de term waar deze naar wijst, kan worden geïmplementeerd als een Quantum circuit.

Dit probleem wordt opgelost door een door `EvolutionSet` de gebruiker gedefinieerd type op te geven waarmee een `GeneratorIndex` van de canonieke sets wordt toegewezen aan een unitary-operator, de `EvolutionUnitary` , uitgedrukt als een Quantum circuit. De `EvolutionSet` definieert de Conventie van de manier waarop een `GeneratorIndex` Structured is en definieert ook de mogelijke reeks `GeneratorIndex` .

```qsharp
newtype EvolutionSet = (GeneratorIndex -> EvolutionUnitary);
```

### <a name="pauli-operator-generators"></a>Pauli operator Generators ###

Een concreet en nuttig voor beeld van generatoren zijn Hamiltonians die een som zijn van Pauli-Opera Tors, elk mogelijk met een andere coëfficiënt.
$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} a_j H_j, \end{align} $ $ waarbij elke $ \hat-H_j $ nu wordt getrokken van de Pauli groep. Voor dergelijke systemen bieden we het `PauliEvolutionSet()` type `EvolutionSet` dat een conventie definieert voor de manier waarop een element van de Pauli-groep en een coëfficiënt kunnen worden geïdentificeerd door een `GeneratorIndex` , die de volgende hand tekening heeft.

```qsharp
newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```

In onze code ring specificeert de eerste para meter `Int[]` een Pauli teken reeks, waarbij $ \Hat I\rightarrow $0, $ \Hat X\rightarrow $1, $ \Hat Y\rightarrow $2, en $ \Hat Z\rightarrow $3. Met de tweede para meter wordt `Double[]` de coëfficiënt van de Pauli-teken reeks opgeslagen in de Hamiltonian. Houd er rekening mee dat alleen het eerste element van deze matrix wordt gebruikt. De derde para meter `Int[]` indexeert de qubits die door deze Pauli teken reeks wordt toegepast en mag geen dubbele elementen bevatten. Daarom kan de Hamiltonian term $0,4 \hat X_0 \hat Y_8 \hat I_2 \hat Z_1 $ worden weer gegeven als

```qsharp
let generatorIndexExample = GeneratorIndex(([1,2,0,3], [0.4]]), [0,8,2,1]);
```

De `PauliEvolutionSet()` is een functie waarmee een `GeneratorIndex` van dit formulier wordt toegewezen aan een `EvolutionUnitary` met de volgende hand tekening.

```qsharp
newtype EvolutionUnitary = ((Double, Qubit[]) => Unit is Adj + Ctl);
```

De eerste para meter vertegenwoordigt een tijd duur, die wordt vermenigvuldigd met de coëfficiënt in de `GeneratorIndex` , van unitary-evolutie. De tweede para meter is het Qubit registreren van de unitary. 

### <a name="time-dependent-generators"></a>Time-Dependent-Generators ###

In veel gevallen zijn we ook geïnteresseerd in het model leren van tijd afhankelijke generatoren, zoals kan optreden in de Schrödinger-vergelijking $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = \hat H (t) \ket{\psi (t)}, \end{align} $ $, waarbij de generator $ \hat H (t) $ nu tijd afhankelijk is. De uitbrei ding van de tijd onafhankelijke genera tors hierboven is eenvoudig. In plaats van een probleem `GeneratorSystem` te hebben met het Hamiltonian voor alle keren $t $, hebben we het type dat door de `GeneratorSystemTimeDependent` gebruiker is gedefinieerd.

```qsharp
newtype GeneratorSystemTimeDependent = (Double -> GeneratorSystem);
```

De eerste para meter is een doorlopende schema parameter $s \in [0, 1] $, en functies van dit type retour neren een `GeneratorSystem` voor dat schema. Houd er rekening mee dat de plannings parameter lineair kan zijn gerelateerd aan de para meter voor fysieke tijd, bijvoorbeeld $s = t/T $, voor een totale tijd van simulatie $T $. In het algemeen hoeft dit echter niet het geval te zijn.

Op dezelfde manier is voor een volledige beschrijving van deze generator een `EvolutionSet` , en dus een door de `EvolutionSchedule` gebruiker gedefinieerd type gedefinieerd.

```qsharp
newtype EvolutionSchedule = (EvolutionSet, GeneratorSystemTimeDependent);
```
