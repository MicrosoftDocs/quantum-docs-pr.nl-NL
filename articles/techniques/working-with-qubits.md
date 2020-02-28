---
title: Werken met qubits
description: Meer informatie over het toewijzen van qubits, het gebruiken van bewerkingen en functies en het meten van de resultaten.
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 1aa2432996dda61d099e3b5bb4db78379ce43d97
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907644"
---
# <a name="working-with-qubits"></a>Werken met qubits

Als u nu een aantal verschillende onderdelen van de Q #-taal hebt gezien, laat u ons daar het dik van zien en ziet u hoe u qubits zelf kunt gebruiken.

## <a name="allocating-qubits"></a>Qubits toewijzen

Voor het verkrijgen van een Qubit die we in Q # kunnen gebruiken, wijzen we qubits binnen een `using`-blok *toe* :

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

Alle qubits die op deze manier zijn toegewezen, worden gestart in de $ \ket{0}$-status; in het bovenstaande voor beeld is `register` dus de status $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.
Aan het einde van het `using` blok worden alle qubits die door dat blok zijn toegewezen, onmiddellijk ongedaan gemaakt en kunnen niet verder worden gebruikt.

> [!WARNING]
> Doel computers verwachten dat qubits zich in $ \ket{0}$ staat onmiddellijk voordat de toewijzing ongedaan wordt gemaakt, zodat ze opnieuw kunnen worden gebruikt en worden aangeboden aan andere `using` blokken voor toewijzing.
> Als dat mogelijk is, gebruikt u unitary-bewerkingen om de toegewezen qubits te retour neren aan $ \ket{0}$.
> Als dat het geval is, kan de @"microsoft.quantum.intrinsic.reset" bewerking worden gebruikt om in plaats daarvan een Qubit te meten en dit meet resultaat te gebruiken om ervoor te zorgen dat de gemeten Qubit wordt geretourneerd naar $ \ket{0}$. Een dergelijke meting vernietigt alle entanglement met de resterende qubits en kan daardoor van invloed zijn op de berekening.

## <a name="intrinsic-operations"></a>Intrinsieke bewerkingen

Zodra de toewijzing is toegewezen, kan een Qubit worden door gegeven aan functies en bewerkingen.
In sommige zin is dit alles wat een Q #-programma kan doen met een Qubit, omdat de acties die kunnen worden uitgevoerd, allemaal als bewerkingen worden gedefinieerd.
Deze bewerkingen worden in meer detail weer gegeven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), maar we noemen nu enkele nuttige bewerkingen die kunnen worden gebruikt om te communiceren met qubits.

Eerst worden de Pauli-Opera tors met één Qubit $X $, $Y $ en $Z $ weer gegeven in Q # door de intrinsieke bewerkingen `X`, `Y`en `Z`, die elk het type `(Qubit => Unit is Adj + Ctl)`hebben.
Zoals beschreven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), kunnen we $X $ en dus `X` als een bits-Flip-bewerking of niet-poort.
Met de `X` bewerking kunnen wij statussen van de vorm $ \ket{s_0 s_1 \dots s_n} $ voor een bepaalde klassieke-bits teken reeks $s $ voorbereiden:

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> Later worden er meer compacte manieren weer gegeven voor het schrijven van deze bewerking waarvoor hand matige Datatransport besturing niet is vereist.

We kunnen ook staten voorbereiden zoals $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ en $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ door gebruik te maken van de Hadamard Transform $H $, die wordt weer gegeven in Q # door de intrinsieke bewerking `H : (Qubit => Unit is Adj + Ctl)`:

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a>Metingen

Met behulp van de `Measure` bewerking, een ingebouwde, intrinsieke, niet-unitary bewerking kunnen we klassieke informatie uit een object van het type `Qubit` ophalen en een klassieke waarde als resultaat toewijzen, die een gereserveerd type heeft `Result`, waarmee wordt aangegeven dat het resultaat geen Quantum status meer is.
De invoer voor `Measure` is een Pauli-as op de Bloch-bol, vertegenwoordigd door een waarde van het type `Pauli` (voor instantie `PauliX`) en een waarde van het type `Qubit`.

Een eenvoudig voor beeld is de volgende bewerking, die één Qubit toewijst in de $ \ket{0}$-status, waarna een Hadamard-bewerking `H` wordt toegepast en het resultaat wordt gemeten in de `PauliZ` basis.

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

Een iets ingewik kelder voor beeld wordt gegeven door de volgende bewerking, waarmee de Booleaanse waarde wordt geretourneerd `true` als alle qubits in een REGI ster van het type `Qubit[]` de status nul hebben wanneer ze worden gemeten in een opgegeven Pauli, en die `false` anders retourneert.

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

De Q #-taal staat de klassieke controle stroom afhankelijk van de resultaten van het meten van qubits.
Met deze mogelijkheid kunnen krachtige Probabilistic-gadgets worden geïmplementeerd waarmee de reken kosten voor het implementeren van unitaries kunnen worden verminderd.
Een voor beeld is het eenvoudig om te implementeren, dat wil zeggen, *herhalen-tot-succes-* patronen (RUS) in Q #.
Deze RUS-patronen zijn Probabilistic-Program ma's die een *verwachte* lage kosten in termen van elementaire poorten hebben, maar waarvoor de werkelijke kosten afhankelijk zijn van een feitelijke uitvoering en een daad werkelijke interleaving van verschillende mogelijke vertakkingen.

Q # ondersteunt de construct om herhaalde tot geslaagd (RUS) patronen te vergemakkelijken.

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

waar `statementBlock1` en `statementBlock2` geen of meer Q #-instructies zijn, en `expression` een geldige expressie die resulteert in een waarde van het type `Bool`.
In een typische use-case implementeert de volgende Q #-bewerking een rotatie rond een Irrational-as van $ (I + 2i Z)/\sqrt{5}$ op de Bloch-bol. Dit wordt bereikt door gebruik te maken van een bekend RUS-patroon:

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

In dit voor beeld ziet u het gebruik van een onveranderlijke variabele `finished` die binnen het bereik van de volledige herhalings-tot-reparatie-lus ligt en die wordt geïnitialiseerd vóór de lus en wordt bijgewerkt in de reparatie stap.

Tot slot wordt een voor beeld van een RUS-patroon weer gegeven om een Quantum status te bereiden $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, te beginnen bij de status $ \ket{+} $.
Zie ook het [voor beeld van een eenheid testen dat is opgenomen in de standaard bibliotheek](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
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

Opvallende programmatische functies die in deze bewerking worden weer gegeven, zijn een complexere `fixup` deel van de lus, waarbij Quantum bewerkingen worden betrokken, en het gebruik van `AssertProb`-instructies om de kans te bepalen dat de Quantum status op bepaalde opgegeven punten in het programma wordt gemeten.
Zie ook [testen en fout opsporing](xref:microsoft.quantum.techniques.testing-and-debugging) voor meer informatie over de [`Assert`](xref:microsoft.quantum.intrinsic.assert) en [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) bewerkingen.
