---
Titel: beschrijving van de Quantum Computing-woorden lijst: een woorden lijst met algemene termen, acties en objecten die worden gebruikt in Quantum Computing.
Auteur: bradben MS. Author: v-benbra MS. date: 9/1/2020 MS. topic: Reference UID: micro soft. Quantum. Glossary no-loc:
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

# <a name="quantum-computing-glossary"></a>Woorden lijst voor Quantum Computing

## <a name="adjoint"></a>Adjoint

De complex geconjugeerde omzetting van een [bewerking](xref:microsoft.quantum.glossary#operation). Voor bewerkingen waarbij een [unitary](xref:microsoft.quantum.glossary#unitary-operator) -operator wordt geïmplementeerd, is de adjoint de inverse van de bewerking en wordt aangegeven door een Dagger-symbool. Als de bewerking bijvoorbeeld `U` de unitary-operator u vertegenwoordigt $ $ , `Adjoint U` vertegenwoordigt $ u ^ \dagger $ . Zie [functor Application](xref:microsoft.quantum.qsharp.functorapplication#functor-application)(Engelstalig) voor meer informatie.

## <a name="ancilla"></a>Ancilla

Een [Qubit](xref:microsoft.quantum.glossary#qubit) die fungeert als tijdelijk geheugen voor een quantum computer en zo nodig wordt toegewezen en toegewezen.  Zie [meerdere qubits](xref:microsoft.quantum.concepts.multiple-qubits)voor meer informatie.

## <a name="bell-state"></a>Bell-status

Een van de vier specifieke maximally [Entangled](xref:microsoft.quantum.glossary#entanglement) [Quantum-statussen](xref:microsoft.quantum.glossary#quantum-state) van twee qubits. De vier statussen zijn gedefinieerd $ \ket { \beta _ { ij } } = ( \mathbb { I } \otimes X ^ iz ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ . Een Bell-status wordt ook wel een [EPR-paar](xref:microsoft.quantum.glossary#epr-pair)genoemd.

## <a name="bloch-sphere"></a>Bloch-bol

Een grafische weer gave van een [Quantum status](xref:microsoft.quantum.glossary#quantum-state) met één[Qubit](xref:microsoft.quantum.glossary#qubit) als een punt in een drie-dimensionale eenheid. Zie  [qubits en trans formaties visualiseren met behulp van de Bloch-bol](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)voor meer informatie.

## <a name="callable"></a>Aanroep bare

Een [bewerking](xref:microsoft.quantum.glossary#operation) of [functie](xref:microsoft.quantum.glossary#function) in de [ Q# taal](https://github.com/microsoft/qsharp-language/tree/main/Specifications/Language#q-language).
Zie [ Q# Program ma's](xref:microsoft.quantum.guide.programs) voor meer informatie.

## <a name="clifford-group"></a>Clifford-groep

De set bewerkingen die de octants van de Bloch- [bol](xref:microsoft.quantum.glossary#bloch-sphere) in beslag nemen en permutaties van de [Pauli-Opera tors](xref:microsoft.quantum.glossary#pauli-operators). Dit zijn onder andere de bewerkingen [ $ X $ ](xref:Microsoft.Quantum.Intrinsic.X), [ $ Y $ ](xref:Microsoft.Quantum.Intrinsic.Y), [ $ Z $ ](xref:Microsoft.Quantum.Intrinsic.Z), [ $ H $ ](xref:Microsoft.Quantum.Intrinsic.H) en [ $ S $ ](xref:Microsoft.Quantum.Intrinsic.S).

## <a name="controlled"></a>Gelijkrichter

Een Quantum [bewerking](xref:microsoft.quantum.glossary#operation) waarbij een of meer [qubits](xref:microsoft.quantum.glossary#qubit) als enablers voor de doel bewerking worden gebruikt. Zie [functor Application](xref:microsoft.quantum.qsharp.functorapplication#functor-application)(Engelstalig) voor meer informatie.

## <a name="dirac-notation"></a>Dirac-notatie

Een symbolische steno waarmee de weer gave van [Quantum statussen](xref:microsoft.quantum.glossary#quantum-state), ook wel *bra-ket* notatie, wordt vereenvoudigd.  Het gedeelte *Bra* vertegenwoordigt een vector voor een rij, bijvoorbeeld $ \bra { een } = \begin{bmatrix} { _1 } & a { _2 } \end{bmatrix} $ en het gedeelte *Ket* vertegenwoordigt een kolom vector, $ \ket { b } = \begin{bmatrix} b { _1 } \\\\ b { _2 } \end{bmatrix} $ . Zie [Dirac-notatie](xref:microsoft.quantum.concepts.dirac)voor meer informatie.

## <a name="eigenvalue"></a>Eigenvalue

De factor waarmee de grootte van een [eigenvector](xref:microsoft.quantum.glossary#eigenvector) van een bepaalde trans formatie wordt gewijzigd door de toepassing van de trans formatie.  Gezien een vier Kante matrix $ M $ en een eigenvector $ v $ , wordt $ = $ de AVK, waarbij $ c $ de eigenvalue is, en een complex aantal argumenten. Zie [Advanced matrix concepten](xref:microsoft.quantum.concepts.matrix-advanced)(Engelstalig) voor meer informatie.

## <a name="eigenvector"></a>Eigenvector

Een vector waarvan de richting wordt gewijzigd door een bepaalde trans formatie en waarvan de grootte wordt gewijzigd door een factor die overeenkomt met de [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)van die vector. Op basis van een vier Kante matrix $ M $ en een eigenvalue $ c $ , $ = $ wordt de AVK, waarbij $ v $ een eigenvector van de matrix is, en een complex aantal argumenten. Zie [Advanced matrix concepten](xref:microsoft.quantum.concepts.matrix-advanced)(Engelstalig) voor meer informatie.

## <a name="entanglement"></a>Verstrengeling

Quantum deeltjes, zoals [qubits](xref:microsoft.quantum.glossary#qubit), kunnen worden aangesloten of *Entangled* , zodat ze onafhankelijk van elkaar kunnen worden beschreven. De meet resultaten worden ook gecorreleerd wanneer ze oneindig ver van elkaar zijn gescheiden. Entanglement is essentieel om de [status](xref:microsoft.quantum.glossary#quantum-state) van een Qubit te [meten](xref:microsoft.quantum.glossary#measurement) .  Zie [Advanced matrix concepten](xref:microsoft.quantum.concepts.matrix-advanced)(Engelstalig) voor meer informatie.

## <a name="epr-pair"></a>EPR paar

Een van de vier specifieke maximally Entangled [Quantum-statussen](xref:microsoft.quantum.glossary#quantum-state) van twee [qubits](xref:microsoft.quantum.glossary#qubit). De vier statussen zijn gedefinieerd $ \ket { \beta _ { ij } } = ( \mathbb { 1 } \otimes X ^ iz ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ . Een EPR-paar wordt ook wel een [Bell-status](xref:microsoft.quantum.glossary#bell-state) genoemd

## <a name="evolution"></a>Evolutie

Hoe een [Quantum status](xref:microsoft.quantum.glossary#quantum-state) in de loop van de tijd verandert. Zie [matrix exponentiëlen](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)voor meer informatie.

## <a name="function"></a>Functie
Een type subroutine in de Q# taal die louter deterministisch is. Terwijl functies worden gebruikt binnen Quantum algoritmen, kunnen ze niet reageren op [qubits](xref:microsoft.quantum.glossary#qubit) of aanroep [bewerkingen](xref:microsoft.quantum.glossary#operation). Zie [ Q# Program ma's](xref:microsoft.quantum.guide.programs) voor meer informatie.

## <a name="gate"></a>Poort

Een verouderde term voor bepaalde ingebouwde Quantum [bewerkingen](xref:microsoft.quantum.glossary#operation), op basis van het concept van klassieke logische poorten. Een [Quantum circuit](xref:microsoft.quantum.glossary#quantum-circuit-diagram) is een netwerk van Gates, op basis van het vergelijk bare concept van klassieke logica-circuits.

## <a name="global-phase"></a>Globale fase

Wanneer twee [statussen](xref:microsoft.quantum.glossary#quantum-state) gelijk zijn aan een meervoud van een complex getal $ e ^ { i \phi } $ , worden ze in een wereld wijde fase onderscheiden. In tegens telling tot lokale fasen kunnen globale fasen niet worden geobserveerd met behulp van enige [meet](xref:microsoft.quantum.glossary#measurement)periode. Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie.

## <a name="hadamard"></a>Hadamard

De Hadamard-bewerking (ook wel de Hadamard-Gate of Transform genoemd) werkt op één [Qubit](xref:microsoft.quantum.glossary#qubit) en plaatst deze in een even super [positie](xref:microsoft.quantum.glossary#superposition) van $ \ket { 0 } $ of $ \ket { 1 } $ als de Qubit in eerste instantie de $ \ket { status 0 heeft } $ . In Q# wordt deze bewerking toegepast door de vooraf gedefinieerde [`H`](xref:Microsoft.Quantum.Intrinsic.H) bewerking.

## <a name="immutable"></a>Onveranderbare

Een variabele waarvan de waarde niet kan worden gewijzigd. Een onveranderbare variabele in Q# wordt gemaakt met behulp van het `let` sleutel woord. Als u variabelen wilt declareren die *kunnen* worden gewijzigd, gebruikt u het sleutel woord [onveranderbaar](xref:microsoft.quantum.glossary#immutable) om te declareren en het `set` tref woord om de waarde te wijzigen. 

## <a name="measurement"></a>Meting

Een manipulatie van een [Qubit](xref:microsoft.quantum.glossary#qubit) (of set qubits) die het resultaat van een waarneming oplevert, in feite het verkrijgen van een klassieke bit. Zie [de Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)voor meer informatie.

## <a name="mutable"></a>Veranderlijk

Een variabele waarvan de waarde kan worden gewijzigd nadat deze is gemaakt. Een onveranderlijke variabele in Q# wordt gedeclareerd met het `mutable` sleutel woord en gewijzigd met het `set` sleutel woord. Variabelen die met het `let` sleutel woord zijn gemaakt, zijn [onveranderbaar](xref:microsoft.quantum.glossary#immutable) en hun waarde kan niet worden gewijzigd.

## <a name="namespace"></a>Naamruimte

Een label voor een verzameling verwante namen (bijvoorbeeld [bewerkingen](xref:microsoft.quantum.glossary#operation), [functies](xref:microsoft.quantum.glossary#function)en door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.glossary#user-defined-type)). Voor de naam ruimte [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation) etiketten worden alle symbolen in de standaard bibliotheek beschreven die u helpen bij het voorbereiden van initiële statussen.

## <a name="operation"></a>Bewerking

De basis eenheid van de Quantum berekening in Q# . Het is ongeveer gelijk aan een functie in C, C++ of python, of een statische methode in C# of Java. Zie [ Q# Program ma's](xref:microsoft.quantum.guide.programs)voor meer informatie.

## <a name="oracle"></a>Oracle

Een subroutine die gegevens afhankelijke informatie levert aan een Quantum algoritme tijdens runtime. Normaal gesp roken is het doel om een [superpositie](xref:microsoft.quantum.glossary#superposition) van uitvoer te bieden die overeenkomt met de invoer die zich in superpositie bevindt. Zie voor meer informatie [Oracle](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>Gedeeltelijke toepassing

Het aanroepen van een [functie](xref:microsoft.quantum.glossary#function) of [bewerking](xref:microsoft.quantum.glossary#operation) zonder de vereiste invoer. Hiermee wordt een nieuwe [aanroep](xref:microsoft.quantum.glossary#callable) geretourneerd waarvoor alleen de ontbrekende para meters (aangegeven door een onderstrepings teken) moeten worden opgegeven tijdens een toekomstige toepassing. Zie voor meer informatie [gedeeltelijke toepassing](xref:microsoft.quantum.qsharp.partialapplication).

## <a name="pauli-operators"></a>Pauli-Opera tors

Een set van 3 2 x 2 unitary-matrices, ook wel bekend als de `X` , `Y` en `Z` Quantum bewerkingen. De ID-matrix, $ I $ , wordt vaak ook opgenomen in de set.  $I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix} $ , $ X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} $ , $ Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix} $ , $ Z = \begin{bmatrix} 1 & 0 \\\\ & -1 \end{bmatrix} $ .   Zie [Single-Qubit Operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)(Engelstalig) voor meer informatie.

## <a name="quantum-circuit-diagram"></a>Quantum circuit diagram

Een methode voor het grafisch weer geven van de reeks [poorten](xref:microsoft.quantum.glossary#gate) voor eenvoudige Quantum-Program ma's, bijvoorbeeld 

![Voorbeeld diagram van circuit](~/media/qpe.png). 

Zie [Quantum circuits](xref:microsoft.quantum.concepts.circuits)voor meer informatie.

## <a name="quantum-libraries"></a>Quantum bibliotheken

Verzamelingen [bewerkingen](xref:microsoft.quantum.glossary#operation), [functies](xref:microsoft.quantum.glossary#function) en door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.glossary#user-defined-type) voor het maken van Q# Program ma's. De [standaard bibliotheek](xref:microsoft.quantum.libraries.standard.intro) wordt standaard geïnstalleerd. Andere beschik bare bibliotheken zijn de [bibliotheek voor schei kunde](xref:microsoft.quantum.chemistry.concepts.intro), de [numerieke bibliotheek](xref:microsoft.quantum.numerics.intro) en de [machine learning-bibliotheek](xref:microsoft.quantum.machine-learning.concepts.intro).

## <a name="quantum-state"></a>Quantum status

De nauw keurige status van een geïsoleerd Quantum systeem, waaruit [meting](xref:microsoft.quantum.glossary#measurement) kansen kunnen worden geëxtraheerd. In Quantum Computing gebruikt de Quantum Simulator deze informatie om te simuleren hoe qubits reageert op bewerkingen. Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie.

## <a name="qubit"></a>Qubit

Een eenvoudige eenheid van quantum informatie, vergelijkbaar met een *bit* in klassieke computing. Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie.

## <a name="repeat-until-success"></a>Herhalen-tot-geslaagd

Een concept dat vaak wordt gebruikt in Quantum algoritmen die bestaan uit het herhaaldelijk Toep assen van een berekening tot aan een bepaalde voor waarde is voldaan. Als er niet aan de voor waarde is voldaan, is er vaak een reparatie vereist voordat het opnieuw wordt geprobeerd door de volgende iteratie in te voeren. Zie de [ Q# Gebruikers handleiding](xref:microsoft.quantum.guide) voor meer informatie

## <a name="standard-libraries"></a>Standaardbibliotheken

[Bewerkingen](xref:microsoft.quantum.glossary#operation), [functies](xref:microsoft.quantum.glossary#function) en door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.glossary#user-defined-type) die samen met de compiler worden geïnstalleerd Q# tijdens de installatie. De implementatie van de standaard bibliotheek is neutraal met betrekking tot doel computers. Zie [standaard bibliotheken](xref:microsoft.quantum.libraries.standard.intro)voor meer informatie.

## <a name="superposition"></a>Superpositie

Het concept in het quantum computing dat een [Qubit](xref:microsoft.quantum.glossary#qubit) is een lineaire combi natie van twee statussen, $ \ket { 0 } $ en $ \ket { 1 } $ tot deze wordt [gemeten](xref:microsoft.quantum.glossary#measurement).  Zie [informatie over Quantum Computing](xref:microsoft.quantum.overview.understanding)voor meer informatie.

## <a name="target-machine"></a>Doel computer

Een compilatie doel dat een abstract Quantum programma verlaagt naar hardware of simulatie. Dit omvat doorgaans herschrijf bewerkingen voor veel doelen, waaronder het vervangen van een Gate, code ring voor fout correctie, geometrische indeling en andere. Zie [Quantum simulators and host Applications](xref:microsoft.quantum.machines)(Engelstalig) voor meer informatie.

## <a name="teleportation"></a>Teleportatie

Een methode voor het opnieuw genereren van gegevens, of de [Quantum status](xref:microsoft.quantum.glossary#quantum-state), van een [Qubit](xref:microsoft.quantum.glossary#qubit) van de ene locatie naar een andere zonder fysiek de Qubit te verplaatsen, met [entanglement](xref:microsoft.quantum.glossary#entanglement) en [meting](xref:microsoft.quantum.glossary#measurement).  Zie [Quantum circuits](xref:microsoft.quantum.concepts.circuits) en de respectieve Kata bij [Quantum Katas](xref:microsoft.quantum.overview.katas)voor meer informatie.

## <a name="tuple"></a>Kaart

Een verzameling door komma's gescheiden waarden die fungeert als een enkele waarde. Het *type* van een tuple wordt gedefinieerd door de typen waarden die deze bevat. In Q# zijn Tuples [onveranderbaar](xref:microsoft.quantum.glossary#immutable) en kunnen worden genest, matrices bevatten of worden gebruikt in een matrix. Zie [Tuples](xref:microsoft.quantum.qsharp.valueliterals#tuple-literals)voor meer informatie.

## <a name="unitary-operator"></a>Unitary-operator

Een operator waarvan de inverse is gelijk aan de [adjoint](xref:microsoft.quantum.glossary#adjoint), d.w.z. $ uu ^ { \dagger } = \id $ .

## <a name="user-defined-type"></a>Door de gebruiker gedefinieerd type

Een aangepast type dat een of meer benoemde of anonieme items kan bevatten. Zie [type declaraties] micro soft. Quantum. qsharp. typedeclarations # type-declaraties voor meer informatie.
