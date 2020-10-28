---
title: Werken met qubits
description: Meer informatie over het werken met qubits in Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9a3d7e03016332a04ac9d1610428b6fcd546d1f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691584"
---
# <a name="working-with-qubits"></a>Werken met qubits

Qubits zijn het fundamenteel object van informatie in Quantum Computing. Zie [de Qubit](xref:microsoft.quantum.concepts.qubit)voor een algemene inleiding tot qubits [over Quantum Computing](xref:microsoft.quantum.overview.understanding), en voor meer informatie over de wiskundige weer gave ervan. 

In dit artikel wordt beschreven hoe u met qubits in een programma kunt werken Q# . 

> [!IMPORTANT]
>Geen van de instructies die in dit artikel worden besproken, is geldig in de hoofd tekst van een functie. Ze zijn alleen geldig in-bewerkingen.

## <a name="allocating-qubits"></a>Qubits toewijzen

Omdat fysieke qubits een kostbaar middel zijn in een quantum computer, moet u een deel van de taak van de compiler controleren om ervoor te zorgen dat ze zo efficiënt mogelijk worden gebruikt.
Als zodanig moet u aangeven dat u Q# qubits wilt *toewijzen* voor gebruik binnen een bepaald instructie blok.
U kunt qubits toewijzen als één Qubit, of als een matrix van qubits, ook wel een *REGI ster* genoemd. 

### <a name="clean-qubits"></a>Qubits opschonen

Gebruik de `using` instructie om nieuwe qubits toe te wijzen voor gebruik tijdens een instructie blok.

De instructie bestaat uit het tref woord `using` , gevolgd door een binding tussen haakjes `( )` en het instructie blok waarbinnen de qubits beschikbaar zijn.
De binding volgt hetzelfde patroon als `let` instructies: een enkel symbool of een tuple van symbolen, gevolgd door een gelijkteken `=` en een enkele waarde of een overeenkomende tuple van *initializers* .

Initialisatie functies zijn beschikbaar voor één Qubit, aangeduid als `Qubit()` , of een matrix van qubits, `Qubit[n]` , waarbij `n` een `Int` expressie is.
Bijvoorbeeld:

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

Alle qubits die op deze manier zijn toegewezen, worden met de {0} status $ \ket $ gestart. In het vorige voor beeld `auxiliary` is een enkelvoudige Qubit in de status $ \ket {0} $ en `register` bevindt zich in de vijf Qubit-status $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $.
Aan het einde van het `using` blok worden alle qubits die zijn toegewezen door dat blok onmiddellijk ongedaan gemaakt en kunnen niet verder worden gebruikt.

> [!WARNING]
> Doel machines kunnen ontoegewezen qubits opnieuw gebruiken en deze aanbieden aan andere `using` blokken voor toewijzing. Als zodanig verwacht de doel computer dat qubits zich in de $ \ket $-status bevindt onmiddellijk voordat de toewijzing wordt opgeheven {0} .
> Als dat mogelijk is, gebruikt u unitary-bewerkingen om de toegewezen qubits te retour neren aan $ \ket {0} $.
> Als dat het geval is, kunt u de @"microsoft.quantum.intrinsic.reset" bewerking, die de Qubit retourneert naar $ \ket $, gebruiken {0} door deze te meten en voorwaardelijk een bewerking uit te voeren op basis van het resultaat. Een dergelijke meting vernietigt alle entanglement met de resterende qubits en kan daardoor van invloed zijn op de berekening.


### <a name="borrowed-qubits"></a>Geleed qubits

Gebruik de `borrowing` instructie om qubits toe te wijzen voor tijdelijk gebruik, die geen specifieke status hoeven te hebben.

U kunt gelede qubits als Scratch ruimte gebruiken tijdens een berekening.
Deze qubits hebben doorgaans geen schone status, dat wil zeggen dat ze niet noodzakelijkerwijs zijn geïnitialiseerd in een bekende status, zoals $ \ket {0} $.
Deze worden vaak aangeduid als ' Dirty ' qubits omdat hun status onbekend is en zelfs kan worden Entangled met andere delen van het geheugen van de quantum computer.

De binding volgt hetzelfde patroon en regels als de- `using` instructie.
Bijvoorbeeld:
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
De geleende qubits bevinden zich in een onbekende status en het vervalt buiten het bereik aan het einde van het instructie blok.
De lenende door Voer om de qubits te verlaten in dezelfde staat waarin ze zich bevonden bij het lenen daarvan; dat wil zeggen dat de status aan het begin en het einde van het instructie blok hetzelfde moet zijn.
Omdat deze status niet noodzakelijkerwijs een klassieke status is, mogen in de meeste gevallen het lenen van scopes geen metingen bevatten. 

Bij het lenen van qubits probeert het systeem eerst de aanvraag in te vullen vanuit qubits die in gebruik zijn, maar niet worden geopend in de hoofd tekst van de `borrowing` instructie.
Als er onvoldoende qubits zijn, wijst deze nieuwe qubits toe om de aanvraag te volt ooien.

In het geval van bekende qubits zijn implementaties van meerdere beheerde CNOT-Gates die slechts enkele weinig qubits en implementatie van versnelers vereisen.
Zie voor een voor beeld van het gebruik in Q# het [lenen van qubits-voor beeld](#borrowing-qubits-example) in dit artikel of het papier [*confactoring met 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler en Svore 2017) voor een algoritme die gebruikmaakt van geleed qubits.

## <a name="intrinsic-operations"></a>Intrinsieke bewerkingen

Zodra de toewijzing is toegewezen, kunt u een Qubit door geven aan functies en bewerkingen.
In sommige zin is dit alles wat een Q# programma kan doen met een Qubit, omdat de acties die kunnen worden uitgevoerd, allemaal als bewerkingen worden gedefinieerd.

In dit artikel worden enkele nuttige Q# bewerkingen besproken die u kunt gebruiken om te communiceren met qubits.
Zie [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude)voor meer informatie over deze en andere. 

Eerst worden de Pauli-Opera tors (single-Qubit) $X $, $Y $ en $Z $ weer gegeven in Q# de intrinsieke bewerkingen [`X`](xref:Microsoft.Quantum.Intrinsic.X) , [`Y`](xref:Microsoft.Quantum.Intrinsic.Y) en [`Z`](xref:Microsoft.Quantum.Intrinsic.Z) die elk type hebben `(Qubit => Unit is Adj + Ctl)` .

Zoals beschreven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), beschouw $X $ en dus `X` als een bits-Flip-bewerking of niet-poort.
U kunt de `X` bewerking voor het voorbereiden van statussen van de vorm $ \ket{s_0 s_1 \dots s_n} $ voor een klassieke-bits teken reeks $s $:

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
        // Remember to reset the qubits before deallocation:
        ResetAll(register);
    }
}
```

> [!TIP]
> Later ziet u een compactere manier om deze bewerking te schrijven waarvoor geen hand matige controle stroom is vereist.

U kunt ook statussen voorbereiden zoals $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ en $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ met behulp van de Hadamard Transform $H $, die wordt vertegenwoordigd Q# door de intrinsieke bewerking [`H`](xref:Microsoft.Quantum.Intrinsic.H) (ook type (Qubit => eenheid is ADJ en CTL)):

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString in the earlier example.
    PrepareBitString(bitstring, register);
    // Next, use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the desired state.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a>Metingen

Metingen van afzonderlijke qubits kunnen worden uitgevoerd in verschillende slagen, die allemaal vertegenwoordigd worden door een Paulias op de [Bloch-bol](xref:microsoft.quantum.glossary#bloch-sphere).
De *reken kundige basis* verwijst naar de `PauliZ` basis en is de meest voorkomende basis voor de meting.

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a>Eén Qubit meten op `PauliZ` basis

Gebruik de [`M`](xref:Microsoft.Quantum.Intrinsic.M) bewerking, een ingebouwde, intrinsieke, niet-unitary bewerking, om één Qubit te meten op `PauliZ` basis en een klassieke waarde aan het resultaat toe te wijzen.
`M` heeft een gereserveerd retour type, `Result` dat alleen waarden kan overnemen `Zero` of `One` overeenkomt met de gemeten statussen $ \ket {0} $ of $ \ket {1} $-geeft aan dat het resultaat geen Quantum status meer is.

Een eenvoudig voor beeld is de volgende bewerking, die één Qubit toewijst in de $ \ket {0} $-status, vervolgens een Hadamard-bewerking toepast `H` op de waarde en het resultaat op basis daarvan meet `PauliZ` .

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // Apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, return the result of the measurement.
        return result;
    }
}
```

### <a name="measure-one-or-more-qubits-in-specific-bases"></a>Een of meer qubits meten in specifieke bases

U kunt de bewerking gebruiken om een matrix van een of meer qubits in een specifieke Base te meten [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) .

De invoer voor `Measure` is een matrix van `Pauli` typen (bijvoorbeeld `[PauliX, PauliZ, PauliZ]` ) en een matrix van qubits.

Een iets ingewik kelder voor beeld wordt gegeven door de volgende bewerking, waarmee de Boole-waarde wordt geretourneerd `true` als alle qubits in een REGI ster van `Qubit[]` het type in de status nul staan wanneer deze worden gemeten in een opgegeven Pauli, en die `false` anders retourneert.

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

Houd er rekening mee dat in dit voor beeld nog steeds alleen `Measure` een afzonderlijke qubits wordt uitgevoerd, maar de bewerking kan worden uitgebreid naar gezamenlijke metingen op meerdere qubits.

## <a name="borrowing-qubits-example"></a>Lenen van qubits-voor beeld

Er zijn voor beelden in de Canon die gebruikmaken van het `borrowing` tref woord, zoals de volgende functie `MultiControlledXBorrow` . Als u `controls` het besturings element qubits dat aan een bewerking moet worden toegevoegd `X` , wordt het aantal Dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) toegevoegd door deze implementatie `Length(controls)-2` .

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

In dit voor beeld is een uitgebreid gebruik van de `With` Combinator gebruikt, in het formulier dat van toepassing is op bewerkingen die adjoint ondersteunen, bijvoorbeeld `WithA` .
Dit is een goede programmeer stijl, omdat het besturings element wordt toegevoegd aan structuren waarbij `With` alleen de interne bewerking wordt door gegeven aan de besturings elementen.
Houd er ook rekening mee dat naast de `body` bewerking een implementatie van de `controlled` hoofd tekst van de bewerking expliciet is gegeven, in plaats van een instructie te gebruiken `controlled auto` .
De reden hiervoor is dat, vanwege de structuur van het circuit, het eenvoudig is om verdere besturings elementen toe te voegen, wat nuttig is ten opzichte van het toevoegen van controle aan elke poort in de `body` . 

Het is een goed proces om deze code te vergelijken met een andere Canon `MultiControlledXClean` -functie die hetzelfde doel heeft voor het implementeren van een `X` door een besturings systeem beheerde bewerking, maar die gebruikmaakt van verschillende schone qubits met behulp van het `using` mechanisme. 

## <a name="next-steps"></a>Volgende stappen

Meer informatie over [controle stroom](xref:microsoft.quantum.guide.controlflow) in Q# .