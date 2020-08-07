---
Titel: meerdere qubits beschrijving: meer informatie over het uitvoeren van bewerkingen op twee of meer qubits.
Auteur: QuantumWriter UID: micro soft. Quantum. concepten. Multiple-qubits MS. Author: nawiebe@microsoft.com MS. date: 12/11/2017 MS. topic: artikel no-loc:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="multiple-qubits"></a>Meerdere qubits

Hoewel single-Qubit Gates beschikken over een aantal intuïtieve functies, zoals de mogelijkheid om zich in meer dan één staat op een bepaald moment te bevinden, is het mogelijk dat er op een quantum computer sprake is van een ' single-Qubit-Gates, dan hebben we een apparaat met reken kracht die zou kunnen dwarfed door zelfs een reken machine alleen een klassieke supercomputer te laten.
De werkelijke kracht van Quantum Computing wordt alleen duidelijk naarmate we het aantal qubits verg Roten.
Deze stroom treedt deels op omdat de dimensie van de vector ruimte van Quantum status vectoren exponentieel toeneemt met het aantal qubits.
Dit betekent dat hoewel een enkelvoudige Qubit redelijk kan worden gemodelleerd, het simuleren van een quantum van 50-Qubit weliswaar de limieten van bestaande supercomputeren pusht.
Het verg Roten van de omvang van de berekening door slechts één extra Qubit *verdubbelt* het geheugen dat nodig is voor het opslaan van de status en *verdubbelt* ongeveer de reken tijd.
Dit snelle, verdubbeling van de reken kracht is waarom een quantum computer met een relatief klein aantal qubits de krach tigste super computers van vandaag, morgen en verder niet kan overschrijden voor bepaalde reken taken.

Waarom hebben we exponentiële groei voor Quantum-status vectoren?  Het doel van deze sectie is om de regels te bekijken die worden gebruikt voor het bouwen van Qubit-statussen uit Qubit-Staten en de poort bewerkingen te bespreken die in onze Gate set moeten worden opgenomen om een Universal veel-Qubit quantum-computer te vormen.
Deze hulpprogram ma's zijn absoluut nood zakelijk om inzicht te krijgen in de poort sets die vaak worden gebruikt in Q# code en om Intuition te verkrijgen over waarom Quantum effecten, zoals entanglement of interferentie, meer krachtiger zijn dan klassieke computing.

## <a name="representing-two-qubits"></a>Die twee qubits vertegenwoordigen
Het belangrijkste verschil tussen de een-en twee Qubit Staten is dat twee Qubit-Staten vier driedimensionaal zijn in plaats van twee dimensies.
Dit komt doordat de reken kundige basis voor twee Qubit Staten wordt gevormd door de tensor-producten van een Qubit-status.  We hebben bijvoorbeeld\begin{align}
00 \equiv \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 1 0 0 \end{bmatrix} & = \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} , \qquad 01 \equiv \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \\\\ \end{bmatrix} ,\\\\
10 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 0 0 \end{bmatrix} & = \begin{bmatrix} \\\\ \\\\ 1 \\\\ 0 \end{bmatrix} , \qquad 11 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 0 \\\\ 0 \\\\ 1 \end{bmatrix} .
\end{align}

Het is eenvoudig om te zien dat de Quantum status van n qubits in de meeste gevallen $ $ wordt vertegenwoordigd door een eenheids vector van dimensie $ 2 ^ n $ met behulp van deze constructie.  De vector

$$
\begin{bmatrix}\alpha _ { 00 } 01 \\\\ 10 \alpha   _ { } \\\\ \alpha _ { 11 } \\\\ \alpha   _ { }  \end{bmatrix}
$$

Dit object vertegenwoordigt een Quantum status op twee qubits als $ | \alpha _ { 00 } | ^ | \alpha 2 +_ { 01 } | ^ 2 + | \alpha _ { 10 } | ^ | \alpha 2 +_ { 11 } | ^ 2 = 1 $ . Net als bij één qubits bevat de Quantum status vector van meerdere qubits alle informatie die nodig is om het gedrag van het systeem te beschrijven.

Als we twee afzonderlijke qubits ontvangen, een in de staat $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ en een tweede Qubit in de staat $ \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $ , wordt de bijbehorende status van twee Qubit    

$$
\begin{bmatrix} \alpha \\\\  \beta \end{bmatrix} \otimes \begin{bmatrix} \gamma \\\\  \delta \end{bmatrix} 
=\begin{bmatrix} \alpha \begin{bmatrix} \gamma \\\\  \delta \end{bmatrix} \\\\ \beta \begin{bmatrix}\gamma \\\\  \delta \end{bmatrix} \end{bmatrix}
= \begin{bmatrix} \alpha\gamma \\\\  \alpha\delta \\\\  \beta\gamma \\\\  \beta\delta \end{bmatrix}, $$

waarbij de bewerking $ \otimes $ het tensor-product (of het Kronecker-product) van vectoren wordt genoemd. Houd er rekening mee dat we het tensor-product van twee statussen met één Qubit in staat stellen om een status van twee Qubit te vormen, maar niet alle twee Qubit-Quantum waarden kunnen worden geschreven als het tensor product van twee single-Qubit Staten.
Er zijn bijvoorbeeld geen statussen $ \psi = \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ en $ \phi = \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $ zo dat hun tensor-product de status is     

$$\psi\otimes\phi = \begin{bmatrix} 1/ \sqrt { 2 } \\\\ 0 \\\\ 0 \\\\ / \sqrt { 2 } \end{bmatrix} .$$ 

Een dergelijke status van twee Qubit, die niet kan worden geschreven als het tensor-product van single-Qubit statussen, wordt ' Entangled State ' genoemd. de twee qubits zijn gezegd als [*Entangled*](https://en.wikipedia.org/wiki/Quantum_entanglement).  Zonder enige spraak, omdat de Quantum status niet kan worden beschouwd als een tensor product van één Qubit-status, wordt de informatie die de status heeft, niet naar een van de qubits afzonderlijk beperkt.  In plaats daarvan wordt de informatie niet lokaal opgeslagen in de correlaties tussen de twee staten.  Deze niet-localiteit van informatie is een van de belangrijkste onderscheidings functies van Quantum Computing ten opzichte van klassiek computing en is essentieel voor een aantal Quantum protocollen, waaronder [Quantum-teleportie](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/teleportation) en [Quantum fout correctie](xref:microsoft.quantum.libraries.error-correction).

## <a name="measuring-two-qubit-states"></a>Meting van twee Qubit Staten ##
Het meten van twee Qubit Staten lijkt veel op de metingen met één Qubit. De status meten

$$
    \begin{bmatrix}
        \alpha_ { 00 } 01 \\\\ \alpha _ { }\\\\ 
        \alpha_ { 10 } 11 \\\\ \alpha _ {}
    \end{bmatrix}
$$

resulteert $ in 00 $ met kans $ | \alpha _ { 00 } | ^ 2 $ , $ 01 $ met $ kans | \alpha _ { 01 } | ^ 2 $ , $ 10 $ met kans $ | \alpha _ { 10 } | ^ 2 $ en $ 11 $ met kans $ 11 ^ 2. | \alpha _ { } | $ De variabelen $ \alpha _ { 00 } , \alpha _ { 01 } , \alpha _ { 10 } $ en $ 11 hebben een opzettelijke naam om deze verbinding duidelijk te maken \alpha _ { } $ . Als de uitkomst na de meting 00 is $ , $ is de Quantum status van het systeem met twee Qubit samengevouwen en nu

$$
    00:00\equiv
    \begin{bmatrix}
        i\\\\ 
        0,3\\\\ 
        0,3\\\\ 
        0 \end{bmatrix} .
$$

Het is ook mogelijk slechts één Qubit van een Quantum-status van twee Qubit te meten. In gevallen waarbij u slechts één van de qubits meet, is de impact van de meting subtiel verschillend, omdat de gehele status niet wordt samengevouwen in een reken kundige status, en niet wordt samengevouwen tot slechts één subsysteem.  Met andere woorden, in dergelijke gevallen waarbij slechts één Qubit wordt gewerkt, wordt slechts een van de subsystemen, maar niet alle, samengevouwen.  

Om dit te zien, moet u de eerste Qubit van de volgende status meten, die wordt gevormd door het Toep assen van de Hadamard Transform $ H $ op twee qubits in eerste instantie ingesteld op de status "0":$$
H ^ 2 (1 0 1 0) 1 2 1 1 1 1-1 1-1, 1 1-1-1 1-1 – 1 1 1 0 0 0 1 2 1 1 1 als resultaat { \otimes } \left \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \right = \frac { } { } \begin{bmatrix} & & & \\\\ & & & \\\\ & & & \\\\ & & & \end{bmatrix} \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} = \frac { } { } \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \mapsto \begin{cases} \text { } = 0 & \frac { 1 } { \sqrt { 2 1 } } \begin{bmatrix} \\\\ 1 \\\\ 0 \\\\ 0 \end{bmatrix} \\\\ \text { resultaat } = 1 & \frac { 1 } { \sqrt { 2 } } \begin{bmatrix} 0 \\\\ 0 \\\\ 1 \\\\ 1 \end{bmatrix} \\\\ \end{cases} .  
$$
Beide resultaten hebben een kans van 50%.  Het resultaat van 50% waarschijnlijk voor beide kunnen worden afgeleid van het feit dat de initiële Quantum State vector invariant is onder het wisselen $ $ van 0 met $ 1 $ op de eerste Qubit.

De wiskundige regel voor het meten van de eerste of tweede Qubit is eenvoudig.  Als we $ e_k $ de $ k ^ \rm van de { } $ reken kundige basis vector en $ $ de set van alle $ e_k zodanig zijn $ dat de betreffende Qubit de waarde 1 heeft $ $ voor die waarde van $ k $ .  Als we bijvoorbeeld de eerste Qubit willen meten, $ $ bestaan S uit $ e_1 \equiv 10 $ en $ e_3 \equiv 11 $ .  En als we geïnteresseerd zijn in de tweede Qubit $ S $ , bestaat er uit $ e_2 \equiv 01 $ en $ e_3 \equiv 11 $ .  De waarschijnlijkheid om de gekozen Qubit te meten als $ 1 $ is voor status vector$\psi$

$$
P ( \text { resultaat } = 1) = \sum _ { e_k \text { in de set } S } \psi ^ \dagger e_k e_k ^ \dagger \psi .
$$

> [!NOTE]
>In dit document gebruiken we de indeling little-endian voor het labelen van de reken kundige basis. In little endian indeling zijn de minst significante bits het eerst. Bijvoorbeeld, het getal vier in de indeling little-endian wordt vertegenwoordigd door de teken reeks van bits 001.

Aangezien elke qubit-meting alleen $ 0 of 1 kan opleveren $ $ $ , is de kans op het meten van $ 0 slechts $ $ 1-P ( \text { resultaat } = 1) $ .  Daarom geven we alleen expliciet een formule voor de kans op het meten van $ 1 $ .

De actie die een dergelijke meting op de status heeft, kan wiskundig worden uitgedrukt als

$$
\psi\mapsto \frac{\sum _ { e_k \text { in de set } S } e_k e_k ^ \dagger \psi } { \sqrt { P ( \text { resultaat } = 1) } } .
$$

De voorzichtigste lezer kan zich zorgen maken over wat er gebeurt wanneer de kans van de meting nul is.  Hoewel de resulterende status technisch niet is gedefinieerd in dit geval, hoeft u zich geen zorgen te maken over dergelijke gevallen, omdat de kans nul is.


Als we $ \psi $ de uniforme status vector hebben ontvangen die hierboven is gegeven, is het belang rijk om de eerste Qubit te meten. 

$$
P ( \text { meting van de eerste Qubit } = 1) = ( \psi ^ \dagger e_1) (e_1 ^ \dagger \psi ) + ( \psi ^ \dagger e_3) (e_3 ^ \dagger \psi ) = | e_1 ^ \dagger \psi | ^ 2 + | e_3 ^ \dagger \psi | ^ 2.
$$

Houd er rekening mee dat dit slechts de som is van de twee waarschijnlijkheden die zouden kunnen worden verwacht voor het meten van de resultaten $ 10 $ en $ 11, alle qubits die moeten $ worden gemeten.
In ons voor beeld evalueert dit naar

$$
\frac{1 } { 4 } \left | \begin{bmatrix} 0 & 0 & 1 & 0 1 1% 1 \end{bmatrix} \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \right | ^ 2 + \frac { 1 4 0 0 } { } \left | \begin{bmatrix} & 0 1 1 1 & & \end{bmatrix} \begin{bmatrix} \\\\ \\\\ \\\\ \end{bmatrix} \right | ^ 2 = \frac { 1 } { 2 } .
$$

wat precies overeenkomt met wat onze Intuition vertelt, zou ons moeten zijn.  Op dezelfde manier kan de status worden geschreven als

$$
\frac{\frac{e_1 } { 2 } + \frac { e_3 } { 2 } } { \sqrt { \frac { 1 2 } { } } } = \frac { 1 } { \sqrt { 2 } } \begin{bmatrix} 0 \\\\ 0 \\\\ 1 \\\\ 1\end{bmatrix}
$$

opnieuw in overeenstemming met onze intuition.

## <a name="two-qubit-operations"></a>Twee Qubit bewerkingen
Net als bij een single-Qubit-trans formatie is elke unitary-Transform een geldige bewerking op qubits. Over het algemeen is een unitary-trans formatie op $ n $ qubits een matrix $ U $ met een grootte van $ 2 ^ n \times 2 ^ n $ (zodat deze wordt toegepast op vectoren met een grootte van $ 2 ^ n $ ), zodat $ u ^ { -1 } = U ^ \dagger $ .
De poort CNOT (Controlled-NOT) is bijvoorbeeld een gang bare twee Qubit-poort en wordt vertegenwoordigd door de volgende unitary-matrix:

$$
\operatorname{CNOT 1 \ 0 \ 0 \ 0 } = \begin{bmatrix} \\\\ 0 \ 1 \ 0 \ 0 \\\\ 0 \ 0 \ 0 \ 1 \\\\ 0 \ 0 \ 1 \ 0\end{bmatrix}
$$

We kunnen ook twee Qubit-poorten vormen door enkelvoudige Qubit-poorten op beide qubits toe te passen. Als we de Gates bijvoorbeeld Toep assen 

$$
\begin{bmatrix}
a \ b \\\\ c \ d\end{bmatrix}
$$

en

$$\begin{bmatrix}
e \ f \\\\ g \ h\end{bmatrix}
$$

op de eerste en tweede qubits is dit gelijk aan het Toep assen van de twee Qubit unitary die door hun tensor-product worden verstrekt:$$\begin{bmatrix}
a \ b \\\\ c \ d\end{bmatrix}
\otimes 
\begin{bmatrix}
e \ f \\\\ g \ h\end{bmatrix}=
    \begin{bmatrix}
    AE \ af \ BF\\\\
    AG \ ah \ BG \ BH\\\\
    CE \ CF \ de \ DF\\\\
    CG \ CH \ DG \ DH \end{bmatrix} .$$
Daarom kunnen we twee Qubit-poorten vormen door het tensor-product van een aantal bekende single-Qubit-poorten te nemen. Enkele voor beelden van twee Qubit-Gates zijn $ h \otimes h $ , X en $ \otimes \boldone $ $ x \otimes Z $ .

Houd er rekening mee dat hoewel er twee single-Qubit Gates een twee-Qubit poort definiëren door hun tensor-product te nemen. Niet alle twee Qubit-poorten kunnen worden geschreven als het tensor-product van single-Qubit Gates.  Een dergelijke poort wordt een *entangling* -poort genoemd. Een voor beeld van een entangling-Gate is de CNOT-poort.

De Intuition achter een Controlled-not-Gate kan worden gegeneraliseerd met wille keurige poorten.  Een beheerde poort in het algemeen is een poort die als identiteit fungeert (Internet Explorer heeft geen actie), tenzij een specifieke Qubit $ 1 is $ .  We geven een beheerde unitary aan, die in dit geval wordt gecontroleerd op de Qubit $ met de naam x $ , met een $ \Lambda \_ x (U) $ .  Als voor beeld $ \Lambda van een _0 (u) e \_ { 1 } \otimes { \psi } = e 1 \_ { } \otimes u { \psi } $ en $ \Lambda \_ 0 (u) e 0 \_ { } \otimes { \psi } = \_ { } \otimes { \psi } $ , waarbij $ e \_ 0 $ en $ e \_ 1 $ zijn de reken kundige basis vectoren voor één Qubit die overeenkomt met de waarden $ 0 $ en $ 1 $ .  Denk bijvoorbeeld aan de volgende Controlled- $ Z- $ Gate, waarna we dit kunnen uitdrukken als$$
\Lambda\_0 (Z) 1 0 0 0 0 1 0 0 0 0 = \begin{bmatrix} & 1 0 0 0 & & \\\\ & & & \\\\ & & & \\\\ & & & -1 \end{bmatrix} = ( \boldone \otimes h) \operatorname { CNOT } ( \boldone \otimes h).
$$

Het bouwen van beheerde unitaries op een efficiënte manier is een belang rijke uitdaging.  De eenvoudigste manier om dit te implementeren vereist het maken van een Data Base met gestuurde versies van fundamentele Gates en het vervangen van elke fundamentele poort in de oorspronkelijke unitary-bewerking met de gecontroleerde tegen hanger.  Dit is vaak zeer verspilling en slim inzicht kan worden gebruikt om alleen een aantal poorten met gecontroleerde versies te vervangen om dezelfde gevolgen te verkrijgen.  Daarom bieden we in ons Framework de mogelijkheid om de Naïve-methode voor het beheren of toestaan van de gebruiker om een gecontroleerde versie van de unitary te definiëren als een geoptimaliseerde, afgestemde versie bekend is.

Poorten kunnen ook worden beheerd met behulp van klassieke informatie.  Een klassiek niet-Gate is bijvoorbeeld gewoon een gewone not-Gate, maar wordt alleen toegepast als een klassieke bit 1 is in $ $ plaats van een Quantum bit.  In deze zin kan een klassieke beheerde poort worden beschouwd als een if-instructie in de Quantum code, waarbij de poort alleen in één vertakking van de code wordt toegepast.


Net als bij de single-qubite-case is een Qubit-poort set Universal als een wille keurige $ 4 \times 4 $ unitary matrix kan worden benaderd door een product van poorten van deze set tot een wille keurige precisie.
Een voor beeld van een universele Gate set is de Hadamard-poort, de T-poort en de CNOT-poort. Door producten van deze Gates te nemen, kunnen we een wille keurige unitary-matrix op twee qubits benaderen.

## <a name="many-qubit-systems"></a>Veel Qubit systemen
We volgen precies dezelfde patronen in de tweequbite Case voor het bouwen van veel Qubit Quantum-statussen van kleinere systemen.  Dergelijke statussen zijn gebouwd door tensor producten van kleinere staten te maken.  U kunt bijvoorbeeld de bits teken reeks $ 1011001 $ in een quantum computer coderen.  We kunnen dit coderen als

$$
1011001 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} .
$$

Quantum Gates werken op dezelfde manier.  Als we bijvoorbeeld de X-poort willen Toep $ assen $ op de eerste Qubit en vervolgens een CNOT tussen de tweede en derde qubits uitvoeren, kunnen we deze trans formatie uitdrukken als

\begin{align}
&(X \otimes \operatorname { CNOT } _ { 12 } \otimes \boldone \otimes \boldone \otimes \boldone \otimes \boldone ) \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 0 \end{bmatrix} \otimes \begin{bmatrix} \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} \\\\ \end{bmatrix} \otimes \begin{bmatrix} \\\\ 1 0 0 1\end{bmatrix}\\\\
&\qquad\qquad\equiv0011001.\end{align}

In veel Qubit-systemen is het vaak nodig om qubits toe te wijzen en te detoewijzen die als tijdelijk geheugen voor de quantum computer fungeren.  Een dergelijke Qubit wordt een ancilla genoemd.  Standaard gaan we ervan uit dat de status van de Qubit is geïnitialiseerd voor $ e_0 $ bij toewijzing.  We gaan ervan uit dat deze opnieuw wordt geretourneerd naar e_0 voordat de toewijzing ongedaan wordt maakt $ $ .  Deze veronderstelling is belang rijk omdat als er een ancilla-Qubit wordt Entangled met een andere Qubit-registratie wanneer de toewijzing wordt opgeheven, de ancilla wordt beschadigd.  Daarom wordt altijd aangenomen dat dergelijke qubits zijn teruggezet naar de oorspronkelijke status voordat ze worden vrijgegeven.

Ten slotte moeten er nieuwe poorten worden toegevoegd aan onze Gate-set voor het maken van Universal quantum computing voor twee Qubit quantum computers, maar moeten er geen nieuwe poorten worden geïntroduceerd in de multi-Qubit-case.  De poorten $ H $ , $ T $ en CNOT vormen een universele poort die is ingesteld op veel qubits, omdat een algemene unitary-trans formatie kan worden opgesplitst in een reeks van twee Qubit rotaties.  Vervolgens kunnen we gebruikmaken van de theorie die is ontwikkeld voor de twee qubite cases en deze hier opnieuw gebruiken als we veel qubits hebben.

Hoewel de lineaire algebraic notatie die we tot nu toe hebben gebruikt, kan worden gebruikt om de statussen voor meerdere Qubit te beschrijven, wordt het lastiger om de grootte van de statussen te verg Roten.  De resulterende kolom-vector voor een 7-bits teken reeks is bijvoorbeeld $ 128 $ Dimension, waardoor deze wordt omgeleid met behulp van de notatie die voorheen zeer lastig is beschreven.  Daarom pres teren we een gemeen schappelijke notatie in Quantum Computing, waarmee we deze zeer dimensionale vectoren beknopt kunnen beschrijven.
