---
title: Quantum computing woordenlijst
description: Een woordenlijst van veelvoorkomende termen, acties en objecten die worden gebruikt in quantum computing.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: ee78515a0f47730b7d3df10da0853c5b8a7f6624
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "81482205"
---
# <a name="quantum-computing-glossary"></a>Quantum computing woordenlijst

## <a name="adjoint"></a>Aangrenzende

De complexe conjugaat transponeren van een [operatie](xref:microsoft.quantum.glossary#operation). Voor bewerkingen die een [unitaire](xref:microsoft.quantum.glossary#unitary-operator) operator implementeren, is de aangrenzende het omgekeerde van de bewerking en wordt aangegeven met een dolksymbool. Als de bewerking `U` bijvoorbeeld de operator $U$ `Adjoint U` vertegenwoordigt, vertegenwoordigt u $U^\dolk$. Zie [Adjacentt](xref:microsoft.quantum.language.file-structure#adjoint)voor meer informatie.

## <a name="ancilla"></a>Ancilla (Ancilla)

Een [qubit](xref:microsoft.quantum.glossary#qubit) die dient als tijdelijk geheugen voor een quantumcomputer en wordt toegewezen en de-toegewezen als dat nodig is.  Zie [Meerdere qubits voor](xref:microsoft.quantum.concepts.multiple-qubits)meer informatie .

## <a name="bell-state"></a>De staat van de klok

Een van de vier specifieke maximaal [verstrengelde](xref:microsoft.quantum.glossary#entanglement) [kwantumtoestanden](xref:microsoft.quantum.glossary#quantum-state) van twee qubits. De vier staten zijn gedefinieerd $\ket{\beta_{ij}} = (\mathbb{I} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$. Een Bell staat is ook bekend als een [EPR paar](xref:microsoft.quantum.glossary#epr-pair).

## <a name="bloch-sphere"></a>Bloch bol

Een grafische weergave van een enkele[qubit](xref:microsoft.quantum.glossary#qubit) [kwantumtoestand](xref:microsoft.quantum.glossary#quantum-state) als punt in een driedimensionale eenheidsbol. Zie [Qubits en transformaties visualiseren met behulp van de Bloch Sphere](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)voor meer informatie.

## <a name="callable"></a>Belbaar

Een [bewerking](xref:microsoft.quantum.glossary#operation) of [functie](xref:microsoft.quantum.glossary#function) in de Q#-taal. Zie [Bewerkings- en functietypen](xref:microsoft.quantum.language.type-model#operation-and-function-types)voor meer informatie.

## <a name="clifford-group"></a>Clifford groep

De reeks bewerkingen die de octanten van de [Bloch-bol](xref:microsoft.quantum.glossary#bloch-sphere) bezetten en effectpermutaties van de [Pauli-operatoren](xref:microsoft.quantum.glossary#pauli-operators). Deze omvatten de activiteiten [$X$](xref:microsoft.quantum.intrinsic.x), [$Y$](xref:microsoft.quantum.intrinsic.y), [$Z$](xref:microsoft.quantum.intrinsic.z), [$H$](xref:microsoft.quantum.intrinsic.h) en [$S$ .](xref:microsoft.quantum.intrinsic.s)

## <a name="controlled"></a>Gecontroleerd

Een [kwantumbewerking](xref:microsoft.quantum.glossary#operation) waarbij een of meer [qubits](xref:microsoft.quantum.glossary#qubit) nodig zijn als enablers voor de doelbewerking. Zie [Gecontroleerd](xref:microsoft.quantum.language.type-model#controlled)voor meer informatie.

## <a name="dirac-notation"></a>Dirac-notatie

Een symbolische steno die de weergave van [kwantumtoestanden](xref:microsoft.quantum.glossary#quantum-state)vereenvoudigt , ook wel *bh-ket* notatie genoemd.  Het *bh-gedeelte* vertegenwoordigt een rijvector, bijvoorbeeld $\bra{A} = \begin{bmatrix} A{_1} & A{_2} \end{bmatrix}$ en het *ketgedeelte* vertegenwoordigt een kolomvector, \\ \\ $\ket{B} = \begin{bmatrix} B{_1} B{_2} \end{bmatrix}$. Zie [Dirac Notation](xref:microsoft.quantum.concepts.dirac)voor meer informatie.

## <a name="eigenvalue"></a>Eigenwaarde

De factor waarmee de omvang van een [eigenvector](xref:microsoft.quantum.glossary#eigenvector) van een bepaalde transformatie wordt veranderd door de toepassing van de transformatie.  Gezien een vierkante matrix $M $ en een eigenvector $v$, dan $Mv = cv $, waar $c $ is de eigenvalue en kan een complex aantal van elk argument. Zie [Geavanceerde matrixconcepten](xref:microsoft.quantum.concepts.matrix-advanced)voor meer informatie.

## <a name="eigenvector"></a>Eigenvector (Eigenvector)

Een vector waarvan de richting onveranderd is door een bepaalde transformatie en waarvan de omvang wordt gewijzigd door een factor die overeenkomt met [de eigenwaarde](xref:microsoft.quantum.glossary#eigenvalue)van die vector . Gezien een vierkante matrix $M$ en een eigenvalue $c$, dan $Mv = cv$, waar $v$ is een eigenvector van de matrix en kan een complex aantal van elk argument. Zie [Geavanceerde matrixconcepten](xref:microsoft.quantum.concepts.matrix-advanced)voor meer informatie.

## <a name="entanglement"></a>Entanglement

Quantumdeeltjes, zoals [qubits,](xref:microsoft.quantum.glossary#qubit)kunnen zodanig worden verbonden of *verstrengeld* dat ze niet onafhankelijk van elkaar kunnen worden beschreven. Hun meetresultaten zijn gecorreleerd, zelfs wanneer ze oneindig ver weg worden gescheiden. Verstrengeling is essentieel voor [het meten van](xref:microsoft.quantum.glossary#measurement) de [toestand](xref:microsoft.quantum.glossary#quantum-state) van een qubit.  Zie [Geavanceerde matrixconcepten](xref:microsoft.quantum.concepts.matrix-advanced)voor meer informatie.

## <a name="epr-pair"></a>EPR-paar

Een van de vier specifieke maximaal verstrengelde [kwantumtoestanden](xref:microsoft.quantum.glossary#quantum-state) van twee [qubits](xref:microsoft.quantum.glossary#qubit). De vier staten zijn gedefinieerd $\ket{\beta_{ij}}{1} = (\mathbb \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$. Een EPR-paar staat ook bekend als een [Bell-staat](xref:microsoft.quantum.glossary#bell-state)

## <a name="evolution"></a>Evolution

Hoe een [kwantumtoestand](xref:microsoft.quantum.glossary#quantum-state) verandert in de tijd. Zie [Matrix-exponentiële exponentieel voor](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)meer informatie.

## <a name="function"></a>Functie
Een type subroutine in de Q#-taal die puur klassiek is (niet-quantum). Hoewel functies worden gebruikt binnen kwantumalgoritmen, kunnen ze niet reageren op [qubits of](xref:microsoft.quantum.glossary#qubit) [calloperations.](xref:microsoft.quantum.glossary#operation) Zie [Bewerkings- en functietypen](xref:microsoft.quantum.language.type-model#operation-and-function-types)voor meer informatie.

## <a name="gate"></a>Gate

Een legacy term voor een quantum [operatie](xref:microsoft.quantum.glossary#operation), gebaseerd op het concept van de klassieke logica poorten. Een [kwantumcircuit](xref:microsoft.quantum.glossary#quantum-circuit-diagram) is een netwerk van poorten (of operaties), gebaseerd op het vergelijkbare concept van klassieke logische circuits.

## <a name="global-phase"></a>Globale fase

Wanneer twee [toestanden](xref:microsoft.quantum.glossary#quantum-state) identiek zijn aan een veelvoud van een complex getal $e^{i\phi}$, wordt gezegd dat ze verschillen tot een globale fase. In tegenstelling tot lokale fasen kunnen globale fasen niet worden waargenomen door middel [van een measurment](xref:microsoft.quantum.glossary#measurement). Zie [Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie .

## <a name="hadamard"></a>Hadamard

De Hadamard operatie (ook wel aangeduid als de Hadamard poort of transformeren) werkt op een{0}enkele [qubit](xref:microsoft.quantum.glossary#qubit) {1}en zet het in een [gelijkmatige superpositie](xref:microsoft.quantum.glossary#superposition) van $\ket $ of $\ket $ als de qubit is in eerste instantie in de $\ket{0}$ staat. In Q#wordt deze bewerking toegepast door [`H`](xref:microsoft.quantum.intrinsic.h) de vooraf gedefinieerde bewerking.

## <a name="immutable"></a>Onveranderlijke

Een variabele waarvan de waarde niet kan worden gewijzigd. Er wordt een onveranderlijke variabele `let` in Q# gemaakt met behulp van het trefwoord. Als u variabelen wilt declareren die *kunnen* worden gewijzigd, gebruikt u het [muteerom](xref:microsoft.quantum.glossary#immutable) te verklaren en het trefwoord om de `set` waarde te wijzigen. 

## <a name="measurement"></a>Meting

Een manipulatie van een [qubit](xref:microsoft.quantum.glossary#qubit) (of set qubits) die het resultaat van een observatie oplevert, in feite het verkrijgen van een klassieke bit. Zie [Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)voor meer informatie .

## <a name="mutable"></a>Veranderlijk

Een variabele waarvan de waarde kan worden gewijzigd nadat deze is gemaakt. Een veranderlijke variabele in Q# `mutable` wordt gedeclareerd met behulp van het trefwoord en gewijzigd met behulp van het `set` trefwoord. Variabelen die met `let` het zoekwoord zijn gemaakt, zijn [onveranderlijk](xref:microsoft.quantum.glossary#immutable) en de waarde ervan kan niet worden gewijzigd.

## <a name="namespace"></a>Naamruimte

Een label voor een verzameling verwante namen (d.w.z. [bewerkingen,](xref:microsoft.quantum.glossary#operation) [functies](xref:microsoft.quantum.glossary#function)en [door de gebruiker gedefinieerde typen).](xref:microsoft.quantum.glossary#user-defined-type) De naamruimte [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) labelt bijvoorbeeld alle symbolen die zijn gedefinieerd in de standaardbibliotheek die helpen bij het voorbereiden van de eerste status.

## <a name="operation"></a>Bewerking

De basiseenheid van quantum uitvoering in Q#. Het is ongeveer gelijk aan een functie in C, C++ of Python, of een statische methode in C# of Java. Zie [Bewerkings- en functietypen](xref:microsoft.quantum.language.type-model#operation-and-function-types)voor meer informatie.

## <a name="operator-application"></a>Operatortoepassing

Het uitvoeren van een kwantumoperatie. Hiermee wordt meestal een unitaire matrix gebruikt op de huidige quantumstatusvector.

## <a name="oracle"></a>Oracle

Een subroutine die gegevensafhankelijke informatie biedt aan een kwantumalgoritme tijdens runtime. Meestal is het doel om een [superpositie](xref:microsoft.quantum.glossary#superposition) van uitgangen die overeenkomen met ingangen die in superpositie. Zie [Oracles voor](xref:microsoft.quantum.libraries.data-structures#oracles)meer informatie.

## <a name="partial-application"></a>Gedeeltelijke toepassing

Het aanroepen van een [functie](xref:microsoft.quantum.glossary#function) of [bewerking](xref:microsoft.quantum.glossary#operation) zonder alle vereiste ingangen. Dit retourneert een nieuwe [aanroepbare](xref:microsoft.quantum.glossary#callable) die alleen de ontbrekende parameters (aangegeven door een underscore) hoeft te leveren tijdens een toekomstige toepassing. Bijvoorbeeld, gezien de `MyFunc(x : int, y : int) : int {return x + y;}` functie u deze gedeeltelijk `let NewFunc = MyFunc(_, 3)`toepassen op een nieuwe functie. U de nieuwe functie op een later `NewFunc(2)` tijdstip aanroepen met de ontbrekende parameter die de waarde *5*retourneert.  Zie [Gedeeltelijke toepassing](xref:microsoft.quantum.language.expressions#partial-application)voor meer informatie.

## <a name="pauli-operators"></a>Pauli exploitanten

Een set van drie 2 x 2 unitaire `Y` `Z` matrices bekend als de `X`, en quantum operaties. De identiteitsmatrix, $I$, is vaak ook opgenomen in de set.  $I = \begin{bmatrix} \\ \\ 1 & 0 0 & 1 \end{bmatrix}$, $X \\ \\ = \begin{bmatrix} 0 & 1 1 & 0 \end{bmatrix}$, $Y = \begin{bmatrix} 0 & -i \\ \\ & 0 \end{bmatrix}$, $Z = \begin{bmatrix} 1 & 0 \\ \\ 0 & -1 \end{bmatrix}$.   Zie [Single-qubit-bewerkingen](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)voor meer informatie .

## <a name="quantum-circuit-diagram"></a>Diagram quantumcircuit

Een methode om de volgorde van [bewerkingen](xref:microsoft.quantum.glossary#operation) (of [poorten)](xref:microsoft.quantum.glossary#gate)grafisch](~/media/qpe.png)weer te geven voor eenvoudige kwantumprogramma's, bijvoorbeeld Het circuitdiagram van de steekproef ![. Zie [Quantumcircuits voor](xref:microsoft.quantum.concepts.circuits)meer informatie.

## <a name="quantum-libraries"></a>Kwantumbibliotheken

Verzamelingen van [bewerkingen,](xref:microsoft.quantum.glossary#operation) [functies](xref:microsoft.quantum.glossary#function) en door de gebruiker gedefinieerde typen voor het maken van Q#-programma's. [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) De [standaardbibliotheek](xref:microsoft.quantum.libraries.standard.intro) is standaard geïnstalleerd. Andere bibliotheken beschikbaar zijn de [Scheikundebibliotheek,](xref:microsoft.quantum.chemistry.concepts.intro)de [Bibliotheek Numeriek en](xref:microsoft.quantum.numerics.intro) de [machineleerbibliotheek.](xref:microsoft.quantum.machine-learning.concepts.intro)

## <a name="quantum-state"></a>Kwantumtoestand

De precieze toestand van een geïsoleerd kwantumsysteem, waaruit [meetkansen](xref:microsoft.quantum.glossary#measurement) kunnen worden geëxtraheerd. In quantum computing gebruikt de quantumsimulator deze informatie om te simuleren hoe qubits reageren op bewerkingen. Zie [Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie .

## <a name="qubit"></a>Qubit Qubit

Een basiseenheid van kwantuminformatie, analoog aan een *beetje* in de klassieke informatica. Zie [Qubit](xref:microsoft.quantum.concepts.qubit)voor meer informatie .

## <a name="repeat-until-success"></a>Herhaling-tot-succes

Een kwantumalgoritme dat probabilistically slaagt. Na het mislukken, zal de routine opnieuw proberen totdat succesvol (of een limiet is bereikt). Zie [Herhalen tot succes (RUS)](xref:microsoft.quantum.techniques.qubits#measurements) voor meer informatie

## <a name="standard-libraries"></a>Standaardbibliotheken

[Bewerkingen,](xref:microsoft.quantum.glossary#operation) [functies](xref:microsoft.quantum.glossary#function) en door de gebruiker gedefinieerde typen die tijdens de installatie samen met de [Q#-compiler](xref:microsoft.quantum.glossary#user-defined-type) zijn geïnstalleerd. De standaard bibliotheekimplementatie is agnostisch met betrekking tot doelmachines. Zie [Standaardbibliotheken voor](xref:microsoft.quantum.libraries.standard.intro)meer informatie .

## <a name="superposition"></a>Superpositie

Het concept in quantum computing dat een [qubit](xref:microsoft.quantum.glossary#qubit) een lineaire combinatie is van twee toestanden, $\ket{\0}$ en $\ket{\1}$, totdat deze wordt [gemeten.](xref:microsoft.quantum.glossary#measurement)  Zie [Wat is quantum computing](xref:microsoft.quantum.overview.what)voor meer informatie.

## <a name="target-machine"></a>Doelmachine

Een compilatiedoel dat een abstract kwantumprogramma verlaagt naar hardware of simulatie. Dit omvat meestal herschrijft voor vele doeleinden, waaronder poortvervanging, codering voor foutcorrectie, geometrische lay-out en anderen. Zie [Quantumsimulators en hosttoepassingen voor](xref:microsoft.quantum.machines)meer informatie.

## <a name="teleportation"></a>Teleportatie

Een methode voor het regenereren van gegevens, of de [kwantumtoestand](xref:microsoft.quantum.glossary#quantum-state), van de [ene qubit](xref:microsoft.quantum.glossary#qubit) van de ene plaats naar de andere zonder de qubit fysiek te verplaatsen, met behulp van [verstrengeling](xref:microsoft.quantum.glossary#entanglement) en [meting](xref:microsoft.quantum.glossary#measurement).  Zie [Quantumcircuits](xref:microsoft.quantum.concepts.circuits) en [Putting it all together](xref:microsoft.quantum.techniques.puttingittogether)voor meer informatie.

## <a name="tuple"></a>Tupel

Een verzameling door komma's gescheiden waarden die als één waarde fungeert. Het *type* tuple wordt gedefinieerd door de typen waarden die het bevat. In Q#zijn tuples [onveranderlijk](xref:microsoft.quantum.glossary#immutable) en kunnen ze worden genest, arrays bevatten of in een array worden gebruikt. Zie [Tuple-typen](xref:microsoft.quantum.language.type-model#tuple-types)voor meer informatie.

## <a name="unitary-operator"></a>Unitaire operator

Een operator waarvan de omgekeerde is gelijk aan de [aangrenzende](xref:microsoft.quantum.glossary#adjoint), dat wil zeggen, $UU^{\dolk} = \id$.

## <a name="user-defined-type"></a>Door de gebruiker gedefinieerd type

Een verzameling ingebouwde of eerder gedefinieerde typen die één eenheid kunnen worden genoemd. Zie [Door de gebruiker gedefinieerde typen voor](xref:microsoft.quantum.language.type-model#user-defined-types)meer informatie.