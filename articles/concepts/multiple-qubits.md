---
title: Meerdere qubits | Microsoft Docs
description: Meerdere qubits
author: QuantumWriter
uid: microsoft.quantum.concepts.multiple-qubits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3e0404cfd67f693ff6b7a8297566e59208fc7ec0
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183774"
---
# <a name="multiple-qubits"></a>Meerdere qubits

Hoewel single-Qubit Gates beschikken over een aantal intuïtieve functies, zoals de mogelijkheid om in meer dan één toestand op een bepaald moment te worden uitgevoerd, als al het aantal op een quantum computer een ' single-Qubit-Gates had, zouden we een apparaat met reken kracht hebben dat zou worden dwarfed door zelfs een reken machine mag alleen een klassieke supercomputer hebben.
De werkelijke kracht van Quantum Computing wordt alleen duidelijk naarmate we het aantal qubits verg Roten.
Deze stroom treedt deels op omdat de dimensie van de vector ruimte van Quantum status vectoren exponentieel toeneemt met het aantal qubits.
Dit betekent dat hoewel een enkelvoudige Qubit redelijk kan worden gemodelleerd, het simuleren van een quantum van 50-Qubit weliswaar de limieten van bestaande supercomputeren pusht.
Het verg Roten van de omvang van de berekening door slechts één extra Qubit *verdubbelt* het geheugen dat nodig is voor het opslaan van de status en *verdubbelt* ongeveer de reken tijd.
Dit snelle, verdubbeling van de reken kracht is waarom een quantum computer met een relatief klein aantal qubits de krach tigste super computers van vandaag, morgen en verder niet kan overschrijden voor bepaalde reken taken.

Waarom hebben we exponentiële groei voor Quantum-status vectoren?  Het doel van deze sectie is om de regels te bekijken die worden gebruikt voor het bouwen van Qubit-statussen uit Qubit-Staten en de poort bewerkingen te bespreken die in onze Gate set moeten worden opgenomen om een Universal veel-Qubit quantum-computer te vormen.
Deze hulpprogram ma's zijn absoluut nood zakelijk om inzicht te krijgen in de poort sets die vaak worden gebruikt in Q #-code en om Intuition te verkrijgen over waarom Quantum effecten, zoals entanglement of interferentie, meer krachtiger zijn dan klassiek computing.

## <a name="representing-two-qubits"></a>Die twee qubits vertegenwoordigen
Het belangrijkste verschil tussen de een-en twee Qubit Staten is dat twee Qubit-Staten vier driedimensionaal zijn in plaats van twee dimensies.
Dit komt doordat de reken kundige basis voor twee Qubit Staten wordt gevormd door de tensor-producten van een Qubit-status.  We hebben bijvoorbeeld \begin{align} 00 \equiv \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix}1 \\\\ 0 \end{bmatrix} & = \begin{bmatrix}1 \\\\ 0\\\\ 0\\@no__ t_9_ 0 \end{bmatrix}, \qquad 01 \equiv \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix}0 \\\\ 1 \end{bmatrix} = \begin{bmatrix}0 \\\\ 1\\\\ 0\\\\ 0 \end{bmatrix},\\\\ 10 \equiv \begin{bmatrix}0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix}1 \\\\ 0 \end{bmatrix} & = \begin{bmatrix}0 \\\\ 0\\\\ 1\\\\ 0 \end{bmatrix}, \qquad 11 \equiv \begin{bmatrix}0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix}0 \\\\ 1 \end{bmatrix} = \begin{bmatrix}0 \\\\ 0\\\\ 0 @no__ t_40_ \\ 1 \end{bmatrix}.
\end{align}

Het is eenvoudig om te zien dat de Quantum status van $n $ qubits wordt vertegenwoordigd door een eenheids vector van dimensie $2 ^ n $ met behulp van deze constructie.  De vector

$ $ \begin{bmatrix} \alpha_{00} \\\\ \alpha_{01} \\\\ \alpha_{10} \\\\ \alpha_{11} \end{bmatrix} $ $

vertegenwoordigt een Quantum status op twee qubits als $ | \alpha_{00}| ^ 2 + | \alpha_{01}| ^ 2 + | \alpha_{10}| ^ 2 + | \alpha_{11}| ^ 2 = 1 $. Net als bij één qubits bevat de Quantum status vector van meerdere qubits alle informatie die nodig is om het gedrag van het systeem te beschrijven.

Als we twee afzonderlijke qubits hebben gekregen, is een in de status $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ en een tweede Qubit in de staat $ \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $, de bijbehorende twee-Qubit status

$ $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} \otimes \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} = \begin{bmatrix} \alpha \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} \\\\ Bèta \begin{bmatrix}\gamma \\\\ \delta \end{bmatrix} \end{bmatrix} = \begin{bmatrix} \alpha\gamma \\\\ \alpha\delta \\\\ \beta\gamma \\\\ \beta\delta \end{bmatrix}, $ $

waarbij de bewerking $ \otimes $ het tensor product (of het Kronecker product) van vectoren wordt genoemd. Houd er rekening mee dat we het tensor-product van twee statussen met één Qubit in staat stellen om een status van twee Qubit te vormen, maar niet alle twee Qubit-Quantum waarden kunnen worden geschreven als het tensor product van twee single-Qubit Staten.
Er zijn bijvoorbeeld geen statussen $ \psi = \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ en $ \phi = \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $, waardoor het tensor-product de status is 

$ $ \psi\otimes \phi = \begin{bmatrix} 1/\ SQRT{2} \\\\ 0 \\\\ 0 \\\\ 1/\ SQRT{2} \end{bmatrix}. $ $ 

Een dergelijke status van twee Qubit, die niet kan worden geschreven als het tensor-product van single-Qubit statussen, wordt ' Entangled State ' genoemd. de twee qubits zijn gezegd als [*Entangled*](https://en.wikipedia.org/wiki/Quantum_entanglement).  Zonder enige spraak, omdat de Quantum status niet kan worden beschouwd als een tensor product van één Qubit-status, wordt de informatie die de status heeft, niet naar een van de qubits afzonderlijk beperkt.  In plaats daarvan wordt de informatie niet lokaal opgeslagen in de correlaties tussen de twee staten.  Deze niet-localiteit van informatie is een van de belangrijkste onderscheidings functies van Quantum Computing ten opzichte van klassiek computing en is essentieel voor een aantal Quantum protocollen, waaronder [Quantum-teleportie](https://github.com/Microsoft/Quantum/tree/master/Samples/src/Teleportation) en [Quantum fout correctie](xref:microsoft.quantum.libraries.error-correction).

## <a name="measuring-two-qubit-states"></a>Meting van twee Qubit Staten ##
Het meten van twee Qubit Staten lijkt veel op de metingen met één Qubit. De status meten

$ $ \begin{bmatrix} \alpha_{00} \\\\ \alpha_{01} \\\\ \alpha_{10} \\\\ \alpha_{11} \end{bmatrix} $ $

levert $0 $ met kans $ | \alpha_{00}| ^ $2, $1 $ met kans $ | \alpha_{01}| ^ $2, $10 $ met kans $ | \alpha_{10}| ^ $2 en $11 $ met kans $ | \alpha_{11}| ^ $2. De variabelen $ \alpha_{00}, \alpha_{01}, \alpha_{10}, $ en $ \alpha_{11}$ zijn opzettelijk benoemd om deze verbinding duidelijk te maken. Als de uitkomst na de meting $0 $ is, is de Quantum status van het systeem met twee Qubit samengevouwen en nu

$ $0 \equiv \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix}.
$$

Het is ook mogelijk slechts één Qubit van een Quantum-status van twee Qubit te meten. In gevallen waarbij u slechts één van de qubits meet, is de impact van de meting subtiel verschillend, omdat de gehele status niet wordt samengevouwen in een reken kundige status, en niet wordt samengevouwen tot slechts één subsysteem.  Met andere woorden, in dergelijke gevallen waarbij slechts één Qubit wordt gewerkt, wordt slechts een van de subsystemen, maar niet alle, samengevouwen.  

Om dit te zien, moet u de eerste Qubit van de volgende status meten, die wordt gevormd door het Toep assen van de Hadamard Transform $H $ op twee qubits in eerste instantie ingesteld op de status "0": $ $ H ^ {\otimes 2} \left (\begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \begin{ bmatrix} 1 \\\\ 0 \end{bmatrix} \right) = \frac{1}{2}\begin{bmatrix}1 & 1 & 1 & 1 \\\\ 1 &-1 & 1 &-1 \\\\ 1 & 1 &-1 &-1 @no__ t_10_ \\ 1 &-1 &-1 & 1 \end{bmatrix}\begin{bmatrix}1\\\\ 0\\\\ 0\\\\ 0 \ end {bmatrix} = \frac{1}{2}\begin{bmatrix}1\\\\ 1\\\\ 1\\\\ 1 \ end {bmatrix} \mapsto \begin{cases}\Text{outcome} = 0 & \frac{1}{\sqrt{2}} \begin{bmatrix}1\\\\ 1\\\\ 0\\\\ 0 \end{bmatrix}\\\\ \Text{outcome} = 1 & \frac{1}{\sqrt{2}} \begin{bmatrix}0\\\\ 0\\\\ 1\\\\ 1 \end{bmatrix}\\\\ \end{ cases}.
$ $ Beide resultaten hebben een waarschijnlijkheid van 50%.  Het resultaat van 50% waarschijnlijk voor beide kunnen worden afgeleid van het feit dat de initiële Quantum State-vector is invariant onder swaping $0 $ met $1 $ op de eerste Qubit.

De wiskundige regel voor het meten van de eerste of tweede Qubit is eenvoudig.  Als we $e _k $ de $k ^ {\rm do} $ reken kundige basis vector hebben en $S $ de set van alle $e _k $, zodat de betreffende Qubit de waarde $1 $ voor die waarde van $k $ heeft.  Als we bijvoorbeeld de eerste Qubit willen meten, zou $S $ bestaan uit $e _2 \ equiv $10 en $e _3 \ equiv $11.  En als we geïnteresseerd zijn in het tweede Qubit $S $ bestaat uit $e _1 \ equiv $1 en $e _3 \equiv $11.  De waarschijnlijkheid om de gekozen Qubit te meten als $1 $ is voor status vector $ \psi $

$ $ P (\Text{outcome} = 1) = \sum_{e_k \Text{in de set} S} \psi ^ \dagger e_k e_k ^ \dagger \psi.
$$

Aangezien elke qubit-meting alleen $0 $ of $1 $ kan leveren, is de kans op het meten van $0 $, simpelweg $1-P (\Text{outcome} = 1) $.  Daarom geven we alleen expliciet een formule voor de waarschijnlijkheid van het meten van $1 $.

De actie die een dergelijke meting op de status heeft, kan wiskundig worden uitgedrukt als

$ $ \psi \mapsto \frac{\sum_{e_k \Text{in de set} S} e_k e_k ^ \dagger \psi}{\sqrt{P (\Text{outcome} = 1)}}.
$$

De voorzichtigste lezer kan zich zorgen maken over wat er gebeurt wanneer de kans van de meting nul is.  Hoewel de resulterende status technisch niet is gedefinieerd in dit geval, hoeft u zich geen zorgen te maken over dergelijke gevallen, omdat de kans nul is.


Als we $ \psi $ de uniform State vector hebben die hierboven is gegeven en die de eerste Qubit graag moeten meten 

$ $ P (\Text{Measurement van First Qubit} = 1) = (\psi ^ \dagger e_2) (e_2 ^ \dagger \psi) + (\psi ^ \dagger e_3) (e_3 ^ \dagger \psi) = | e_2 ^ \dagger \psi | ^ 2 + | e_3 ^ \dagger \psi | ^ 2.
$$

Houd er rekening mee dat dit slechts de som is van de twee waarschijnlijkheden die worden verwacht voor het meten van de resultaten $10 $ en $11 $ waren alle qubits die moeten worden gemeten.
In ons voor beeld evalueert dit naar

$ $ \frac{1}{4}\left | \begin{bmatrix}0 & 0 & 1 & 0 \ end {bmatrix} \ begin {bmatrix} 1\\\\ 1\\\\ 1\\\\ 1 \ end {bmatrix} \right | ^ 2 + \frac{1}{4}\left | \ begin {bmatrix} 0 & 0 & 0 & 1 \ end {bmatrix} \ begin {bmatrix} 1\\\\ 1\\\\ 1\\\\ 1 \ end {bmatrix} \right | ^ 2 = \frac{1}{2}.
$$

wat precies overeenkomt met wat onze Intuition vertelt, zou ons moeten zijn.  Op dezelfde manier kan de status worden geschreven als

$ $ \frac{\frac{e_2}{2}+ \frac{e_3}{2}} {\sqrt{\frac{1}{2}}} = \frac{1}{\sqrt{2}} \begin{bmatrix} 0\\\\ 0\\\\ 1\\\\ 1 \ end {bmatrix} $ $

opnieuw in overeenstemming met onze intuition.

## <a name="two-qubit-operations"></a>Twee Qubit bewerkingen
Net als bij een single-Qubit-trans formatie is elke unitary-Transform een geldige bewerking op qubits. Over het algemeen is een unitary-trans formatie op $n $ qubits een matrix $U $ van grootte $2 ^ n \times 2 ^ n $ (zodat deze wordt toegepast op vectoren met een grootte van $2 ^ n $), zoals $U ^{-1} = U ^ \dagger $. De poort CNOT (Controlled-NOT) is bijvoorbeeld een gang bare twee Qubit-poort en wordt vertegenwoordigd door de volgende unitary-matrix:

$ $ \operatorname{CNOT} = \begin{bmatrix} 1 \ 0 \ 0 \ 0 \\\\ 0 \ 1 \ 0 \ 0 \\\\ 0 \ 0 \ 0 \ 1 \\\\ 0 \ 0 \ 1 \ 0 \end{bmatrix} $ $

We kunnen ook twee Qubit-poorten vormen door enkelvoudige Qubit-poorten op beide qubits toe te passen. Als we de Gates bijvoorbeeld Toep assen 

$ $ \begin{bmatrix} a \ b\\\\ c \ d \end{bmatrix} $ $

en de

$ $ \begin{bmatrix} e \ f\\\\ g \ h \end{bmatrix} $ $

op de eerste en tweede qubits is dit gelijk aan het Toep assen van de twee Qubit unitary die door hun tensor-product worden verstrekt: $ $ \begin{bmatrix} a \ b\\\\ c \ d \end{bmatrix} \otimes \begin{bmatrix} e \ f\\\\ g \ h \end{bmatrix} = \ begin {bmatrix} AE \ af \ BF \\\\ AG \ ah \ BG \ BH \\\\ CE \ CF \ de \ DF \\\\ CG \ CH \ DG \ DH \end{bmatrix}. $ $. Daarom kunnen we twee Qubit-poorten vormen door het tensor-product van sommige bekende single-Qubit-poorten te nemen. Enkele voor beelden van twee Qubit-Gates zijn $H \otimes H $, $X \otimes \boldone $ en $X \otimes Z $.

Houd er rekening mee dat hoewel er twee single-Qubit Gates een twee-Qubit poort definiëren door hun tensor-product te nemen. Niet alle twee Qubit-poorten kunnen worden geschreven als het tensor-product van single-Qubit Gates.  Een dergelijke poort wordt een *entangling* -poort genoemd. Een voor beeld van een entangling-Gate is de CNOT-poort.

De Intuition achter een Controlled-not-Gate kan worden gegeneraliseerd met wille keurige poorten.  Een beheerde poort in het algemeen is een poort die als identiteit fungeert (Internet Explorer heeft geen actie), tenzij een specifieke Qubit $1 $ is.  We geven een beheerde unitary aan, die in dit geval wordt gecontroleerd op de Qubit met het label $x $, met een $ \Lambda\_x (U) $.  Als voor beeld $ \Lambda_0 (U) e\_{1}\otimes {\psi} = e\_{1}\otimes U {\psi} $ en $ \Lambda\_0 (U) e\_{0}\otimes {\psi} = e\_{0}\otimes{\psi} $ , waarbij $e\_$0 en $e\_$1 de reken kundige basis vectoren zijn voor een enkele Qubit die overeenkomt met de waarden $0 $ en $1 $.  Houd er rekening mee dat u de volgende Controlled-$Z $ Gate zou kunnen uitdrukken als $ $ \Lambda\_0 (Z) = \begin{bmatrix}1 & 0 & 0 & 0\\\\0 & 1 & 0 & 0\\\\0 & 0 & 1 & 0\\\\0 & 0 & 0 &-1 \end{bmatrix} = (\boldone\otimes H) \operatorname{CNOT} (\boldone\otimes H).
$$

Het bouwen van beheerde unitaries op een efficiënte manier is een belang rijke uitdaging.  De eenvoudigste manier om dit te implementeren vereist het maken van een Data Base met gestuurde versies van fundamentele Gates en het vervangen van elke fundamentele poort in de oorspronkelijke unitary-bewerking met de gecontroleerde tegen hanger.  Dit is vaak zeer verspilling en slim inzicht kan worden gebruikt om alleen een aantal poorten met gecontroleerde versies te vervangen om dezelfde gevolgen te verkrijgen.  Daarom bieden we in ons Framework de mogelijkheid om de Naïve-methode voor het beheren of toestaan van de gebruiker om een gecontroleerde versie van de unitary te definiëren als een geoptimaliseerde, afgestemde versie bekend is.

Poorten kunnen ook worden beheerd met behulp van klassieke informatie.  Een klassiek niet-Gate is bijvoorbeeld gewoon een gewone not-Gate, maar wordt alleen toegepast als een klassieke bit $1 $ is in plaats van een Quantum bit.  In deze zin kan een klassieke beheerde poort worden beschouwd als een if-instructie in de Quantum code, waarbij de poort alleen in één vertakking van de code wordt toegepast.


Net als bij de single-Qubit is een Qubit-poort ingesteld op Universal als elke $4 \ Times $4 unitary matrix kan worden benaderd door een product van poorten van deze set tot wille keurige precisie.
Een voor beeld van een universele Gate set is de Hadamard-poort, de T-poort en de CNOT-poort. Door producten van deze Gates te nemen, kunnen we een wille keurige unitary-matrix op twee qubits benaderen.

## <a name="many-qubit-systems"></a>Veel Qubit systemen
We volgen precies dezelfde patronen in de tweequbite Case voor het bouwen van veel Qubit Quantum-statussen van kleinere systemen.  Dergelijke statussen zijn gebouwd door tensor producten van kleinere staten te maken.  U kunt bijvoorbeeld de bits teken reeks $1011001 $ in een quantum computer coderen.  We kunnen dit coderen als

$ $1011001 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{ bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}.
$$

Quantum Gates werken op dezelfde manier.  Als u de $X $ Gate bijvoorbeeld wilt Toep assen op de eerste Qubit en vervolgens een CNOT wilt uitvoeren tussen de tweede en derde qubits kunnen we deze trans formatie uitdrukken als

\begin{align} & (X \otimes \operatorname{CNOT}_{12}\otimes \boldone\otimes \boldone \otimes \boldone \otimes \boldone) \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\ otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\ otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\\\\ & \qquad\qquad\equiv 0011001.
\end{align}

In veel Qubit-systemen is het vaak nodig om qubits toe te wijzen en te detoewijzen die als tijdelijk geheugen voor de quantum computer fungeren.  Een dergelijke Qubit wordt een ancilla genoemd.  Standaard gaan we ervan uit dat de status Qubit is geïnitialiseerd voor $e _0 $ bij toewijzing.  We gaan ervan uit dat deze opnieuw wordt geretourneerd naar $e _0 $ vóór de toewijzing.  Deze veronderstelling is belang rijk, omdat als er een ancilla-Qubit wordt Entangled met een andere Qubit-registratie wanneer het opnieuw wordt toegewezen, wordt de ancilla door het proces van de toewijzing beschadigd.  Daarom wordt altijd aangenomen dat dergelijke qubits zijn teruggezet naar de oorspronkelijke status voordat ze worden vrijgegeven.

Ten slotte moeten er nieuwe poorten worden toegevoegd aan onze Gate-set voor het maken van Universal quantum computing voor twee Qubit quantum computers, maar moeten er geen nieuwe poorten worden geïntroduceerd in de multi-Qubit-case.  De poorten $H $, $T $ en CNOT vormen een universele poort die is ingesteld op veel qubits, omdat een algemene unitary-trans formatie kan worden opgesplitst in een reeks van twee Qubit draaiingen.  Vervolgens kunnen we gebruikmaken van de theorie die is ontwikkeld voor de twee qubite cases en deze hier opnieuw gebruiken als we veel qubits hebben.

Hoewel de lineaire algebraic notatie die we tot nu toe hebben gebruikt, kan worden gebruikt om de statussen voor meerdere Qubit te beschrijven, wordt het lastiger om de grootte van de statussen te verg Roten.  De resulterende kolom-vector voor een 7-bits teken reeks, bijvoorbeeld is $128 $ Dimensional, waardoor deze wordt omgeleid met de notatie die voorheen zeer lastig is beschreven.  Daarom pres teren we een gemeen schappelijke notatie in Quantum Computing, waarmee we deze zeer dimensionale vectoren beknopt kunnen beschrijven.
