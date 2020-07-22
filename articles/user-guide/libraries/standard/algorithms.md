---
title: 'Quantum algoritmen in Q #'
description: Meer informatie over de belangrijkste Quantum Computing-algoritmen, waaronder amplitude versterking, Fourier Transform, Draper en Beauregard adders, en fase schatting.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.algorithms
ms.openlocfilehash: 7f4916353c53d6459356243098281ccb16b17278
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871311"
---
# <a name="quantum-algorithms"></a>Quantum algoritmen #

## <a name="amplitude-amplification"></a>Amplitudeversterking ##

*Amplitude versterking* is een van de fundamentele hulpprogram Ma's van Quantum Computing. Het is het belangrijkste idee dat grover de zoek functie, amplitude schatting en veel Quantum machine learning-algoritmen ondervindt.  Er zijn veel varianten, en in Q # bieden we een algemene versie op basis van een Oblivious amplitude-versterking met gedeeltelijke reflecties om het breedste toepassings gebied te bieden.

Het centrale idee achter amplitude versterking is het verhogen van de kans op een gewenste uitkomst door een reeks reflecties uit te voeren.  Deze reflecties draaien de begin status dichter naar de gewenste doel status, ook wel een gemarkeerde status genoemd.  Als de waarschijnlijkheid van het meten van de begin status een gemarkeerde status is, is $ \sin ^ 2 (\theta) $ en na het Toep assen van amplitude versterking $m $ keer de kans op succes wordt $ \sin ^ 2 ((2 min. + 1) \theta) $.  Dit betekent dat als $ \theta = \ PI/[2 (2n + 1)] $ voor een bepaalde waarde van $n $, de amplitude-versterking de kans op succes tot $100 \\ % $ kan verhogen na $n $ iteraties van de amplitude versterking.  Omdat $ \theta = \sin ^ {-1} (\sqrt{\Pr (geslaagd)}) $ Dit betekent dat het aantal iteraties dat nodig is om een geslaagde deterministischheid te verkrijgen, quadratically lager is dan het verwachte aantal dat nodig is om een gemarkeerde status niet-deterministisch te vinden met wille keurige steek proeven.

Voor elke iteratie van de amplitude versterking moeten twee reflectie operatoren worden opgegeven. In het bijzonder, als $Q $ de amplitude versterking is, en $P _0 $ een projector operator is op de eerste subruimte en $P _1 $ de projector op de gemarkeerde subruimte is, dan $Q =-(\boldone-2P_0) (\boldone-2P_1) $.  Het is raadzaam dat een projector een Hermitian-operator is met eigenvalues $ + $1 en $0 $, en als resultaat $ (\boldone-2P_0) $ is unitary, omdat het eigenvalues heeft die wortel zijn van Unity (in dit geval $ \pm $1). Bekijk bijvoorbeeld het geval van een Grover-zoek opdracht met de begin status $H ^ {\otimes n} \ket {0} $ en marked State $ \ket{m} $, $P _0 = H ^ {\otimes n} \ket {0} \bra {0} H ^ {\otimes n} $ en $P _1 = \ket{m}\bra{m} $.  In de meeste toepassingen van amplitude versterking $P _0 $ een projector is op een oorspronkelijke staat, wat betekent dat $P _0 = \boldone-2 \ Ket {\ psi} \ Bra {\ psi} $ voor sommige vector $ \ket{\psi} $; voor Oblivious amplitude amplication $P _0 $ bijvoorbeeld projecteren op veel Quantum Staten (dat wil zeggen, de multipliciteit van de $ + $1 eigenvalue van $P _0 $ groter is dan $1 $).

De logica achter de amplitude versterking volgt rechtstreeks van de eigen van $Q $.  Met name de eigenvectors van $Q $ dat de oorspronkelijke status geen ondersteuning voor nul heeft, kan worden weer gegeven als lineaire combi Naties van de $ + $1 eigenvectors van $P _0 $ en $P _1 $.  Met name de eerste status voor amplitude versterking (ervan uitgaande dat het een $ + $1 eigenvector van $P _0 $) kan worden geschreven als $ $ \ket{\psi} = \frac{-i}{\sqrt {2} } \left (e ^ {i\theta} \ Ket {\ psi_ +} + e ^ {-i\theta} \ Ket {\ psi_-} \right), $ $ waarbij $ \ket{\ psi_ \pm} $ eigenvectors zijn van $Q $ met eigenvalues $e ^ {\pm 2i \ theta} $ en alleen ondersteuning biedt voor de $ + $1 eigenvectors van $P _0 $ en $P _1 $.  Het feit dat de eigenvalues zijn $e ^ {\pm i \theta} $ impliceert dat de operator $Q $ een draaiing uitvoert in een tweedimensionale subruimte die is opgegeven door de twee projectors en de begin toestand waarin de draai hoek $2 \ theta $ is.  Daarom moet u na $m $-iteraties van $Q $ de kans op succes is $ \sin ^ 2 ([2 min. + 1] \theta) $.

Een andere nuttige eigenschap die er uit komt, is dat de eigenvalue $ \theta $ direct gerelateerd is aan de waarschijnlijkheid dat de oorspronkelijke status zou worden gemarkeerd (in het geval waar $P _0 $ een projector is op alleen de begin toestand).  Omdat de eigenphases van $Q $ $2 \ theta = 2 \ Sin ^ {-1} (\sqrt{\Pr (geslaagd)}) is, volgt $ het. als we de fase-schatting Toep assen op $Q $, kunnen we de kans op succes voor een unitary Quantum-procedure ontdekken.  Dit is handig omdat u quadratically minder toepassingen van de Quantum procedure nodig hebt om de kans op succes te ontdekken dan anders zou zijn.

Q # introduceert een amplitude versterking als een specialisatie van obliviouse amplitude versterking.  De Oblivious-amplitude versterking heeft deze moniker, omdat de projector op de eerste eigenspace geen projector hoeft te zijn op de oorspronkelijke staat.  In deze zin is het protocol Oblivious in de oorspronkelijke staat.  De belangrijkste toepassing van de Oblivious-amplitude versterking is in bepaalde *lineaire combi Naties van simulatie methoden van unitary* Hamiltonian, waarbij de oorspronkelijke status onbekend is, maar wordt Entangled met een ancilla-REGI ster in het simulatie protocol.  Als dit ancilla-REGI ster zou moeten worden gewaardeerd als een vaste waarde, zegt $0 $, dan passen die simulatie methoden de gewenste unitary-trans formatie toe op de resterende qubits (het systeem register genoemd).  Alle andere meet resultaten leiden echter tot storingen.  Met de versterking van Oblivious-amplitude kan de kans op succes van deze meting worden verhoogd tot $100 \\ % $ met behulp van de bovenstaande reden.  Daarnaast komt de normale amplitude versterking overeen met de gevallen waarin het systeem register leeg is.  Daarom gebruikt Q # Oblivious amplitude versterking als de belangrijkste amplitude versterking subroutine.

De algemene routine ( `AmpAmpObliviousByReflectionPhases` ) heeft twee registers die we aanroepen `ancillaRegister` en `systemRegister` . Daarnaast worden er twee Oracle-waarden geaccepteerd voor de nood zakelijke reflecties. De `ReflectionOracle` handelingen worden alleen uitgevoerd op het `ancillaRegister` moment dat de `ObliviousOracle` acties gezamenlijk op beide kassa's worden uitgevoerd. De invoer voor `ancillaRegister` moet worden geïnitialiseerd op een-1-eigenstate van de eerste reflectie operator $ \boldone-2P_1 $.

Normaal gesp roken wordt de status in de Oracle-voor bereiding berekend op basis van de berekening $ \ket{0...0} $. In onze implementatie bestaat het `ancillaRegister` uit één Qubit ( `flagQubit` ) dat de `stateOracle` en de rest van de gewenste ancillas regelt. De `stateOracle` wordt toegepast wanneer `flagQubit` $ \ket {1} $.

Een kan ook Oracle bevatten `StateOracle` en `ObliviousOracle` in plaats van reflecties via een aanroep van `AmpAmpObliviousByOraclePhases` .

Zoals vermeld, is traditionele amplitude versterking slechts een speciaal geval van deze routines waar `ObliviousOracle` de identiteits operator is en er geen systeem-qubits (dat wil zeggen, `systemRegister` is leeg). Als u fasen wilt verkrijgen voor gedeeltelijke reflecties (bijvoorbeeld voor Grover Search), is de functie `AmpAmpPhasesStandard` beschikbaar. Raadpleeg `DatabaseSearch.qs` voor een voorbeeld implementatie van het algoritme van Grover.

We hebben de draaiings fasen met één Qubit gekoppeld aan de fasen van de reflectie operator zoals beschreven in het artikel met [G.H. low, I. L. Chuang](https://arxiv.org/abs/1707.05391). De vaste-punt fasen die worden gebruikt, worden in [Yoder, laag en Chuang](https://arxiv.org/abs/1409.3305) samen met de fasen in [laag, Yoder en Chuang](https://arxiv.org/abs/1603.03996)beschreven.

Voor achtergrond kunt u beginnen met [standaard amplitude versterking](https://arxiv.org/abs/quant-ph/0005055) en vervolgens overschakelen naar een inleiding tot [Obliviouse amplitude versterking](https://arxiv.org/abs/1312.1414) en finally-generalisaties die worden gepresenteerd in [laag en Chuang](https://arxiv.org/abs/1610.06546). Een goed overzicht van het hele gebied (zoals het is gekoppeld aan Hamiltonian simulatie) werd gegeven door [Dominic Berry](http://www.dominicberry.org/presentations/Durban.pdf).

## <a name="quantum-fourier-transform"></a>Kwantum Fourier-trans formatie ##

De Fourier-trans formatie is een fundamenteel hulp middel voor klassieke analyse en is net zo belang rijk voor Quantum berekeningen.
Daarnaast overschrijdt de efficiency van de *Quantum Fourier trans formatie* (QFT) ver wat mogelijk is op een klassieke machine, waardoor deze een van de eerste hulp middelen is die u kunt gebruiken bij het ontwerpen van een Quantum algoritme.

Als een geschatte generalisatie van de QFT bieden we de <xref:microsoft.quantum.canon.approximateqft> bewerking die verdere optimalisaties mogelijk maakt door rotaties te verwijderen die niet strikt nood zakelijk zijn voor de gewenste nauw keurigheid van de algoritme.
De geschatte QFT vereist de dyadic $Z $-rotation-bewerking <xref:microsoft.quantum.intrinsic.rfrac> en de <xref:microsoft.quantum.intrinsic.h> bewerking.
Er wordt van uitgegaan dat de invoer en uitvoer worden gecodeerd in big endian encoding---dat wil zeggen dat de Qubit met de index `0` wordt gecodeerd in de meest linkse (hoogste) bit van de weer gave van een binair geheel getal.
Deze indeling wordt uitgelijnd met de [Ket-notatie](xref:microsoft.quantum.concepts.dirac), omdat het REGI ster van drie qubits in de status $ \ket {100} $ overeenkomt met $q _0 $ in de staat $ \ket {1} $, terwijl $q _1 $ en $q _2 $ de status $ \ket {0} $ heeft.
De benaderings parameter $a $ bepaalt het Pruning-niveau van de $Z $-rotations, dat wil zeggen $a \in [0.. n] $.
In dit geval worden alle $Z $-rotations $2 \ pi/2 ^ k $, waarbij $k > a $ worden verwijderd uit het QFT-circuit.
Het is bekend dat voor $k \ge \ log_2 (n) + \ log_2 (1/\epsilon) + $3. een van de kan $ \\ | \operatorname{QFT}-\operatorname{AQFT} \\ | < \epsilon $ zijn.
Hier $ \\ | \cdot \\ | $ is de operator norm die in dit geval de vierkantswortel van de grootste [eigenvalue](xref:microsoft.quantum.concepts.matrix-advanced) van $ (\operatorname{QFT}-\operatorname{AQFT}) (\operatorname{QFT}-\operatorname{AQFT}) ^ \dagger $ is.

## <a name="arithmetic"></a>Rekenkundig ##

Net zoals reken kundig een centrale rol speelt in de klassieke computing, is het ook onmisbaar voor Quantum Computing.  Algoritmen, zoals het factor algoritme voor Shor, Quantum simulatie methoden en veel oracular-algoritmen zijn afhankelijk van samenhangende reken kundige bewerkingen.  De meeste benaderingen van reken kundige builds op Quantum adder-circuits.  De eenvoudigste adder neemt een klassieke invoer $b $ en voegt de waarde toe aan een Quantum status met een geheel getal $ \ket{a} $.  Wiskundig, de adder (die we $ \operatorname{Add} (b) $ voor klassieke invoer $b $) heeft de eigenschap die

$ $ \operatorname{Add} (b) \ket{a} = \ket{a + b}.
$ $ Dit Basic adder-circuit is meer dan een incrementer dan een adder.
Het kan worden omgezet in een adder met twee Quantum invoer via $ $ \operatorname{Add}\ket{a}\ket{b} = \ket{a}\ket{a + b}, $ $ met behulp van $n $ beheerde toepassingen van adders van het formulier \begin{align} \operatorname{Add} \ket{a} \ket{b} & = \Lambda \_ {a \_ 0} \Left (\operatorname{add} (1) \Right) \Lambda \_ {a \_ 1} \left (\operatorname{add} (2) \right) \Lambda \_ {a \_ 2} \left (\operatorname{add} (4) \right) \cdots \Lambda \_ {a \_ {n-1}} \left (\operatorname{add} ({{n-1}}) \right) \ket{a}\ket{b} \\ \\ & = \ket{a} \ket{b + a}, \end{align} voor $n $-bitsinteger-gehele getallen $a $ en $b $ en modulus $2 ^ n $.  Stel dat de notatie $ \Lambda \_ x (a) $ verwijst naar de gecontroleerde versie van die bewerking $A $, met het besturings element qubit $x $ as.

Op dezelfde manier kunnen gespreide vermenigvuldiging (een modulaire vorm van essentieel voor het factor-algoritme van de Shor) worden uitgevoerd met behulp van een vergelijk bare reeks beheerde toevoegingen: \begin{align} \operatorname{Mult} (a) \ket{x}\ket{b} & = \Lambda \_ {x \_ 0} \Left (\operatorname{add} (2 ^ 0 a) \Right) \Lambda \_ {a \_ 1} \left (\operatorname{add} (2 ^ 1a) \right) \Lambda \_ {a \_ 2} \left (\operatorname{add} (2 ^ 2 a) \right) \cdots \Lambda \_ {x \_ {n-1}} \left (\operatorname{add} ({2 ^ {n-1}} a) \right) \ket{x}\ket{b} \\ \\ & = \ket{x}\ket{b + AX}.
\end{align} er is een subtlety met vermenigvuldiging op quantum computers waarvan u mogelijk merkt dat u de definitie van $ \operatorname{Mult} $ hierboven ziet.  In tegens telling tot de Quantum versie van dit circuit slaat u het product van de invoer op in een hulp registratie in plaats van in het invoer register.  In dit voor beeld wordt het REGI ster geïnitialiseerd met de waarde $b $, maar normaal gesp roken wordt de waarde nul ingedrukt.  Dit is nodig omdat in het algemeen geen multiplicative inverse is voor algemene $a $ en $x $.  Aangezien alle Quantum bewerkingen, het opslaan van metingen, kunnen worden teruggedraaid, moeten we voldoende informatie bewaren om de vermenigvuldiging ongedaan te maken.  Daarom wordt het resultaat opgeslagen in een andere matrix.  Dit leidt tot het opslaan van de uitvoer van een onomkeerbaare bewerking, zoals vermenigvuldigen, in een afzonderlijk REGI ster, ook wel bekend als ' Bennett, slag ' na Charlie Bennett,. Dit is een fundamenteel hulp middel in zowel omkeerbaar als Quantum Computing.

Er zijn veel Quantum circuits voorgesteld om toe te voegen en elke keer een ander toenemend aantal qubits (ruimte) en het aantal poort bewerkingen (tijd) dat is vereist.  We bekijken twee uiterst efficiënte adders beneden bekend als de Draper adder en de Beauregard Adder.

### <a name="draper-adder"></a>Draper Adder ###

De Draper-Adder is weliswaar een van de meest elegante Quantum adders, omdat deze direct de Quantum eigenschappen aanroept om de toevoeging uit te voeren.  Het inzicht achter de Draper Adder is dat de Fourier-trans formatie kan worden gebruikt om fase verschuivingen te vertalen naar een beetje verschuiving.  Daarna wordt een Fourier-trans formatie toegepast, waarbij de juiste fase verschuivingen worden toegepast en vervolgens de Fourier-trans formatie ongedaan wordt maakt, kunt u een adder implementeren.  In tegens telling tot veel andere adders die zijn voorgesteld, gebruikt de Draper-adder expliciet Quantum effecten die zijn geïntroduceerd via de Quantum-Fourier-trans formatie.  Het heeft geen natuurlijk klassiek tegen hanger.  De specifieke stappen van de Draper-adder worden hieronder gegeven.

Stel dat u twee $n $-bits-registers hebt waarin de gehele getallen $a $ en $b $ worden opgeslagen voor alle $a $ $ $ \operatorname{QFT}\ket{a} = \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} e ^ {i2\pi (AJ)/2 ^ n} \ket{j}.
$ $ Bij het definiëren van $ $ \ket{\phi \_ k (a)} = \frac {1} {\sqrt {2} } \left (\ket {0} + e ^ {i2\pi a/2 ^ k} \ket {1} \right), $ $ na sommige algebra ziet u dat $ $ \operatorname{QFT}\ket{a} = \ket{\phi \_ 1 (a)} \otimes \cdots \otimes \ket{\phi \_ n (a)}.
$ $ Het pad naar het uitvoeren van een adder wordt vervolgens gewist nadat u hebt gezien dat de som van de invoer kan worden geschreven als $ $ \ket{a + b} = \operatorname{QFT} ^ {-1} \ket{\phi \_ 1 (a + b)} \otimes \cdots \otimes \ket{\phi \_ n (a + b)}.
$ $ De gehele getallen $b $ en $a $ kunnen vervolgens worden toegevoegd door de controle van de gecontroleerde fase voor elk van de qubits in de ontleding uit te voeren met de bits van $b $ as-besturings elementen.

Deze uitbrei ding kan verder worden vereenvoudigd door te voor komen dat een geheel getal $j $ en reëel getal $x $, $e ^ {i2\pi (x + j)} = e ^ {i2\pi x} $.  Dit komt doordat als u $360 ^ {\circ} $ graden ($ 2 \ pi $ radialen) in een cirkel roteert, u uiteindelijk precies op de slag gaat.  Het enige belang rijk deel van $x $ voor $e ^ {i2\pi x} $ is daarom het gedeelte van $x $.  Met name als er een binaire uitbrei ding van het formulier $x = y-+0. x \_ 0x \_ 2 \ ldots x \_ n $ then $e ^ {i2\pi x} = e ^ {i2\pi (0. x \_ 0x \_ 2 \ ldots x \_ {n-1}})} $ en daarom $ $ \ket{\phi \_ k (a + b)} = \frac {1} {\sqrt {2} } \left (\ket {0} + e ^ {i2\pi [a/2 ^ k +0. b \_ K\ldots b \_ 1]} \ket {1} \right). $ $ Dit betekent dat als we een aanvulling hebben op de tensor factoren in de uitbrei ding van de Fourier-trans formatie van $ \ket{a} $, het aantal rotaties kleiner wordt naarmate $k $ afneemt.  Hierdoor wordt het aantal Quantum-Gates dat nodig is in de adder aanzienlijk verminderd.  We vermelden de Fourier-trans formatie, de toevoeging van de fase en de inverse Fourier-transformatie stappen die bestaan uit de Draper adder als $ \operatorname{QFT} ^ {-1} \left (\Phi \\ \! \operatorname{add}\right) \operatorname{QFT} $. Hieronder vindt u een Quantum circuit dat deze vereenvoudiging gebruikt om het hele proces te implementeren.

![Draper adder weer gegeven als circuit diagram](~/media/draper.svg)

Elke beheerde $e ^ {I2 \ Pi/k} in het circuit verwijst naar een poort met gecontroleerde fasen.  Dergelijke Gates hebben de eigenschap op het paar qubits waarop ze handelen, $ \ket {00} \mapsto \ket {00} $, $ \ket {11} \mapsto e ^ {I2 \ Pi/k} \ Ket {11} $.  Met dit circuit kunnen we toevoegingen uitvoeren met behulp van geen extra qubits die nodig zijn om de invoer en de uitvoer op te slaan.

### <a name="beauregard-adder"></a>Beauregard Adder ###

De Beauregard Adder is een Quantum modulaire adder die gebruikmaakt van de Draper adder om het toevoegen van modulo $N $ uit te voeren voor een wille keurige waarde, positief geheel getal $N $.  De significantie van de Quantum modulaire adders, zoals de Beauregard adder, is in grote mate gepaard met hun gebruik in de modulaire machtsverheffen-stap binnen het Shor-algoritme voor factories.  Een Quantum modulaire adder heeft de volgende actie voor de Quantum invoer $ \ket{b} $ en de klassieke invoer $a $, waarbij $a $ en $b $ zijn beloofd als integers rest $N $, wat betekent dat ze in het interval $ [0, \ldots, N-1] $ liggen.

$ $ \ket{b}\rightarrow \ket{b + a \Text{mod} N} = \begin{cases} \ket{b + a}, & b + a < N \\ \\ \ket{b + a-N}, & (b + a) \ge N \end{cases}.
$$

De Beauregard adder maakt gebruik van de Draper adder of meer specifiek $ \phi \\ \! \operatorname{add} $, om $a $ en $b $ in de fase toe te voegen.  Vervolgens wordt dezelfde bewerking gebruikt om te bepalen of $a + b <N $ wordt afgetrokken van $N $ en te testen als $a + b-N<$0.  Het circuit slaat deze informatie op in een bijkomende Qubit en voegt $N $ terug het REGI ster toe als $a + b<N $.  Vervolgens wordt het systeem afgesloten door de computer te ontlasten (deze stap is nodig om ervoor te zorgen dat de ancilla na het aanroepen van de adder niet meer kunnen worden toegewezen).  Het circuit voor de Beauregard adder wordt hieronder gegeven.

![Beauregard adder weer gegeven als circuit diagram](~/media/beau.svg)

Hier heeft de poort $ \Phi \\ \! \operatorname{add} $ hetzelfde als $ \Phi \\ \! \operatorname{add} $, behalve dat in deze context de invoer klassiek is in plaats van Quantum.  Hierdoor kunnen de bewaakte fasen in $ \Phi \\ \! \operatorname{add} $ worden vervangen door fase-Gates die vervolgens samen worden gecompileerd in minder bewerkingen om zowel het aantal qubits als het aantal poorten dat nodig is voor de adder te verminderen.

Ga voor meer informatie naar [M. Roetteler, th. Beth](http://doi.org/10.1007/s00200-008-0072-2 ) en [D. Coppersmith](https://arxiv.org/abs/quant-ph/0201067).

### <a name="quantum-phase-estimation"></a>Kwantumalgoritme voor faseschatting ###

Een bijzonder belang rijke toepassing van de Quantum Fourier Transform is het leren van de eigenvalues van unitary-Opera Tors, een probleem bekend als *fase schatting*.
Houd rekening met een unitary $U $ en een status $ \ket{\phi} $, waardoor $ \ket{\phi} $ een eigenstate van $U $ is met onbekende eigenvalue $ \phi $, \begin{Equation} U\ket {\ Phi} = \phi\ket{\phi}.
\end{Equation} als we alleen toegang hebben tot $U $ als Oracle, kunnen we de fase $ \phi $ leren door gebruik te maken van de $Z $-rotaties die zijn toegepast op het doel van een beheerde bewerking die op het besturings element wordt door gegeven.

Stel dat $V $ een beheerde toepassing is van $U $, zodanig dat \begin{align} V (\ket {0} \otimes \ket{\phi}) & = \ket {0} \otimes \ket{\phi} \\ \\ \textrm{en} V (\ket {1} \otimes \ket{\phi}) & = e ^ {i \phi} \ket \otimes {1} \ket{\phi}.
\end{align} vervolgens op lineariteit, \begin{align} V (\ket{+} \otimes \ket{\phi}) & = \frac{(\ket \otimes {0} \ket{\phi}) + e ^ {i \phi} (\ket {1} \otimes \ket{\phi})} {\sqrt {2} }.
\end{align} we kunnen voor waarden verzamelen om te vinden dat \begin{align} V (\ket{+} \otimes \ket{\phi}) & = \frac{\ket {0} + e ^ {i \phi} \ket {1} } {\sqrt {2} } \otimes \ket{\phi} \\ \\ & = (R_1 (\phi) \ket{+}) \otimes \ket{\phi}, \end{align} waarbij $R _1 $ de unitary is die door de bewerking wordt toegepast <xref:microsoft.quantum.intrinsic.r1> .
Anders is het effect van het Toep assen van $V $ precies hetzelfde als het Toep assen van $R _1 $ met een onbekende hoek, zelfs als we alleen toegang hebben tot $V $ als Oracle.
Voor de rest van deze bespreking bespreken we bijvoorbeeld de fase schatting in termen van $R _1 (\phi) $, die we implementeren met behulp van de zogenaamde *fase kickback*.

Omdat het besturings element en het doel register untangled na dit proces blijven, kunnen we $ \ket{\phi} $ opnieuw gebruiken als het doel van een beheerde toepassing van $U ^ $2 om een tweede besturings element voor een Qubit in de status $R _1 (2 \phi) \ket{+} $ voor te bereiden.
Op deze manier kunnen we een REGI ster ontvangen van de vorm \begin{align} \ket{\psi} & = \ sum_ {j = 0} ^ n R_1 (2 ^ j \phi) \ket{+} \\ \\ & \propto \ bigotimes_ {j = 0} ^ {n} \left (\ket {0} + \exp (i 2 ^ {j} \phi) \ket {1} \right) \\ \\ & \propto \ sum_ {k = 0} ^ {2 ^ n-1} \exp (i \phi k) \ket{k} \end{align} waarbij $n $ het aantal bits nauw keurig is dat nodig is, en waar we $ \propto $ hebben gebruikt {} {} om aan te geven dat de normalisatie factor $1/\sqrt{2 ^ n} $ is onderdrukt.

Als we ervan uitgaan dat $ \phi = 2 \pi p/2 ^ k $ voor een geheel getal $p $, herkennen we dit als $ \ket{\psi} = \operatorname{QFT} \ket{p_0 p_1 \dots p_n} $, waarbij $p _j $ de $j ^ {\textrm{th}} $ bit $2 \pi \phi $ is.
Wanneer de adjoint van de Quantum Fourier-trans formatie wordt toegepast, krijgen we daarom de binaire weer gave van de fase die is gecodeerd als een Quantum status.

In Q # wordt dit geïmplementeerd door de <xref:microsoft.quantum.characterization.quantumphaseestimation> bewerking, waarbij een <xref:microsoft.quantum.oracles.discreteoracle> implementatie toepassing van $U ^ m $ wordt gebruikt als een functie van positieve gehele getallen $m $.
