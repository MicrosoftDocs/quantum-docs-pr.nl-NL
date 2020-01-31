---
title: 'Alles op elkaar afzetten-Q # technieken | Microsoft Docs'
description: 'Alles op elkaar afzetten: Q # technieken'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3605826da159757d4b321dbf4ec6acd7f4e6be05
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820161"
---
# <a name="putting-it-all-together-teleportation"></a>Alles combi neren: teleportie #
We gaan terug naar het voor beeld van het telepoorts circuit dat is gedefinieerd in [Quantum circuits](xref:microsoft.quantum.concepts.circuits). We gaan deze gebruiken om de concepten te illustreren die we tot nu toe hebben geleerd. Hieronder vindt u een uitleg van Quantum teleportie voor degenen die niet bekend zijn met de theorie, gevolgd door een overzicht van de code-implementatie in Q #. 

## <a name="quantum-teleportation-theory"></a>Quantum-teleportie: theorie
Quantum teleportal is een techniek voor het verzenden van een onbekende Quantum status (waarnaar we verwijzen als '__bericht__') van een Qubit op de ene locatie naar een Qubit op een andere locatie (hier verwijzen we naar deze qubits als '__hier__' en '__daar__'). We kunnen ons __bericht__ als een vector weer geven met behulp van de Dirac-notatie: 

$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $

De status van het __bericht__ Qubit is niet bekend bij ons, omdat we niet weten wat de waarden van $ \alpha $ en $ \beta $ zijn.

### <a name="step-1-create-an-entangled-state"></a>Stap 1: een Entangled-status maken
Als u het __bericht__ wilt verzenden, moet u __hier__ de Qubit Entangled met __de Qubit.__ Dit wordt bereikt door een Hadamard-poort toe te passen, gevolgd door een CNOT-poort. Laten we eens kijken naar de wiskundige formules achter deze poort bewerkingen.

We beginnen __hier__ met de __qubits en in__ de $ \ket{0}$-status. Na het entangling van deze qubits hebben ze de volgende status:

$ $ \ket{\phi ^ +} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) $ $

### <a name="step-2-send-the-message"></a>Stap 2: het bericht verzenden
Als u het __bericht__ wilt verzenden, past u eerst een CNOT-Gate toe met het __bericht__ Qubit en __hier__ Qubit als invoer (het __bericht__ Qubit het besturings element en de Qubit als __doel Qubit,__ in dit geval). Deze invoer status kan worden geschreven:

$ $ \ket{\psi}\ket{\phi ^ +} = (\alpha\ket{0} + \beta\ket{1}) (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11})) $ $

Dit kan worden uitgebreid naar:

$ $ \ket{\psi}\ket{\phi ^ +} = \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $

Als herinnering wordt de CNOT-Gate gespiegeld met de doel-Qubit wanneer het besturings element Qubit 1 is. Een invoer van $ \ket{000}$ resulteert bijvoorbeeld in geen wijziging als de eerste Qubit (het besturings element) 0 is. Doe echter een geval waarbij de eerste Qubit 1 is, bijvoorbeeld een invoer van $ \ket{100}$. In dit geval is de uitvoer $ \ket{110}$, omdat de tweede Qubit (het doel) wordt gespiegeld door de CNOT-Gate.

We beschouwen nu onze uitvoer zodra de CNOT-Gate op de bovenstaande invoer heeft gehandeld. Het resultaat is:

$ $ \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{110} + \frac{\beta}{\sqrt{2}} \ket{101} $ $

De volgende stap voor het verzenden van het __bericht__ is het Toep assen van een Hadamard-poort op het __bericht__ Qubit (dat is de eerste Qubit van elke term). 

Als herinnering geeft de Hadamard-Gate het volgende:

Invoer | Uitvoer
---------------------------| ---------------------------------------------------------------
$ \ket{0}$  | $ \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) $
$ \ket{1}$  | $ \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}) $

Als we de Hadamard-poort Toep assen op de eerste Qubit van elke periode van onze uitvoer hierboven, krijgen we het volgende resultaat:

$ $ \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{00} + \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{11} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{01} $ $

Houd er rekening mee dat elke term $2 \frac{1}{\sqrt{2}} $-factoren heeft. We kunnen deze uitvermenigvuldigen met het volgende resultaat:

$ $ \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{11} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{10} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{01} $ $

De $ \frac{1}{2}$-factor is gebruikelijk voor elke term zodat we deze nu buiten de vier Kante haken kunnen halen:

$ $ \frac{1}{2}\big [\alpha (\ket{0} + \ket{1}) \ket{00} + \alpha (\ket{0} + \ket{1}) \ket{11} + \beta (\ket{0}-\ket{1}) \ket{10} + \beta (\ket{0}-\ket{1}) \ket{01}\big] $ $

De vier Kante haken kunnen vervolgens worden vermenigvuldigd voor elke term met het volgende:

$ $ \frac{1}{2}\big [\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010}-\beta\ket{110} + \beta\ket{001}-\beta\ket{101}\big] $ $

### <a name="step-3-measure-the-result"></a>Stap 3: het resultaat meten

Als gevolg van __hier__ en __er__ wordt Entangled, dan is de meting __hier__ van invloed op de __status.__ Als we de eerste en tweede Qubit (__bericht__ en __hier__) meten, kunnen we weten wat staat __er__ in, vanwege deze eigenschap van Entanglement. 

* Als we het resultaat 00 meten en ontvangen, wordt de superpositie samengevouwen, waardoor alleen de termen consistent zijn met dit resultaat. Dat is $ \alpha\ket{000} + \beta\ket{001}$. Dit kan worden herstructureeerd tot $ \ket{00}(\alpha\ket{0} + \beta\ket{1}) $. Als we de eerste en tweede Qubit meten als 00, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{0} + \beta\ket{1}) $ bevindt.
* Als we het resultaat 01 meten en ophalen, wordt de superpositie samengevouwen, waardoor alleen de termen met dit resultaat overeenkomen. Dat is $ \alpha\ket{011} + \beta\ket{010}$. Dit kan worden herstructureeerd tot $ \ket{01}(\alpha\ket{1} + \beta\ket{0}) $. Als we de eerste en tweede Qubit meten als 01, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{1} + \beta\ket{0}) $ bevindt.
* Als we het resultaat 10 meten en ophalen, wordt de superpositie samengevouwen, waardoor alleen de termen consistent zijn met dit resultaat. Dat is $ \alpha\ket{100}-\beta\ket{101}$. Dit kan worden herstructureeerd naar $ \ket{10}(\alpha\ket{0}-\beta\ket{1}) $. Als we de eerste en tweede Qubit naar 10 meten, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{0}-\beta\ket{1}) $ bevindt.
* Als we het resultaat 11 meten en ophalen, wordt de superpositie samengevouwen, waardoor alleen de termen met dit resultaat overeenkomen. Dat is $ \alpha\ket{111}-\beta\ket{110}$. Dit kan worden herstructureeerd naar $ \ket{11}(\alpha\ket{1}-\beta\ket{0}) $. Als we de eerste en tweede Qubit meten in 11, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{1}-\beta\ket{0}) $ bevindt.

### <a name="step-4-interpret-the-result"></a>Stap 4: het resultaat interpreteren

Het oorspronkelijke __bericht__ dat we willen verzenden, is als herinnering:

$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $

We moeten de __er__ Qubit in deze staat ophalen, zodat de ontvangen status het certificaat is dat is bedoeld. 

* Als we hebben gemeten en een resultaat van 00 hebben ontvangen, bevindt de derde Qubit __er__in de status $ (\alpha\ket{0} + \beta\ket{1}) $. Aangezien dit het bedoelde __bericht__is, is er geen wijziging vereist.
* Als we het resultaat van 01 hebben gemeten en ontvangen, bevindt de derde Qubit, __daar__, zich in de status $ (\alpha\ket{1} + \beta\ket{0}) $. Dit verschilt van het beoogde __bericht__, maar het Toep assen van een not-Gate geeft ons de gewenste status $ (\alpha\ket{0} + \beta\ket{1}) $.
* Als we een resultaat van 10 hebben gemeten en ontvangen, bevindt de derde Qubit, __daar__, zich in de status $ (\alpha\ket{0}-\beta\ket{1}) $. Dit verschilt van het beoogde __bericht__, maar het Toep assen van een Z-Gate geeft ons de gewenste status $ (\alpha\ket{0} + \beta\ket{1}) $.
* Als we hebben gemeten en een resultaat van 11 hebben ontvangen, bevindt de derde Qubit __er__in de status $ (\alpha\ket{1}-\beta\ket{0}) $. Dit verschilt van het beoogde __bericht__, maar het Toep assen van een niet-poort, gevolgd door een Z-Gate, geeft ons de gewenste status $ (\alpha\ket{0} + \beta\ket{1}) $.

Als we meten en de eerste Qubit is 1, wordt een Z-poort toegepast. Als we meten en de tweede Qubit is 1, wordt er geen Gate toegepast.

### <a name="summary"></a>Samenvatting
Hieronder ziet u een Quantum-circuit (Text-Book) waarmee de teleportie wordt geïmplementeerd. Van links naar rechts kunt u het volgende zien:
- Stap 1: Entangling __hier__ en __er__ door een HADAMARD-Gate en CNOT-poort toe te passen.
- Stap 2: het __bericht__ verzenden met behulp van een CNOT-Gate en een Hadamard-poort.
- Stap 3: het maken van een meting van het eerste en tweede qubits, __bericht__ en __hier__.
- Stap 4: een NOT-Gate of een Z-poort Toep assen, afhankelijk van het resultaat van de meting in stap 3.

![' Teleporten (msg: Qubit, daar: Qubit): eenheid '](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a>Quantum-teleportie: code

We hebben ons circuit voor Quantum-teleportie:

![' Teleporten (msg: Qubit, daar: Qubit): eenheid '](~/media/teleportation.svg)

We kunnen de stappen in dit Quantum circuit nu omzetten in Q #.

### <a name="step-0-definition"></a>Stap 0: definitie
Wanneer we teleportie uitvoeren, moeten we het __bericht__ weten dat we willen verzenden en waar we het willen verzenden. Daarom beginnen we met het definiëren van een nieuwe teleport-bewerking die twee qubits als argumenten, `msg` en `there`heeft.

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

We moeten ook een Qubit toewijzen `here` die wordt gerealiseerd met een `using` blok:

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a>Stap 1: een Entangled-status maken
Vervolgens kunnen we het Entangled-paar maken tussen `here` en `there` met behulp van de @"microsoft.quantum.intrinsic.h"-en @"microsoft.quantum.intrinsic.cnot"-bewerkingen:

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a>Stap 2: het bericht verzenden
Vervolgens gebruiken we de volgende $ \operatorname{CNOT} $ en $H $ Gates om onze bericht Qubit te verplaatsen:

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a>Stap 3 & 4: het resultaat meten en interpreteren
Ten slotte gebruiken we @"microsoft.quantum.intrinsic.m" om de metingen uit te voeren en de benodigde poort bewerkingen uit te voeren om de gewenste status te krijgen, zoals aangegeven door `if`-instructies:

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

Hiermee voltooit u de definitie van onze teleportie-operator, waardoor we de toewijzing van `here`ongedaan kunnen maken, de hoofd tekst te beëindigen en de bewerking te beëindigen.

```qsharp
    }
}
```
