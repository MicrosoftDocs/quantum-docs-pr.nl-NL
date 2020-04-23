---
title: Q# technieken - Alles in elkaar zetten
description: Loop door een basis Q# programma dat kwantumteleportatie demonstreert.
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030562"
---
# <a name="putting-it-all-together-teleportation"></a>Putting It All Together: Teleportatie #
Laten we terugkeren naar het voorbeeld van het teleportatiecircuit gedefinieerd in [Quantum Circuits.](xref:microsoft.quantum.concepts.circuits) We gaan dit gebruiken om de concepten te illustreren die we tot nu toe hebben geleerd. Een uitleg van quantum teleportatie is hieronder voorzien voor degenen die niet bekend zijn met de theorie, gevolgd door een walkthrough van de code implementatie in Q#. 

## <a name="quantum-teleportation-theory"></a>Quantum Teleportatie: Theorie
Quantum teleportatie is een techniek voor het verzenden van een onbekende kwantumtoestand (die we zullen noemen de '__boodschap__') van een qubit op een locatie naar een qubit op een andere locatie (we zullen verwijzen naar deze qubits als '__hier__' en '__er__', respectievelijk). We kunnen onze __boodschap__ als een vector vertegenwoordigen met Dirac-notatie: 

$$ \ket{\psi} = \alpha\ket{0} +{1} \beta\ket $$

De status van de __boodschap__ qubit is onbekend voor ons als we niet weten wat de waarden van $\alpha $ en $\beta$.

### <a name="step-1-create-an-entangled-state"></a>Stap 1: Een verstrengelde toestand maken
Om het __bericht__ te sturen moeten we voor de qubit __hier__ te worden verstrikt met de qubit __daar__. Dit wordt bereikt door het toepassen van een Hadamard poort, gevolgd door een CNOT poort. Laten we eens kijken naar de wiskunde achter deze poort operaties.

We zullen beginnen met de qubits __hier__ en{0} __daar__ zowel in de $ \ ket $ staat. Na het verwarren van deze qubits, zijn ze in de staat:

$$ \ket{\phi^+} ={1}\frac{2}{\sqrt{00} }(\ket + \ket{11}) $$

### <a name="step-2-send-the-message"></a>Stap 2: Het bericht verzenden
Om het __bericht__ te verzenden passen we eerst een CNOT-poort toe met de __message__ qubit en __hier__ qubit als inputs (het __bericht__ qubit is de controle en de __here__ qubit is het doel qubit, in dit geval). Deze invoerstatus kan worden geschreven:

$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} +{1}\beta\ket)(\frac{1}{\sqrt{2}{00} {11}}(\ket + \ket)) $$

Dit breidt zich uit naar:

$${2}\ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{000} }\ket +{2}\frac{\alpha}{\sqrt }\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} +{2}\frac{\beta}{\sqrt }\ket{111} $$

Ter herinnering, de CNOT-poort draait de doelqubit wanneer de controle qubit is 1. Dus bijvoorbeeld, een input van{000}$\ket $ zal resulteren in geen verandering als de eerste qubit (het besturingselement) is 0. Neem echter een geval waarbij de eerste qubit 1 is{100}- bijvoorbeeld een invoer van $\ket $. In dit geval is de{110}uitvoer $\ket $ als de tweede qubit (het doel) wordt omgedraaid door de CNOT-poort.

Laten we nu overwegen onze output zodra de CNOT poort heeft gehandeld op onze input hierboven. Het resultaat is:

$${2}\frac{\alpha}{\sqrt }\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$

De volgende stap om het __bericht__ te verzenden is het toepassen van een Hadamard poort op het __bericht__ qubit (dat is de eerste qubit van elke term). 

Ter herinnering, de Hadamard poort doet het volgende:

Invoer | Uitvoer
---------------------------| ---------------------------------------------------------------
$\ket{0}$  | $\frac{1}{\sqrt{2}}(\ket{0} {1}+ \ket )$
$\ket{1}$  | $\frac{1}{\sqrt{2}}(\ket{0} {1}- \ket )$

Als we de Hadamard-poort toepassen op de eerste qubit van elke termijn van onze bovenstaande output, krijgen we het volgende resultaat:

{2}$$ \frac{\alpha}{\sqrt }(\frac{1}{\sqrt{2}{0} }(\ket +{00} \ket)\ket{2}{1}{2}{0} {1}{11} {2}{1}{2}{0} {1}{10} {2}{1}+ \frac{\alpha}{\sqrt }(\frac {\sqrt }(\ket + \ket)\ket + ket + \frac{\beta}{\sqrt }(\frac {\sqrt }(\ket -{1}\ket)\ket{2}+ \frac{\beta}{\sqrt }(\frac {\sqrt }(\ket{0} - \ket)\ket{1}{01} $$

Houd er rekening mee dat{1}elke term{2}twee $\frac {\sqrt }$ factoren heeft. We kunnen vermenigvuldigen deze uit het geven van het volgende resultaat:

$${2}\frac{\alpha} (\ket{0} {1}+ \ket)\ket{00} +{2}\frac{\alpha}{0} (\ket + \ket)\ket{1}{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket){1}{01} \ket

De $\frac{1}{2}$ factor is gemeenschappelijk voor elke term, zodat we nu kunnen nemen buiten de haakjes:

$${1}{2}\frac \big[\alpha(\ket{0} {1}+ \ket)\ket{00} +{0} \alpha(\ket + \ket)\ket{1}{11} +{0} \beta(\ket -{0} \ket)\ket{01}{1}{10} + \beta(\ket - \ket)\ket{1}\big] $$

We kunnen dan vermenigvuldigen uit de haakjes voor elke term geven:

$$ \frac{1}{2}\big[\alpha\ket{000} +{100} \alpha\ket{011} + \alpha\ket +{111} \alpha\ket + \beta\ket{001} {101}{010} - \beta\ket{110} + \beta\ket - \beta\ket \big] $$

### <a name="step-3-measure-the-result"></a>Stap 3: Meet het resultaat

Als gevolg van __hier__ en __daar__ verstrikt, elke meting op __hier__ zal invloed hebben op de toestand van __daar__. Als we meten de eerste en tweede qubit __(bericht__ en __hier__) kunnen we leren welke staat __er__ is in, als gevolg van deze eigenschap van verstrengeling. 

* Als we meten en krijgen een resultaat 00, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat. Dat is $\alpha\ket{000} +\beta\ket{001}$. Dit kan worden aangepast aan{00}$\ket (\alpha\ket{0} {1}+\beta\ket)$. Daarom als we meten de eerste en tweede qubit te zijn __there__00, weten we dat de{0} derde qubit, er , is in de staat $(\alpha\ket +\beta\ket)$.{1}
* Als we meten en krijgen een resultaat 01, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat. Dat is $\alpha\ket{011} +\beta\ket{010}$. Dit kan worden aangepast aan{01}$\ket (\alpha\ket{1} {0}+\beta\ket)$. Daarom als we meten de eerste en tweede qubit te zijn __there__01, weten we dat de{1} derde qubit, er , is in de staat $(\alpha\ket +\beta\ket)$.{0}
* Als we meten en krijgen een resultaat 10, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat. Dat is $\alpha\ket{100} -\beta\ket{101}$. Dit kan worden aangepast aan{10}$\ket (\alpha\ket{0} {1}-\beta\ket)$. Daarom als we meten de eerste en tweede qubit te zijn __there__10, weten we dat de{0} derde qubit, er , is in de staat $(\alpha\ket -\beta\ket)$.{1}
* Als we meten en krijgen een resultaat 11, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat. Dat is $\alpha\ket{111} -\beta\ket{110}$. Dit kan worden aangepast aan{11}$\ket (\alpha\ket{1} {0}-\beta\ket)$. Daarom als we meten de eerste en tweede qubit te zijn __there__11, weten we dat de{1} derde qubit, er , is in de staat $(\alpha\ket -\beta\ket)$.{0}

### <a name="step-4-interpret-the-result"></a>Stap 4: Interpreteer het resultaat

Ter herinnering, het oorspronkelijke __bericht__ dat we wilden sturen was:

$$ \ket{\psi} = \alpha\ket{0} +{1} \beta\ket $$

We moeten de __qubit in__ deze staat krijgen, zodat de ontvangen toestand degene is die bedoeld was. 

* Als we gemeten en kreeg een resultaat van 00, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{0} +\beta\ket)$.{1} Aangezien dit het beoogde __bericht__is, is er geen wijziging nodig.
* Als we gemeten en kreeg een resultaat van 01, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{1} +\beta\ket)$.{0} Dit verschilt van het beoogde __bericht,__ maar het toepassen van een NOT-poort{0} geeft ons{1}de gewenste status $(\alpha\ket +\beta\ket)$.
* Als we gemeten en kreeg een resultaat van 10, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{0} -\beta\ket)$.{1} Dit verschilt van het beoogde __bericht,__ maar het toepassen van een Z-poort{0} geeft ons{1}de gewenste staat $(\alpha\ket +\beta\ket)$.
* Als we gemeten en kreeg een resultaat van 11, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{1} -\beta\ket)$.{0} Dit verschilt van het beoogde __bericht,__ maar het toepassen van een NOT-poort gevolgd door{0} een Z-poort{1}geeft ons de gewenste staat $(\alpha\ket +\beta\ket)$.

Samenvattend, als we meten en de eerste qubit is 1, een Z-poort wordt toegepast. Als we meten en de tweede qubit is 1, een NOT poort wordt toegepast.

### <a name="summary"></a>Samenvatting
Hieronder is een tekst-boek quantum circuit dat de teleportatie implementeert. Als u van links naar rechts gaat, u zien:
- Stap 1: Verwaren __hier__ en __daar__ door het toepassen van een Hadamard poort en CNOT poort.
- Stap 2: Het verzenden van het __bericht__ met behulp van een CNOT-poort en een Hadamard-poort.
- Stap 3: Het nemen van een meting van de eerste en tweede qubits, __bericht__ en __hier__.
- Stap 4: Het aanbrengen van een NOT-poort of een Z-poort, afhankelijk van het resultaat van de meting in stap 3.

!["Teleport(msg : Qubit, there : Qubit) : Unit"](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a>Quantum Teleportatie: Code

We hebben ons circuit voor kwantumteleportatie:

!["Teleport(msg : Qubit, there : Qubit) : Unit"](~/media/teleportation.svg)

We kunnen nu elk van de stappen in dit kwantumcircuit vertalen naar Q#.

### <a name="step-0-definition"></a>Stap 0: Definitie
Wanneer we teleportatie uitvoeren, moeten we weten welke __boodschap__ we willen sturen, en waar we het __(daar)__ willen sturen. Om deze reden beginnen we met het definiëren van een nieuwe `msg` Teleport-bewerking die twee qubits als argumenten krijgt, en: `there`

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

We moeten ook een `here` qubit toewijzen `using` die we bereiken met een blok:

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a>Stap 1: Een verstrengelde toestand maken
We kunnen dan het verstrengelde `there` paar @"microsoft.quantum.intrinsic.h" tussen @"microsoft.quantum.intrinsic.cnot" `here` en met behulp van de en operaties:

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a>Stap 2: Het bericht verzenden
Vervolgens gebruiken we de volgende $\operatorname{CNOT}$ en $H$ poorten om ons bericht qubit te verplaatsen:

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a>Stap 3 & 4: Het meten en interpreteren van het resultaat
Tot slot @"microsoft.quantum.intrinsic.m" gebruiken we om de metingen uit te voeren en de `if` nodige poortbewerkingen uit te voeren om de gewenste status te krijgen, zoals aangegeven door verklaringen:

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a>Stap 5: Het qubit-register opnieuw opstarten

Aan het einde van elke Q # operatie moeten we de{0}qubits laten in de staat $\ket $. We kunnen @"microsoft.quantum.intrinsic.reset" gebruiken om alle qubits opnieuw te starten naar de nulstaat en dit zal onze operatie voltooien.

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


