---
title: De Qubit in Quantum Computing
description: Meer informatie over qubits, de basis eenheid van informatie in Quantum Computing.
author: QuantumWriter
uid: microsoft.quantum.concepts.qubit
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 770b739d95f5c1512234f6f7d2ca4544f1d80e64
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907525"
---
# <a name="the-qubit"></a>De Qubit

Net als bits is het belangrijkste object van informatie in klassieke computing, [*qubits*](https://en.wikipedia.org/wiki/Qubit) (Quantum bits) het belangrijkste object van informatie in Quantum Computing.  We kijken naar het eenvoudigste voor beeld om deze correspondentie te begrijpen: één Qubit.

## <a name="representing-a-qubit"></a>Een Qubit vertegenwoordigt

Hoewel een bit, of binair cijfer, een waarde van $0 $ of $1 $ kan hebben, kan een Qubit een waarde hebben die een van deze twee of een Quantum-superpositie van $0 $ en $1 $ kan hebben.

De status van één qubit kan worden beschreven met behulp van een tweedimensionale kolom vector van de eenheids norm, dat wil zeggen dat de grootte van de items in het kwadraat moet worden opgeteld bij $1 $. Deze vector, de Quantum-status vector, bevat alle informatie die nodig is om het Quantum systeem van één Qubit te beschrijven, net als een enkele bit, met alle informatie die nodig is om de status van een binaire variabele te beschrijven.

Een tweedimensionale kolom vector van reële of complexe getallen met norm $1 $ vertegenwoordigt een mogelijke Quantum status die door een Qubit wordt gehouden. Dus $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ vertegenwoordigt een Qubit-status als $ \alpha $ en $ \beta $ complexe getallen zijn die voldoen aan $ | \alpha | ^ 2 + | \beta | ^ 2 = $1. Enkele voor beelden van geldige Quantum status vectoren die qubits bevatten

$ $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{-1}{\sqrt{2}} \end{bmatrix}, \Text{en} \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{i}{\sqrt{2}} \end{bmatrix}. $ $

De Quantum status vectors $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ en $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ een speciale rol nemen. Deze twee vectoren vormen een basis voor de vector ruimte die de status van de Qubit beschrijft. Dit betekent dat elke Quantum status vector kan worden geschreven als een som van deze basis vectoren. Met name de vector $ \begin{bmatrix} x \\\\ y \end{bmatrix} $ kan worden geschreven als $x \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} + y \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $. Hoewel elke draaiing van deze vectoren als een volledig geldige basis voor de Qubit fungeert, kiezen we de bevoegdheid om dit te doen door de *berekening*uit te voeren.

We nemen deze twee Quantum Staten in overeenstemming met de twee staten van een klassieke bit, namelijk $0 $ en $1 $. De standaard Conventie is om te kiezen

$ $0 \ equiv \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad 1 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}, $ $

Hoewel de tegenovergestelde keuze kan gelijkelijk worden uitgevoerd. Daarom is er een oneindig aantal mogelijke Quantum status vectoren met één Qubit, maar beide komen overeen met de statussen van klassieke bits; alle andere Quantum statussen doen dit niet.

## <a name="measuring-a-qubit"></a>Een Qubit meten

Nu we weten hoe u een Qubit kunt vertegenwoordigen, kunnen we een Intuition verkrijgen voor wat deze provincies vertegenwoordigen door het concept van [*meting*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)te bespreken. Een meting komt overeen met het informele idee van ' lookd ' op een Qubit, waarmee de Quantum status onmiddellijk wordt samengevouwen in een van de twee klassieke Staten $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $ of $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $. Wanneer een Qubit gegeven door de Quantum status vector $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ wordt gemeten, krijgen we het resultaat $0 $ met kans $ | \alpha | ^ 2 $ en de uitkomst $1 $ met kans $ | \beta | ^ 2 $. Op de uitkomst $0 $ is de nieuwe status van de Qubit $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $; op de uitkomst $1 $ is de status $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $. Houd er rekening mee dat deze waarschijnlijkheid tot $1 $ optelt vanwege de normalisatie voorwaarde $ | \alpha | ^ 2 + | \beta | ^ 2 = $1.

De eigenschappen van meting betekenen ook dat het algemene teken van de Quantum State-vector niet van belang is. Het negeren van een vector is gelijk aan $ \alpha \rightarrow-\alpha $ en $ \beta \rightarrow-\beta $. Omdat de waarschijnlijkheid van het meten van $0 $ en $1 $ afhankelijk is van de grootte van de voor waarden, is het invoegen van dergelijke tekens niet van invloed op de waarschijnlijkheid. Dergelijke fasen worden meestal [``*globale fasen*](https://en.wikipedia.org/wiki/Phase_factor) genoemd en kunnen in het algemeen van het formulier $e ^ {i \phi} $ en niet alleen $ \pm $1.

Een laatste belang rijke eigenschap van meting is dat het niet nood zakelijk is om alle Quantum status vectoren te beschadigen. Als we beginnen met een Qubit in de staat $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} $, die overeenkomt met de klassieke staat $0 $, geeft deze status altijd het resultaat $0 $ en wordt de Quantum status ongewijzigd gelaten. Als we in deze zin alleen klassieke bits hebben (qubits die $ \begin{bmatrix}1 \\\\ 0 \end{bmatrix} $ of $ \begin{bmatrix}0 \\\\ 1 \end{bmatrix} $), wordt het systeem door meting niet beschadigd. Dit betekent dat we klassieke gegevens kunnen repliceren en bewerken op een quantum computer, net als bij een klassieke computer. De mogelijkheid om gegevens in beide staten tegelijk op te slaan, is wat een grotere verfijning van Quantum Computing overschrijdt dan wat mogelijk op klassieke en andere Robs quantum computers van de mogelijkheid om Quantum gegevens te kopiëren, zie ook [de theorema zonder klonen](https://en.wikipedia.org/wiki/No-cloning_theorem).

## <a name="visualizing-qubits-and-transformations-using-the-bloch-sphere"></a>Qubits en trans formaties visualiseren met behulp van de Bloch-bol

Qubits kan ook in $3 $ D worden afgebeeld met behulp van de weer gave [*Bloch Sphere*](https://en.wikipedia.org/wiki/Bloch_sphere) .  De Bloch-bol biedt een manier om een Quantum status met één Qubit te beschrijven (dit is een tweedimensionale, complexe vector) als een driedimensionale vector.  Dit is belang rijk omdat het ons de mogelijkheid biedt om Qubit te visualiseren en daarom redenen te ontwikkelen die ingrijpend kunnen zijn in de statussen van meerdere Qubit (waarbij Sadly de Bloch Sphere-weer gave inzoomt).  De Bloch-bol kan als volgt worden gevisualiseerd:

<!--- ![](.\media\bloch.svg){ width=50% } --->
![Bloche Sphere](~/media/concepts_bloch.png)

De pijlen in dit diagram tonen de richting waarin de Quantum status vector wijst en elke trans formatie van de pijl kan worden beschouwd als een rotatie over een van de assen.
Het is een goed idee om met behulp van deze Intuition de algoritmen te ontwerpen en te beschrijven, terwijl u overweegt een Quantum berekening uit te geven als een reeks rotaties een krachtige Intuition is. Q # vermindert dit probleem door een taal te bieden voor het beschrijven van dergelijke draaiingen.

## <a name="single-qubit-operations"></a>Single-Qubit bewerkingen

Quantum computers verwerken gegevens door een universele set Quantum-Gates toe te passen waarmee de draai hoek van de Quantum status vector kan worden geëmuleerd.
Dit voor stel van universality is Akin naar het principe van de universele kracht voor traditionele (klassieke) computing waarbij een poortset als universeel wordt beschouwd als elke trans formatie van de invoer bits kan worden uitgevoerd met behulp van een circuit met een eindige lengte.
In Quantum Computing zijn de geldige trans formaties die we mogen uitvoeren op een Qubit, unitary trans formaties en meting.
De *adjoint-bewerking* of de complex geconjugeerde getransponeerde is van cruciaal belang voor Quantum Computing, omdat het nodig is om Quantum trans formaties te omkeren.
Q # weerspiegelt dit door methoden te bieden voor het automatisch compileren van Gate-reeksen aan hun adjoint, waarmee de programmeur in veel gevallen de code van de hand kan adjoints. Hieronder ziet u een voor beeld van dit:

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Adj { // Auto-generate the adjoint of the operation
    H(qubit);
}
```

Hoewel dit een gelastig voor beeld is (als de <xref:microsoft.quantum.intrinsic.h>-bewerking zelf adjoint is), ziet u hoe dit inwaardevol wordt voor complexere Qubit bewerkingen.
Zie [bewerkingen en functies](xref:microsoft.quantum.techniques.opsandfunctions)voor meer informatie.

Er zijn slechts vier functies die één bit aan één bit op een klassieke computer toewijzen. Daarentegen is er een oneindig aantal unitary-trans formaties op één Qubit op een quantum computer. Daarom kan een beperkte set primitieve Quantum bewerkingen, die [*Gates*](https://en.wikipedia.org/wiki/Quantum_logic_gate)worden genoemd, de oneindige set unitary-trans formaties die zijn toegestaan in de Quantum Computing, exact repliceren. Dit betekent dat, in tegens telling tot klassieke computing, het onmogelijk is dat een quantum computer elk mogelijk Quantum programma implementeert, precies met een eindige hoeveelheid poorten. Daarom kunnen quantum computers niet universeel zijn in dezelfde zin van klassieke computers. Als we er rekening mee houden dat een reeks poorten *universeel* is voor Quantum Computing, hebben we eigenlijk iets zwakkerer dan voor klassiek computing.
Voor universality is het vereist dat een quantum computer alleen elke unitary-matrix binnen een eindige fout *benadert* met behulp van een poort reeks met een eind lengte.
Met andere woorden, een reeks poorten is een universele Gate-set als een unitary-trans formatie ongeveer als een product van poorten van deze set kan worden geschreven. Het is vereist dat voor elke vereiste fout gebonden poorten bestaan $G _{1}, G_{2}, \ldots, G_N $ van de poort set zodanig dat

$ $ G_N G_ {N-1} \cdots G_2 G_1 \approx U. $ $

Houd er rekening mee dat de Conventie voor het vermenigvuldigen van de matrix van rechts naar links de eerste poort bewerking in deze volg orde moet worden $G _N $, in feite de laatste is toegepast op de Quantum status vector. Formeel, we zeggen dat een dergelijke Gate set universeel is als er voor elke fout tolerantie $ \epsilon > 0 $ bestaat $G _1, \ldots, G_N $ zodanig dat de afstand tussen $G _N \ldots G_1 $ en $U $ Maxi maal $ \epsilon $ is. In het ideale geval de waarde van $N $ die nodig is om deze afstand van $ \epsilon $ te bereiken, moet poly-logarithmically met $1/\ Epsilon $ worden geschaald.

Hoe ziet een universele Gate-set eruit als in de praktijk?  De meest eenvoudige, universele Gate-set voor single-Qubit-poorten bestaat uit slechts twee poorten: de Hadamard-poort $H $ en de zogenaamde $T $-Gate (ook wel de $ \ Pi/8 $ Gate):

$ $ H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 &-1 \end{bmatrix}, \qquad T = \begin{bmatrix} 1 & 0 \\\\ 0 & e ^ {i \ Pi/4} \end{bmatrix}.
$$

Om praktische redenen met betrekking tot de Quantum-fout correctie kan het echter handiger zijn om een grotere poortset te gebruiken. Dit is namelijk een reeks die kan worden gegenereerd met $H $ en $T $.
We kunnen de Quantum-poorten in twee categorieën classificeren: Clifford Gates en de $T $-Gate.
Deze onderverdeling is nuttig omdat in veel Quantum-fout correctie schema's de zogenaamde Clifford-poorten gemakkelijk te implementeren zijn, dat wil zeggen dat ze zeer weinig bronnen nodig hebben voor de bewerkingen en qubits om fout tolerant te implementeren, terwijl niet-Clifford-poorten tamelijk kostbaar wanneer fout tolerantie is vereist. De standaardset single-Qubit Clifford-Gates, [standaard opgenomen in Q #](xref:microsoft.quantum.libraries.standard.prelude), bevatten

$ $ H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 &-1 \end{bmatrix}, \qquad S = \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix} = T ^ 2, \qquad X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} = HT ^ 4U, $ $

$ $ Y = \begin{bmatrix} 0 &-i \\\\ i & 0 \end{bmatrix} = T ^ 2HT ^ 4 HT ^ 6, \qquad Z = \begin{bmatrix}1 & 0\\\\ 0 &-1 \end{bmatrix} = T ^ 4.
$$

Hier worden de bewerkingen $X $, $Y $ en $Z $ vaak gebruikt en worden [*Pauli Opera tors*](https://en.wikipedia.org/wiki/Pauli_matrices) genoemd na de maker Wolfgang Pauli.
Samen met de niet-Clifford-poort (de $T $-Gate) kunnen deze bewerkingen worden samengesteld om een unitary-trans formatie op één Qubit te benaderen.

Zie [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions)voor meer informatie over deze bewerkingen, hun Bloch Sphere-representaties en Q #-implementaties.

Als voor beeld van hoe unitary-trans formaties kunnen worden gebouwd uit deze primitieven, komen de drie trans formaties in de bovenstaande Bloch-gebieden overeen met de poort reeks $ \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \mapsto HZH \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $.

Hoewel het vorige de meest populaire primitieve poorten vormt voor het beschrijven van bewerkingen op het logische niveau van de stack (denk aan het logische niveau als het niveau van het Quantum algoritme), is het vaak handig om minder elementaire bewerkingen op het algoritme te overwegen niveau, bijvoorbeeld bewerkingen dichter bij een beschrijvings niveau van de functie. Gelukkig heeft Q # ook methoden die beschikbaar zijn voor het implementeren van unitaries op een hoger niveau, waardoor het mogelijk is dat algoritmen op hoog niveau worden geïmplementeerd zonder dat alles expliciet wordt opsamengesteld naar Clifford en $T $-Gates.

De eenvoudigste manier om een dergelijke primitieve te zijn, is de enkele Qubit. Drie rotaties met één Qubit worden meestal beschouwd: $R _x $, $R _y $ en $R _z $. Als u de actie van de draai $R _x (\theta) $ wilt visualiseren, kunt u bijvoorbeeld een voor beeld van de rechter muisknop geven aan de richting van de $x $-as van de Bloch-bol en de vector met uw hand in een hoek van $ \ theta/2 $ radialen draaien. Deze onduidelijke factor van $2 $ ontstaat uit het feit dat de rechthoekige vectoren $180 ^ \circ $ van elkaar worden weer gegeven op de Bloch-bol, maar eigenlijk $90 ^ \circ $ graden onafhankelijk van elkaar liggen. De bijbehorende unitary-matrices zijn:

\begin{align *} & R_z (\theta) = e ^ {-I\theta z/2} = \begin{bmatrix} e ^ {-i \ theta/2} & 0\\\\ 0 & e ^ {i \ theta/2} \end{bmatrix}, \\\\ & R_x (\theta) = e ^ {-I\theta x/2} = HR_z (\theta) H = \begin{bmatrix} \cos (\ theta/2) &-i\sin (\ theta/2)\\\\-i\sin (\ theta/2) & \cos (\ theta/2) \end{bmatrix}, \\\\ & R_y (\theta) = e ^ {-I\theta y/2} = SHR_z (\theta) HS ^ \dagger = \begin{bmatrix} \cos (\ theta/2) &-\sin (\ theta/2)\\\\ \sin (\ theta/2) & \cos (\ theta/2) \end{bmatrix}. \end{align*}

Net zoals drie draaiingen kunnen samen worden gecombineerd om een wille keurige draaiing uit te voeren in drie dimensies, kan deze worden gezien vanuit de Bloch-weer gave van een wille keurige unitary-matrix, die ook kan worden geschreven als een reeks van drie rotaties. Voor elke unitary matrix $U $ bestaat er $ \alpha, \beta, \gamma, \delta $ zodanig dat $U = e ^ {i\alpha} R_x (\beta) R_z (\gamma) R_x (\delta) $. $R _z (\theta) $ en $H $ vormen dus ook een universele Gate-set, hoewel het geen discrete set is, omdat $ \theta $ een wille keurige waarde kan hebben. Om deze reden en als gevolg van toepassingen in Quantum simulatie zijn deze voortdurende poorten cruciaal voor de Quantum berekening, met name op het niveau van de Quantum algoritme. Om fout tolerante hardware-implementatie te kunnen uitvoeren, worden deze uiteindelijk gecompileerd in afzonderlijke poort reeksen die nauw keurig deze rotaties benaderen.
