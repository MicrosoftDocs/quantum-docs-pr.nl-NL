---
Titel: de Qubit in Quantum Computing Description: meer informatie over qubits, de basis eenheid van informatie in Quantum Computing.
Auteur: QuantumWriter UID: micro soft. Quantum. concepten. Qubit MS. Author: nawiebe@microsoft.com MS. date: 12/11/2017 MS. topic: artikel no-loc:
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
# <a name="the-qubit"></a>De Qubit

Net als bits is het belangrijkste object van informatie in klassieke computing, [*qubits*](https://en.wikipedia.org/wiki/Qubit) (Quantum bits) het belangrijkste object van informatie in Quantum Computing.  We kijken naar het eenvoudigste voor beeld om deze correspondentie te begrijpen: één Qubit.

## <a name="representing-a-qubit"></a>Een Qubit vertegenwoordigt

Hoewel een bit, of binair cijfer, een waarde $ $ van 0 of 1 kan hebben $ $ , kan een Qubit een waarde hebben die een van deze of een Quantum-positie van $ 0 $ en 1 kan hebben $ $ .

De status van één qubit kan worden beschreven met behulp van een tweedimensionale kolom vector van de eenheids norm, dat wil zeggen dat de grootte van de items in het kwadraat moet worden opgeteld bij $ 1 $ . Deze vector, de Quantum-status vector, bevat alle informatie die nodig is om het Quantum systeem van één Qubit te beschrijven, net als een enkele bit, met alle informatie die nodig is om de status van een binaire variabele te beschrijven.

Een tweedimensionale kolom vector van reële of complexe getallen met norm $ 1 $ vertegenwoordigt een mogelijke Quantum status die door een Qubit wordt gehouden. $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ Vertegenwoordigt daarom een Qubit-status als $ \alpha $ en $ \beta $ complexe getallen zijn die aan $ | \alpha | ^ 2 + | \beta | ^ 2 = 1 voldoen $ .   Enkele voor beelden van geldige Quantum status vectoren die qubits bevatten

$$\begin{bmatrix}1 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} , \begin{bmatrix} \frac { 1 } { \sqrt { 2, } } \\\\ \frac { } { \sqrt { 2, 1 2, 1 } } \end{bmatrix} \begin{bmatrix} \frac { } { \sqrt { } } \\\\ \frac { } { \sqrt { } } \end{bmatrix} \text { en } \begin{bmatrix} \frac { 1 2, } { \sqrt { } } \\\\ \frac { } { \sqrt { 2 } } \end{bmatrix} .      $$

De Quantum-status vectoren $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ en $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ nemen een speciale rol. Deze twee vectoren vormen een basis voor de vector ruimte die de status van de Qubit beschrijft. Dit betekent dat elke Quantum status vector kan worden geschreven als een som van deze basis vectoren. Met name de vector $ \begin{bmatrix} x \\\\ y \end{bmatrix} $ kan worden geschreven als $ x \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} + y \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ . Hoewel elke draaiing van deze vectoren als een volledig geldige basis voor de Qubit fungeert, kiezen we de bevoegdheid om dit te doen door de *berekening*uit te voeren.

We nemen deze twee Quantum Staten in overeenstemming met de twee staten van een klassieke bit, namelijk $ 0 $ en $ 1 $ . De standaard Conventie is om te kiezen

$$0 \equiv \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad 1 \equiv \begin{bmatrix} 0 \\\\ \end{bmatrix} ,$$

Hoewel de tegenovergestelde keuze kan gelijkelijk worden uitgevoerd. Daarom is er een oneindig aantal mogelijke Quantum status vectoren met één Qubit, maar beide komen overeen met de statussen van klassieke bits; alle andere Quantum statussen doen dit niet.

## <a name="measuring-a-qubit"></a>Een Qubit meten

Nu we weten hoe u een Qubit kunt vertegenwoordigen, kunnen we een Intuition verkrijgen voor wat deze provincies vertegenwoordigen door het concept van [*meting*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)te bespreken. Een meting komt overeen met het informele idee van ' lookd ' op een Qubit, waarmee de Quantum status onmiddellijk wordt samengevouwen in een van de twee klassieke statussen $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ of $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ . Wanneer een Qubit gegeven door de Quantum status Vector $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ wordt gemeten, krijgen we het resultaat $ 0 $ met waarschijnlijkheid $ | \alpha | ^ 2 $ en de uitkomst $ 1 $ met kans $ | \beta | ^ 2 $ .   Bij een resultaat $ 0 $ is de nieuwe status van de Qubit $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ ; bij $ een resultaat 1 $ is de status $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ . Houd er rekening mee dat deze waarschijnlijkheid tot 1 som is $ $ vanwege de normalisatie voorwaarde $ | \alpha | ^ 2 + | \beta | ^ 2 = 1 $ .

De eigenschappen van meting betekenen ook dat het algemene teken van de Quantum State-vector niet van belang is. Het negeren van een vector is gelijk aan de $ \alpha \right pijl- \alpha $ en $ \beta \right pijl- \beta $ . Omdat de kans op het meten van $ 0 $ en $ 1 $ afhankelijk is van de grootte van de voor waarden, is het invoegen van dergelijke tekens niet van invloed op de waarschijnlijkheid. Dergelijke fasen worden vaak [ `` *globale fasen*](https://en.wikipedia.org/wiki/Phase_factor) genoemd en kunnen in het algemeen van het formulier $ e ^ i zijn { , \phi } $ in plaats van alleen $ \pm 1 $ .

Een laatste belang rijke eigenschap van meting is dat het niet nood zakelijk is om alle Quantum status vectoren te beschadigen. Als we beginnen met een Qubit in de staat $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ , die overeenkomt met de klassieke staat $ 0 $ , geeft deze status altijd het resultaat $ 0 en wordt $ de Quantum status ongewijzigd gelaten. Als we in deze zin alleen klassieke bits hebben (qubits die $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ of 0 1 zijn), wordt $ \begin{bmatrix} \\\\ \end{bmatrix} $ het systeem niet door de meting beschadigd. Dit betekent dat we klassieke gegevens kunnen repliceren en bewerken op een quantum computer, net als bij een klassieke computer. De mogelijkheid om gegevens in beide staten tegelijk op te slaan, is wat een grotere verfijning van Quantum Computing overschrijdt dan wat mogelijk op klassieke en andere Robs quantum computers van de mogelijkheid om Quantum gegevens te kopiëren, zie ook [de theorema zonder klonen](https://en.wikipedia.org/wiki/No-cloning_theorem).

## <a name="visualizing-qubits-and-transformations-using-the-bloch-sphere"></a>Qubits en trans formaties visualiseren met behulp van de Bloch-bol

Qubits kan ook in 3 D worden gepictureeerd $ $ met behulp van de weer gave [*Bloch Sphere*](https://en.wikipedia.org/wiki/Bloch_sphere) .  De Bloch-bol biedt een manier om een Quantum status met één Qubit te beschrijven (dit is een tweedimensionale, complexe vector) als een driedimensionale vector.  Dit is belang rijk omdat het ons de mogelijkheid biedt om Qubit te visualiseren en daarom redenen te ontwikkelen die ingrijpend kunnen zijn in de statussen van meerdere Qubit (waarbij Sadly de Bloch Sphere-weer gave inzoomt).  De Bloch-bol kan als volgt worden gevisualiseerd:

<!--- ![](.\media\bloch.svg) { breedte = 50%} --->
![Bloch-bol](~/media/concepts_bloch.png)

De pijlen in dit diagram tonen de richting waarin de Quantum status vector wijst en elke trans formatie van de pijl kan worden beschouwd als een rotatie over een van de assen.
Het is een goed idee om met behulp van deze Intuition de algoritmen te ontwerpen en te beschrijven, terwijl u overweegt een Quantum berekening uit te geven als een reeks rotaties een krachtige Intuition is. Q#Hiermee verkleint u het probleem door een taal te bieden voor het beschrijven van dergelijke draaiingen.

## <a name="single-qubit-operations"></a>Single-Qubit bewerkingen

Quantum computers verwerken gegevens door een universele set Quantum-Gates toe te passen waarmee de draai hoek van de Quantum status vector kan worden geëmuleerd.
Dit voor stel van universality is Akin naar het principe van de universele kracht voor traditionele (klassieke) computing waarbij een poortset als universeel wordt beschouwd als elke trans formatie van de invoer bits kan worden uitgevoerd met behulp van een circuit met een eindige lengte.
In Quantum Computing zijn de geldige trans formaties die we mogen uitvoeren op een Qubit, unitary trans formaties en meting.
De *adjoint-bewerking* of de complex geconjugeerde getransponeerde is van cruciaal belang voor Quantum Computing, omdat het nodig is om Quantum trans formaties te omkeren.
Q#Dit weerspiegelt door methoden te bieden voor het automatisch compileren van poort reeksen aan hun adjoint, waardoor de programmeur in veel gevallen de code van de hand heeft adjoints. Hieronder ziet u een voor beeld van dit:

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Adj { // Auto-generate the adjoint of the operation
    H(qubit);
}
```

Hoewel dit een gelastig voor beeld is (zoals de < bewerking XREF: micro soft. Quantum. intrinsiek. h > is self-adjoint), kunt u zien hoe dit inwaardevol wordt voor complexere Qubit bewerkingen.
Zie [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie.

Er zijn slechts vier functies die één bit aan één bit op een klassieke computer toewijzen. Daarentegen is er een oneindig aantal unitary-trans formaties op één Qubit op een quantum computer. Daarom kan een beperkte set primitieve Quantum bewerkingen, die [*Gates*](https://en.wikipedia.org/wiki/Quantum_logic_gate)worden genoemd, de oneindige set unitary-trans formaties die zijn toegestaan in de Quantum Computing, exact repliceren. Dit betekent dat, in tegens telling tot klassieke computing, het onmogelijk is dat een quantum computer elk mogelijk Quantum programma implementeert, precies met een eindige hoeveelheid poorten. Daarom kunnen quantum computers niet universeel zijn in dezelfde zin van klassieke computers. Als we er rekening mee houden dat een reeks poorten *universeel* is voor Quantum Computing, hebben we eigenlijk iets zwakkerer dan voor klassiek computing.
Voor universality is het vereist dat een quantum computer alleen elke unitary-matrix binnen een eindige fout *benadert* met behulp van een poort reeks met een eind lengte.
Met andere woorden, een reeks poorten is een universele Gate-set als een unitary-trans formatie ongeveer als een product van poorten van deze set kan worden geschreven. Als er sprake is van een eventueel vereiste fout, bestaan er Gates $ G_ { 1 } , G_ { 2 } , \ldots, G_N $ van de poortset, zodanig dat

$$
G_N G_ { N-1 } \cdots G_2 G_1 \approx U.$$

Houd er rekening mee dat de Conventie voor het vermenigvuldigen van de matrix van rechts naar links de eerste poort bewerking in deze volg orde, $ G_N $ , in feite de laatste is die is toegepast op de Quantum status vector. Formeel, we zeggen dat een dergelijke Gate set universeel is als voor elke fout tolerantie $ \epsilon > 0 $ bestaat $ G_1, \ldots G_N $ zodanig is dat de afstand tussen $ G_N \ldots G_1 $ en $ U $ Maxi maal $ \epsilon $ . In het ideale geval is de waarde van $ N $ vereist om deze afstand van \epsilon te bereiken $ $ , moet poly-logarithmically met $ 1/\ Epsilon worden geschaald $ .

Hoe ziet een universele Gate-set eruit als in de praktijk?  De meest eenvoudige, universele Gate-set voor single-Qubit-poorten bestaat uit slechts twee poorten: de Hadamard $ -Gate H $ en de zogenaamde $ T $ -Gate (ook wel de ' $ \ Pi/8-poort ' genoemd $ ):

$$
H = \frac { 1 2 1 1 } { \sqrt { } } \begin{bmatrix} & , 1 \\\\ & \end{bmatrix} , \qquad T = \begin{bmatrix} 1 0 0 & \\\\ & e ^ { i \ Pi/4 } \end{bmatrix} .
$$

Om praktische redenen met betrekking tot de Quantum-fout correctie kan het echter handiger zijn om een grotere poortset te gebruiken. Dit is namelijk een reeks die kan worden gegenereerd met $ H $ en $ T $ . We kunnen de Quantum-poorten in twee categorieën classificeren: Clifford Gates en de $ T $ -poort.
Deze onderverdeling is nuttig omdat in veel Quantum fout correctie-schema's de zogenaamde Clifford-poorten gemakkelijk te implementeren zijn, dat wil zeggen dat ze zeer weinig resources nodig hebben in de vorm van bewerkingen en qubits om fout tolerant te implementeren, terwijl niet-Clifford-poorten behoorlijk kostbaar zijn wanneer fout tolerantie wordt vereist. De standaardset met single-Qubit Clifford-Gates, [die standaard zijn Q# opgenomen in ](xref:microsoft.quantum.libraries.standard.prelude), zijn onder andere

$$
H = \frac { 1 2 1 1 } { \sqrt { } } \begin{bmatrix} & \\\\ & -1 \end{bmatrix} , \qquad S = \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix} = T ^ 2, \qquad X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} = HT ^ 4U,$$

$$
Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix} = T ^ 2HT ^ 4 HT ^ 6, \qquad Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} = T ^ 4.
$$

Hier worden de bewerkingen $ X $ , $ Y $ en $ Z $ meestal gebruikt en worden benoemde Pauli- [*Opera tors*](https://en.wikipedia.org/wiki/Pauli_matrices) genoemd na de maker Wolfgang Pauli.
Samen met de niet-Clifford-poort (de $ T $ -poort) kunnen deze bewerkingen worden samengesteld om een unitary-trans formatie op één Qubit te benaderen.

Zie voor meer informatie over deze bewerkingen, de representaties en implementaties van de Bloch Q# -bol, [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions).

Als voor beeld van hoe unitary-trans formaties kunnen worden samengesteld uit deze primitieven, komen de drie trans formaties in de bovenstaande Bloch-gebieden overeen met de poort reeks $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \mapsto HZH \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ .

Hoewel het vorige de meest populaire primitieve poorten vormt voor het beschrijven van bewerkingen op het logische niveau van de stack (denk aan het logische niveau als het niveau van het Quantum algoritme), is het vaak handig om minder basis bewerkingen op het niveau van de algoritme te overwegen, bijvoorbeeld bewerkingen dichter bij een niveau van functie beschrijving. Gelukkig Q# beschikt ook over methoden die beschikbaar zijn voor het implementeren van unitaries op een hoger niveau, waardoor het mogelijk is dat algoritmen op hoog niveau worden geïmplementeerd zonder dat alles expliciet op Clifford en $ T-Gates hoeft te worden samengesteld $ .

De eenvoudigste manier om een dergelijke primitieve te zijn, is de enkele Qubit. Er worden meestal drie draaiingen met één Qubit beschouwd: $ R_x $ , $ R_y $ en $ R_z $ . Als u de actie van de draai $ R_x (\theta) wilt visualiseren, kunt u bijvoorbeeld het beste de $ richting van de $ x $ -as van de Bloch-bol naar rechts wijzen en de vector met uw hand in een hoek van $ \ theta/2 $ radialen draaien. Deze verwarrende factor $ 2 $ ontstaat uit het feit dat orthogonale vectoren $ 180 ^ \circ zijn $ bij het uitzetten van de Bloch-bol, maar in feite $ 90 ^ \circ $ graden van geometrisch zijn. De bijbehorende unitary-matrices zijn:

\begin{align* } 
 & R_z (\theta) = e ^ { -i\theta z/2 } = \begin{bmatrix} e ^ { -i \ theta/2 } & 0 \\\\ 0 & e ^ { i \ theta/2 } \end{bmatrix} , \\\\ 
 & R_x (\theta) = e ^ { -i\theta x/2 } = HR_z (\theta) H = \begin{bmatrix} \cos (\ theta/2) & -i\sin (\ theta/2) \\\\ -i\sin (\ theta/2) & \cos (\ theta/2) \end{bmatrix} , \\\\ 
 & R_y (\theta) = e ^ { -i\theta y/2 } = SHR_z (\theta) HS ^ \dagger = \begin{bmatrix} \cos (\ theta/2) & -\sin (\ theta/2) \\\\ \sin (\ theta/2) & \cos (\ theta/2) \end{bmatrix} . \end { uitlijnen*}

Net zoals drie draaiingen kunnen samen worden gecombineerd om een wille keurige draaiing uit te voeren in drie dimensies, kan deze worden gezien vanuit de Bloch-weer gave van een wille keurige unitary-matrix, die ook kan worden geschreven als een reeks van drie rotaties. In het bijzonder, voor elke unitary matrix $ die u hebt,,, $ , zodat $ \alpha \beta \gamma \delta $ $ u = e ^ { i \alpha } R_x ( \beta ) R_z () \gamma R_x ( \delta ) $ . $R_z (\theta) $ en $ H vormen daarom $ ook een universele Gate-set, hoewel het geen afzonderlijke set is, omdat $ \theta $ elke waarde kan nemen. Om deze reden en als gevolg van toepassingen in Quantum simulatie zijn deze voortdurende poorten cruciaal voor de Quantum berekening, met name op het niveau van de Quantum algoritme. Om fout tolerante hardware-implementatie te kunnen uitvoeren, worden deze uiteindelijk gecompileerd in afzonderlijke poort reeksen die nauw keurig deze rotaties benaderen.
