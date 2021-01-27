---
Titel: beschrijving van de Dirac-notatie: meer informatie over het gebruik van de Dirac-notatie om Quantum-waarden weer te geven en om Quantum bewerkingen te simuleren.
Auteur: QuantumWriter UID: micro soft. Quantum. concepten. Dirac MS. Author: v-benbra MS. date: 12/11/2017 MS. topic: conceptuele no-loc:
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

# <a name="dirac-notation"></a>Dirac-notatie

Hoewel de column vector-notatie in lineaire algebra alomtegenwoordige is, is het vaak lastig in Quantum Computing, met name bij het omgaan met meerdere qubits.  Als we bijvoorbeeld definiëren $ \psi $ dat ze een vector zijn, is het niet expliciet duidelijk of er $ \psi $ een rij of kolom vector is.  Als $ \phi $ er dus $ \psi $ vectoren zijn, is het even onduidelijk als deze $ \phi \psi $ zelfs is gedefinieerd, omdat de vormen van $ \phi $ en $ \psi $ mogelijk onduidelijk zijn in de context.  Behalve de dubbel zinnigheid van de vormen van vectoren kunnen zelfs eenvoudige vectoren met de lineaire algebraic-notatie die eerder is geïntroduceerd, zeer lastig zijn. Als we bijvoorbeeld $ $ de status n-Qubit willen beschrijven waarbij elke qubit de waarde $ 0 heeft $ , wordt de status formeel als volgt weer geven: 

$$\begin{bmatrix}1 \\\\ 0 \end{bmatrix} \otimes \cdots \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} . $$  

Het is niet praktisch om dit tensor-product te evalueren omdat de vector zich in een exponentieel grote ruimte bevindt, zodat deze notatie in feite de beste beschrijving is van de status die kan worden opgegeven met de vorige notatie.  

Met de [*Dirac-notatie*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) worden deze problemen opgelost door een nieuwe taal te presen teren aan de nauw keurige behoeften van Quantum monteurs.  Daarom raden we u aan om de voor beelden in deze sectie niet weer te geven als een niet-buigzame recept over het beschrijven van Quantum Staten, maar u kunt het beste de lezer aanmoedigen om deze te bekijken als suggesties die kunnen worden gebruikt om de Quantum ideeën beknopt te maken.

Er zijn twee typen vectoren in de Dirac-notatie: de *Bra* -vector en de *Ket* -vector, dus met de naam, omdat deze samen een *remmen* of binnenste product vormen.  Als $ \psi $ een kolom vector is, kunnen we deze in de Dirac-notatie opslaan als $ \ket { \psi } $ , waarbij de \cdot geeft aan $ \ket { } $ dat het een eenheid kolom vector is, dat wil zeggen een *Ket* -vector.  Op dezelfde manier wordt de rij-Vector $ \psi ^ \dagger $ uitgedrukt als $ \bra { \psi } $ . Met andere woorden, $ \psi ^ \dagger $ die worden verkregen door het Toep assen van een conjugation complexe gegevens op de elementen van de getransponeerde $ \psi $ . De bra-ket-notatie houdt in dat $ \braket { \psi | \psi } $ het binnenste product van een vector $ \psi $ met zichzelf is, dat is per definitie $ 1 $ .  

Meer in het algemeen, als $ \psi $ en de $ \phi $ Quantum status vectoren hun binnenste product is, is dat $ \braket { \phi | \psi } $ impliceert dat de kans op het meten van de status $ \ket { \psi } $ $ \ket { \phi } $ is $ | \braket { \phi | \psi } | ^ 2 $ .  

De volgende Conventie wordt gebruikt voor het beschrijven van de Quantum statussen die de waarden van nul en één coderen (de berekenings grondslagen met één Qubit):

$$
\begin{bmatrix}1 \\\\ 0 \end{bmatrix} = \ket { 0 } ,\qquad
\begin{bmatrix}0 \\\\ 1 \end{bmatrix} = \ket { 1 } .
$$

### <a name="example-representing-the-hadamard-operation-with-dirac-notation"></a>Voor beeld: vertegenwoordigt de bewerking Hadamard met Dirac-notatie

De volgende notatie wordt vaak gebruikt voor het beschrijven van de statussen die het gevolg zijn van het Toep assen van de Hadamard-Gate op $ \ket { 0 } $ en $ \ket { 1 } $ (die overeenkomen met de eenheids vectoren in de $ x $ $ -en-x- $ richting van de Bloch-bol):

$$
\frac{1 } { \sqrt { 2 1 } } \begin{bmatrix} \\\\ \end{bmatrix} = uur \ket { 0 } = \ket { + } ,\qquad
\frac{1 } { \sqrt { 2 } } \begin{bmatrix} 1 \\\\ t/ \end{bmatrix} = m 1 uur \ket { } = \ket { - } .
$$

Deze statussen kunnen ook worden uitgebreid met behulp van de Dirac-notatie als som van $ \ket { 0 } $ en $ \ket { 1 } $ :

$$
\ket{+}= \frac{ 1 } { \sqrt { 2 } } ( \ket { 0 }  +  \ket { 1 } ), \qquad \ket { - } = \frac { 1 } { \sqrt { 2 } } ( \ket { 0 }  -  \ket { 1 } ).
$$

### <a name="computational-basis-vectors"></a>Reken kundige basis vectoren

Dit laat zien waarom deze staten vaak een *berekening* worden genoemd: elke Quantum status kan altijd worden uitgedrukt als som van de reken kundige basis vectoren en dergelijke sommen kunnen eenvoudig worden weer gegeven met behulp van de Dirac-notatie.  De omgekeerde is ook waar de Staten $ \ket { + } $ en $ \ket { - } $ vormen ook een basis voor Quantum Staten.  U kunt dit zien uit het feit dat

$$
\ket{0 } = \frac { 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ), \qquad \ket { 1 } = \frac { 1 } { \sqrt { 2 } } ( \ket { + }  -  \ket { - } ).
$$

Als voor beeld van een Dirac-notatie moet u de rem $ \braket { 0 | 1 overwegen } $ . Dit is het binnenste product tussen $ 0 $ en $ 1 $ .  Het kan worden geschreven als 

$$
\braket{0 | 1 } = \begin{bmatrix} 1 & 0 0 \end{bmatrix} \begin{bmatrix} \\\\ 1 \end{bmatrix} = 0.
$$

Dit betekent dat $ \ket { 0 } $ en $ \ket { 1 een } $ orthogonale vector zijn, wat inhoudt dat $ \braket { 0 | 1 } = \braket { 1 | 0 } = $ 0 is.  Ook per definitie $ \braket { 0 | 0 } = \braket { 1 | 1 } = $ , wat betekent dat de twee reken kundige basis vectoren ook *orthonormal* kunnen worden genoemd.

Deze orthonormal-eigenschappen zijn handig in het volgende voor beeld. Als we $ \ket { \psi } = { \frac { de status 3 } { 5 } } \ket { 1 }  +  { \frac { 4 } { 5 } } \ket { 0 hebben } $ , omdat $ \braket { 1 | 0 } = 0 $ de kans van meting $ 1 $ is 

$$
\big|\braket{1 | \psi } \big | ^ 2 = \left | \frac { 3 } { 5 } \braket { 1 | 1 }  + \frac { 4 } { 5 } \braket { 1 | 0 } \right | ^ 2 = \frac { 9 } { 25 } .
$$

### <a name="tensor-product-notation"></a>Tensor-product notatie

De notatie Dirac bevat ook een impliciete tensor-product structuur.  Dit is belang rijk omdat in de quantum computing de status vector die wordt beschreven door twee niet-gecorreleerde Quantum registers, de tensor-producten van de twee status vectoren zijn.  Een beknoptere beschrijving van de tensor-product structuur of het ontbreken daarvan is essentieel als u een Quantum berekening wilt uitleggen.  De tensor-product structuur impliceert dat we kunnen schrijven $ \psi \otimes \phi $ voor twee Quantum status vectoren $ \phi $ en $ \psi $ als $ \ket { \psi } \ket { \phi } $ , soms expliciet geschreven als $ \ket { \psi } \otimes \ket { \phi } $ , maar door $ \otimes $ het schrijven tussen de vectoren is niet nodig.  De status waarbij bijvoorbeeld twee qubits is geïnitialiseerd op de status nul, wordt gegeven door

$$
\begin{bmatrix}1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \ket { } \otimes \ket { } = \ket { } \ket { } 0 0 0 0.
$$

Op dezelfde manier staat de status $ \ket { p } $ voor geheel getal $ p voor $ een Quantum status die de binaire weer gave van het gehele getal p versleutelt $ $ .  Als we het nummer 5 willen uitdrukken $ $ met behulp van een niet-ondertekende binaire code ring, kunnen we het ook even uitdrukken als

$$
\ket{1 } \ket { 0 } \ket { 1 } = \ket { 101 } = \ket { 5 } .
$$

Binnen deze Notation $ \ket { } $ mag 0 niet verwijzen naar een single-Qubit-status, maar een *Qubit-REGI ster* slaat een binaire code ring van $ 0 op $ .  De verschillen tussen deze twee notaties zijn meestal duidelijk uit de context.  Deze Conventie is handig voor het vereenvoudigen van het eerste voor beeld dat op een van de volgende manieren kan worden geschreven:

$$
\begin{bmatrix}1 \\\\ 0 1 0 0 0 0 0 \end{bmatrix} \otimes \cdots \otimes \begin{bmatrix} \\\\ \end{bmatrix} = \ket { } \otimes \cdots \otimes \ket { } = | \cdots \rangle = \ket { 0 } ^ { \otimes n } = \ket { 0 } .
$$

### <a name="example-describing-superposition-with-dirac-notation"></a>Voor beeld: de superpositie beschrijven met de Dirac-notatie

Als een ander voor beeld van hoe u Dirac-notatie kunt gebruiken om een Quantum status te beschrijven, moet u rekening houden met de volgende gelijkwaardige manieren om een Quantum status te schrijven die een gelijke superpositie is boven elke mogelijke bit-reeks van lengte $ n$

$$
H ^ { \otimes n } \ket { 0 } = \frac { 1 } { 2 ^ { n/2 } } \sum _ { j = 0 } ^ { 2 ^ n-1 } \ket { j } = \ket { + } ^ { \otimes n } .
$$

U vraagt zich misschien af waarom de som van $ 0 $ tot $ 2 ^ { n } -1 $ voor $ n $ bits loopt.  Houd er rekening mee dat er $ 2 ^ { n } $ verschillende configuraties zijn die $ n $ bits kunnen uitvoeren.  U kunt dit zien door aan te geven dat de ene bit twee waarden kan aannemen $ $ , maar dat twee bits $ vier waarden kunnen aannemen, enzovoort $ . Over het algemeen betekent dit dat er $ 2 ^ n $ verschillende mogelijke bits teken reeksen zijn, maar de grootste waarde die is gecodeerd in een van deze $ 1 \cdots 1 = ^ n-1 $ , en dus de bovengrens voor de som.
In dit voor beeld hebben we geen gebruik gemaakt van $ \ket { + } ^ { \otimes n } = \ket { + } $ ten opzichte van $ \ket { 0 } ^ { \otimes n } = \ket { 0, } $ omdat deze notatie Conventie doorgaans is gereserveerd voor de status van de reken kundige basis waarbij elke qubit is geïnitialiseerd op nul.  Hoewel een dergelijke Conventie in dit geval verstandig is, wordt deze niet in de Quantum Computing-documentatie gebruikt.

### <a name="expressing-linearity-with-dirac-notation"></a>Lineair uitdrukken met Dirac-notatie

Een andere leuke functie van de Dirac-notatie is het feit dat deze lineair is.  Als we willen schrijven voor een van de vier Quantum status vectoren, 

$$( \alpha \ket { \psi }  + \beta \ket { \phi } ) \otimes ( \gamma \ket { \chi }  +  \delta \ket { \omega } ) = \alpha \gamma \ket { \psi } \ket { \chi }  +  \alpha \delta \ket { \psi } \ket { \omega } + \beta \gamma \ket { \phi } \ket { \chi } + \beta \delta \ket { \phi } \ket { \omega } .$$

Dat wil zeggen dat u de tensor-product notatie kunt distribueren in de Dirac-notatie zodat tensor-producten tussen status vectoren elkaar oplopen op dezelfde manier als normale vermenigvuldiging.

Bra-vectoren volgen een vergelijk bare Conventie voor ket-vectoren.  De vector $ \bra { \psi } \bra { \phi } $ is bijvoorbeeld gelijk aan de status Vector $ \psi ^ \dagger \otimes \phi ^ \dagger = ( \psi \otimes \phi ) ^ \dagger $ . Als de Ket $ \ket { \psi } $ -Vector $ \alpha \ket { 0 1 is, }  +  \beta \ket { } $ is de Bra vector versie van de vector $ \bra { \psi } = \ket { \psi } ^ \dagger = ( \bra { 0 } \alpha ^ * + \bra { 1 } \beta ^ *) $ .

Stel dat we de kans willen berekenen dat de status $ \ket { \psi } = \frac { 3 } { 5 } \ket { 1 }  +  \frac { 4 } { 5 0 wordt gemeten } \ket { } $ met behulp van een Quantum programma voor het meten van de status van ofwel $ \ket { + } $ of $ \ket { - } $ . Vervolgens $ \ket { - } $ wordt de kans dat het apparaat zou worden uitgevoerd en dat de status is 

$$|\braket{- |\psi}| ^ 2 = \left | \frac { 1 } { \sqrt { 2 } } ( \bra { 0 }  -  \bra { 1 } ) ( \frac { 3 } { 5 } \ket { 1 }  +  \frac { 4 } { 5 } \ket { 0 } ) \right | ^ 2 = \left | - \frac { 3 } { 5 \sqrt { 2 } }  +  \frac { 4 } { 5 \sqrt { 2 } } \right | ^ 2 = \frac { 1 } { 50 } .$$

Het feit dat het negatieve teken in de berekening van de kans wordt weer gegeven, is een manifest van Quantum interferentie, een van de mechanismen waarmee quantum computing voor delen ten opzichte van het klassieke computer gebruik verkrijgt.

## <a name="ketbra-or-outer-product"></a>ketbra of buiten product

De uiteindelijke waarde voor het bespreken van de Dirac-notatie is de *ketbra* of het buitenste product.  Het buitenste product wordt weer gegeven in Dirac-notaties als $ \ket { \psi } \bra { \phi } $ en wordt ook wel ketbras genoemd, omdat de Bras en Kets in de tegenovergestelde volg orde als brakets optreden.  Het buitenste product wordt gedefinieerd via matrix vermenigvuldiging als $ \ket { \psi } \bra { \phi } = \psi \phi ^ \dagger $ voor Quantum status vectoren $ \psi $ en $ \phi $ .  Het eenvoudigste en weliswaar meest voorkomende voor beeld van deze notatie is

$$
\ket{0 } \bra { 0 } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \begin{bmatrix} 1 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\\\ 0 & 0 \end{bmatrix} \qquad \ket { 1 } \bra { 1 } = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \begin{bmatrix} 0 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\\\ 0 & 1 \end{bmatrix} .
$$

Ketbras worden vaak projectors genoemd omdat ze een Quantum status op een vaste waarde projecteren.  Aangezien deze bewerkingen niet unitary zijn (en niet zelfs de norm van een vector behouden), zou het moeten zijn om te voor komen dat een quantum computer een projector niet kan Toep assen.  Projectors maken echter een mooie taak van het beschrijven van de actie die meting heeft op een Quantum status.  Als we bijvoorbeeld een staat meten als $ \ket { \psi } $ $ 0 $ , wordt de resulterende trans formatie die de status heeft gegenereerd als gevolg van de meting

  $$\ket{\psi}\right \frac pijl { ( \ket { 0 } \bra { 0 } ) \ket { \psi } } { | \braket { 0 | \psi } | } = \ket { 0 } ,$$

Als er wordt verwacht dat u de status moet meten en deze moet worden gevonden als $ \ket { 0 } $ .  Als u wilt herhalen, kunnen dergelijke projecters niet deterministisch worden toegepast op een status in een quantum computer.  In plaats daarvan kunnen ze op een wille keurige manier worden toegepast met het resultaat $ \ket { 0 } $ met een bepaalde vaste kans.  De waarschijnlijkheid van een dergelijke meting kan worden geschreven als de verwachte waarde van de Quantum projector in de status

$$
\bra{\psi}( \ket { 0 } \bra { 0 } ) \ket { \psi } = | \braket { \psi | 0 } | ^ 2,$$

Hiermee wordt aangegeven dat projecters een nieuwe manier bieden om het meting proces uit te drukken.

Als we overwegen om de eerste Qubit van een Qubit-status te meten in plaats van $ 1, $ kunnen we dit proces ook op gemakkelijke wijze beschrijven met projectors en Dirac notatie:

$$
P ( \text { eerste Qubit = 1 } ) = \bra { \psi } \left ( \ket { 1 } \bra { 1 } \otimes \boldone ^ { \otimes n-1 } \right ) \ket { \psi } .
$$

Hier kan de identiteits matrix gemakkelijk worden geschreven in de Dirac-notatie als

$$
\boldone= \ket{ 0 } \bra { 0 1 1 1 } + \ket { } \bra { } = \begin{bmatrix} & 0 \\\\ 0 & 1 \end{bmatrix} .
$$

Voor het geval dat er twee qubits zijn, kan de projector worden uitgebreid als 

$$
\ket{1 } \bra { 1 1 } \otimes \id = \ket { } \bra { } \otimes ( \ket { 0 } \bra { 0 } + \ket { 1 } \bra { 1 } ) = \ket { 10 } \bra { 10 }  +  \ket { 11 } \bra { 11 } .
$$

Vervolgens kunnen we zien dat dit consistent is met de discussie over mogelijke meet kansen voor multiqubit-statussen met behulp van de kolom vector notatie:

$$
P ( \text { eerste Qubit = 1 } ) = \psi ^ \dagger (e \_ { 10 } e \_ { 10 } ^ \dagger + e \_ { 11 } e \_ { 11 } ^ \dagger ) \psi = | e \_ { 10 } ^ \dagger \psi | ^ 2 + | e \_ { 11 } ^ \dagger \psi | ^ 2,$$

die overeenkomt met de multi-Qubit-meting discussie.  De generalisatie van dit resultaat op de multi-Qubit-case is echter iets gecompliceerder voor Express met Dirac-notatie dan de kolom vector notatie en is volledig gelijk aan de vorige behandeling.

## <a name="density-operators"></a>Dichtheids operatoren

Een andere handige operator voor het gebruik van de Dirac-notatie is een *dichtheids operator*, soms ook wel een *status operator* genoemd.
Een dichtheids operator voor een Quantum status vector maakt het formulier $ \rho = \ket { \psi } \bra { \psi } $ .
Dit concept van het weer geven van de status als een matrix, in plaats van een vector, is vaak handig omdat het een handige manier is om de kans berekeningen te representeren, en kan er ook voor zorgen dat zowel statistische onzekerheid als de Quantum onzekerheid binnen dezelfde formele instelling worden beschreven.
Algemene Quantum status operatoren, in plaats van vectoren, zijn alomtegenwoordige in bepaalde gebieden van Quantum Computing, maar zijn niet nodig om de basis beginselen van het veld te begrijpen.
Voor de belanghebbende lezer raden we u aan een van de referentie boeken te lezen die zijn opgenomen in [voor meer informatie](xref:microsoft.quantum.more-information).

## <a name="no-locq-gate-sequences-equivalent-to-quantum-states"></a>Q# poort reeksen die gelijk zijn aan Quantum statussen

Een eind punt voor het verhogen van de Quantum-notatie en de Q# programmeer taal: bij het begin van dit document hebben we vermeld dat de Quantum status het fundamenteel object van informatie in quantum computing is.  Het kan dan als een verrassing zijn dat Q# er geen sprake is van een Quantum status.  In plaats daarvan worden alle statussen alleen beschreven door de bewerkingen die worden gebruikt om ze voor te bereiden.  Het vorige voor beeld is dit een uitstekende illustratie.  In plaats van een uniforme superpositie te geven voor elke Quantum-bits teken reeks in een REGI ster, kunnen we het resultaat als $ H ^ { \otimes n } \ket { 0 vertegenwoordigen } $ .  Deze exponentiële korte beschrijving van de status heeft niet alleen het voor deel dat we er in de klassieke reden voor kunnen hebben, maar ook een beknopt overzicht van de bewerkingen die nodig zijn om door de software stack te worden door gegeven om de algoritme te implementeren.  Daarom Q# is het ontworpen om poort reeksen te verzenden in plaats van Quantum Staten, maar op theoretisch niveau zijn de twee perspectieven gelijkwaardig.
