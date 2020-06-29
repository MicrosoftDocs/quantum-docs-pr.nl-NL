---
title: 'Controle stroom in Q #'
description: Lussen, voor waarden enzovoort.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 0cf62a128170bd0c28ff77f00fc23414567b1ea4
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415300"
---
# <a name="control-flow-in-q"></a>Controle stroom in Q #

Binnen een bewerking of functie wordt elke instructie in volg orde uitgevoerd, vergelijkbaar met andere gebruikelijke, klassieke talen.
U kunt de controle stroom echter op drie verschillende manieren wijzigen:

* `if`instructies
* `for`lussen
* `repeat-until-success`lussen

De `if` `for` constructies en de controle stroom worden door gegeven in een vertrouwde zin voor de meeste klassieke programmeer talen. [`Repeat-until-success`](#repeat-until-success-loop)lussen worden verderop in dit artikel besproken.

Belang rijk: `for` lussen en `if` instructies kunnen worden gebruikt in bewerkingen waarvoor automatisch een [specialisatie](xref:microsoft.quantum.guide.operationsfunctions) wordt gegenereerd. In dat scenario keert de adjoint van een `for` lus de richting om en neemt de adjoint van elke iteratie toe.
Met deze actie wordt het principe ' schoenen en SOCKS ' gehanteerd: als u het maken van een SOCKS-en vervolgens schoenen wilt opheffen, moet u de toevoeging op schoenen ongedaan maken en vervolgens op SOCKS ongedaan maken. 

## <a name="if-else-if-else"></a>If, else-if, else

De `if` instructie ondersteunt voorwaardelijke uitvoering.
Het bestaat uit het sleutel woord `if` , een Boole-expressie tussen haakjes en een instructie blok (de _vervolgens_ blok kering).
U kunt eventueel elk wille keurig aantal else-if-componenten volgen, elk met het sleutel woord `elif` , een Boole-expressie tussen haakjes en een instructie blok (het _else-if-_ blok).
Ten slotte kan de instructie eventueel eindigen met een else-component, die bestaat uit het tref woord `else` gevolgd door een ander instructie blok (het _else_ -blok).

De `if` voor waarde wordt geëvalueerd en als deze *waar*is, wordt *then* de blok kering uitgevoerd.
Als de voor waarde *Onwaar*is, wordt de eerste else-if-voor waarde geëvalueerd; Als dat het geval is, wordt de *else-if-* blok kering uitgevoerd.
Als dat niet het geval is, wordt het tweede else-if-blok geëvalueerd en vervolgens de derde, enzovoort, totdat een component met de voor waarde True wordt aangetroffen of omdat er geen else-if-componenten zijn.
*Als de voor waarde origineel* en alle else-if-componenten resulteren in *Onwaar*, wordt het *else* -blok uitgevoerd, indien opgegeven.

Houd er rekening mee dat elk blok wordt uitgevoerd binnen een eigen bereik.
Bindingen die zijn gemaakt in een `if` , `elif` of `else` blok zijn niet zichtbaar nadat de blok kering is beëindigd.

Bijvoorbeeld:

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
of
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a>For-lus

De `for` instructie ondersteunt herhalingen over een bereik met gehele getallen of een matrix.
De instructie bestaat uit het tref woord `for` , gevolgd door een symbool of symbool tuple, het tref woord `in` en een expressie van het type `Range` of de matrix, alle tussen haakjes en een instructie blok.

Het instructie blok (de hoofd tekst van de lus) wordt herhaaldelijk uitgevoerd, met het gedefinieerde symbool (de variabele lus) dat is gekoppeld aan elke waarde in het bereik of de matrix.
Houd er rekening mee dat als de expressie Range resulteert in een leeg bereik of een lege matrix, de hoofd tekst helemaal niet wordt uitgevoerd.
De expressie is volledig geëvalueerd voordat de lus wordt ingevoerd en wordt niet gewijzigd terwijl de lus wordt uitgevoerd.

De lus-variabele is bij elke toegang aan de hoofd tekst van de lus gebonden en is aan het einde van de hoofd tekst losgekoppeld.
De lus-variabele is niet gebonden nadat de for-lus is voltooid.
De binding van de lus-variabele is onveranderbaar en volgt dezelfde regels als andere variabele bindingen. 

In deze voor beelden `qubits` is een REGI ster van qubits (bijvoorbeeld type `Qubit[]` ), 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

Houd er rekening mee dat aan het einde de reken kundige-Shift-Left-operator wordt gebruikt `<<<` . Zie [numerieke expressies](xref:microsoft.quantum.guide.expressions#numeric-expressions)voor meer informatie.

## <a name="repeat-until-success-loop"></a>Herhalen-tot-succes-lus

De Q #-taal staat de klassieke controle stroom afhankelijk van de resultaten van het meten van qubits.
Met deze mogelijkheid kunnen krachtige Probabilistic-gadgets worden geïmplementeerd waarmee de reken kosten voor het implementeren van unitaries kunnen worden verminderd.
Voor beelden hiervan zijn de patronen *herhalen tot en met succes* (RUS) in Q #.
Deze RUS-patronen zijn Probabilistic-Program ma's die een *verwachte* lage kosten in termen van elementaire poorten hebben. de gefactureerde kosten zijn afhankelijk van de daad werkelijke uitvoering en de interleaving van de meerdere mogelijke vertakkingen.

Q # ondersteunt de constructs om herhaalde tot geslaagde patronen (RUS) te vergemakkelijken

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

waar `expression` is een geldige expressie die resulteert in een waarde van het type `Bool` .
De hoofd tekst van de lus wordt uitgevoerd en vervolgens wordt de voor waarde geëvalueerd.
Als de voor waarde waar is, wordt de instructie voltooid. anders wordt de reparatie uitgevoerd en wordt de instructie opnieuw uitgevoerd, te beginnen met de hoofd tekst van de lus.

Alle drie delen van een RUS-lus (de hoofd tekst, de test en de reparatie) worden beschouwd als één bereik *voor elke herhaling*, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in zowel de test als de reparatie.
Het volt ooien van de uitvoering van de reparatie beëindigt echter het bereik voor de instructie, zodat symbool bindingen die zijn gemaakt in de hoofd tekst of de reparatie, niet beschikbaar zijn in volgende herhalingen.

Verder is de `fixup` instructie vaak handig, maar niet altijd nodig.
In gevallen dat het niet nodig is, de construct

```qsharp
repeat {
    // do stuff
}
until (expression);
```

is ook een geldig RUS-patroon.

Zie voor meer voor beelden en Details [herhalen](#repeat-until-success-examples) in dit artikel.

> [!TIP]   
> Vermijd het gebruik van herhalingen tot geslaagde lussen binnen functions. Gebruik *while* -lussen om de bijbehorende functionaliteit binnen functions te bieden. 

## <a name="while-loop"></a>Lus while

Herhalen-tot-succes-patronen hebben een zeer Quantum specifieke connotation. Ze worden veel gebruikt in bepaalde klassen van Quantum algoritmen, dus de speciale taal construct in Q #. Lussen die worden onderbroken op basis van een voor waarde en waarvan de uitvoerings lengte daarom onbekend is tijdens de compilatie, worden met name behandeld in een Quantum runtime. Hun gebruik in functions is echter ongevoelig omdat deze lussen alleen code bevatten die wordt uitgevoerd op conventionele hardware (niet-Quantum). 

Q # biedt daarom ondersteuning voor het gebruik van while-lussen in functions. Een `while` instructie bestaat uit het tref woord `while` , een Boole-expressie tussen haakjes en een instructie blok.
Het instructie blok (de hoofd tekst van de lus) wordt uitgevoerd zolang de voor waarde wordt geëvalueerd `true` .

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a>Instructie return

De instructie return beëindigt de uitvoering van een bewerking of functie en retourneert een waarde naar de aanroeper.
Het bestaat uit het tref woord `return` , gevolgd door een expressie van het juiste type en een punt komma als scheidings tekens.

Bijvoorbeeld:
```qsharp
return 1;
```
of
```qsharp
return (results, qubits);
```

* Een aanroepable die een lege tuple retourneert, `()` heeft geen instructie return nodig.
* Als u een vroege afsluiting van de bewerking of functie wilt opgeven, gebruikt u `return ();` .
Callables die een wille keurig ander type retour neren, moeten een laatste Return-instructie hebben.
* Er is geen maximum aantal retour instructies in een bewerking.
De compiler kan een waarschuwing verzenden als de instructies een instructie return in een blok volgen.

   
## <a name="fail-statement"></a>Fout instructie

De instructie Fail beëindigt het uitvoeren van een bewerking en retourneert een fout waarde naar de aanroeper.
Het bevat het tref woord `fail` , gevolgd door een teken reeks en een punt komma.
De instructie retourneert de teken reeks naar het klassieke stuur programma als het fout bericht.

Er is geen beperking voor het aantal mislukte instructies in een bewerking.
De compiler kan een waarschuwing verzenden als de instructies een mislukte instructie binnen een blok volgen.

Bijvoorbeeld:

```qsharp
fail $"Impossible state reached";
```
of, met behulp van [geïnterpoleerde teken reeksen](xref:microsoft.quantum.guide.expressions#interpolated-strings),
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a>Herhalen-tot-geslaagde voor beelden

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>RUS-patroon voor Qubit draaiing over een Irrational-as 

In een typische use-case implementeert de volgende Q #-bewerking een rotatie rond een Irrational-as van $ (I + 2i Z)/\sqrt {5} $ op de Bloch-bol. De implementatie maakt gebruik van een bekend RUS-patroon:

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a>RUS-lus met een onveranderlijke variabele in het bereik

In dit voor beeld ziet u het gebruik van een onveranderlijke variabele, `finished` die binnen het bereik van de volledige herhaling-until-reupdate-lus ligt en die wordt geïnitialiseerd vóór de lus en wordt bijgewerkt in de reparatie stap.

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a>RUS zonder`fixup`

In dit voor beeld ziet u een RUS-lus zonder de stap voor de reparatie. De code is een Probabilistic-circuit dat een belang rijke rotatie poort implementeert $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ met behulp van de- `H` en- `T` poorten.
De lus eindigt op gemiddeld $ \frac {8} {5} $ herhalingen.
Zie [*herhalen-tot-geslaagd: niet-deterministische ontleding van single-Qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick en Svore, 2014) voor meer informatie.

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a>RUS om een Quantum status voor te bereiden

Ten slotte is hier een voor beeld van een RUS-patroon voor het voorbereiden van een Quantum status $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, te beginnen bij de status $ \ket{+} $.

Belang rijke programmeer functies die in deze bewerking worden weer gegeven, zijn:

* Een complexere `fixup` deel van de lus, waarbij Quantum bewerkingen betrokken zijn. 
* Het gebruik van `AssertProb` instructies om de kans te bepalen dat de Quantum status op bepaalde opgegeven punten in het programma wordt gemeten.

[`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) Zie [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging)voor meer informatie over de-en-bewerkingen.

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

Voor meer informatie, zie voor [beeld van een eenheid testen dat is opgenomen in de standaard bibliotheek](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

## <a name="next-steps"></a>Volgende stappen

Meer informatie over [testen en fout opsporing](xref:microsoft.quantum.guide.testingdebugging) in Q #.
