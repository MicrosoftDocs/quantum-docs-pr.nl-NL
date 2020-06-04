---
title: Werken met qubits
description: Beschrijving van opvulling
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: 0deb0729a88c49798f32a22a943b935d383c570b
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327540"
---
# <a name="working-with-qubits"></a>Werken met qubits

Als u nu een aantal verschillende onderdelen van de Q #-taal hebt gezien, laat u ons daar het dik van zien en ziet u hoe u qubits zelf kunt gebruiken.

Houd er rekening mee dat geen van deze instructies zijn toegestaan in de hoofd tekst van een functie.
Ze zijn alleen geldig in-bewerkingen.

## <a name="allocating-qubits"></a>Qubits toewijzen

### <a name="clean-qubits"></a>Qubits opschonen

De `using` instructie wordt gebruikt om nieuwe qubits *toe te wijzen* voor gebruik tijdens een instructie blok.

De instructie bestaat uit het tref woord `using` , gevolgd door een haakje openen, `(` een binding, een haakje sluiten `)` en het instructie blok waarbinnen de qubits beschikbaar is.
De binding volgt hetzelfde patroon als `let` instructies: een enkel symbool of een tuple van symbolen, gevolgd door een gelijkteken `=` en een enkele waarde of een overeenkomende tuple van *initializers*.

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

Alle qubits die op deze manier zijn toegewezen, worden in de $ \ket {0} $-status in het bovenstaande voor beeld gestart met `register` de status $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $.
Aan het einde van het `using` blok worden alle qubits die zijn toegewezen door dat blok onmiddellijk ongedaan gemaakt en kunnen niet verder worden gebruikt.

> [!WARNING]
> Doel computers verwachten dat qubits zich direct vóór de toewijzing van de $ \ket $ bevindt {0} , zodat ze opnieuw kunnen worden gebruikt en voor toewijzing aan andere blokken worden aangeboden `using` .
> Als dat mogelijk is, gebruikt u unitary-bewerkingen om de toegewezen qubits te retour neren aan $ \ket {0} $.
> Als dat het geval @"microsoft.quantum.intrinsic.reset" is, kan de bewerking worden gebruikt om in plaats daarvan een Qubit te meten en dit meet resultaat te gebruiken om ervoor te zorgen dat de gemeten Qubit wordt geretourneerd naar $ \ket {0} $. Een dergelijke meting vernietigt alle entanglement met de resterende qubits en kan daardoor van invloed zijn op de berekening.


### <a name="borrowed-qubits"></a>Geleed qubits

De `borrowing` instructie wordt gebruikt om qubits beschikbaar te maken voor tijdelijk gebruik, die geen specifieke status hebben.

Met het lenende mechanisme kunt u de toewijzing van qubits die als Scratch ruimte kan worden gebruikt tijdens een berekening.
Deze qubits hebben doorgaans geen schone status, dat wil zeggen dat ze niet noodzakelijkerwijs zijn geïnitialiseerd in een bekende status, zoals $ \ket {0} $.
Deze worden vaak aangeduid als ' Dirty ' qubits omdat hun status onbekend is en zelfs kan worden Entangled met andere delen van het geheugen van de quantum computer.

De binding volgt hetzelfde patroon en dezelfde regels als in een- `using` instructie.
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
De lenende door Voer om de qubits te verlaten in dezelfde staat waarin ze zich bevonden toen ze werden uitgeleend, d.w.z. hun status aan het begin en aan het einde van het blok van de verklaring, wordt naar verwachting hetzelfde.
Deze status is in het bijzonder niet noodzakelijkerwijs een klassieke staat, zoals in de meeste gevallen, het lenen van scopes mag geen metingen bevatten. 

Wanneer qubits wordt uitgeleend, probeert het systeem eerst de aanvraag in te vullen vanuit qubits die in gebruik zijn, maar niet worden geopend tijdens de hoofd tekst van de `borrowing` instructie.
Als er onvoldoende qubits zijn, wordt er nieuwe qubits toegewezen om de aanvraag te volt ooien.


In het geval van bekende qubits zijn implementaties van meerdere beheerde CNOT-Gates die slechts enkele weinig qubits en implementatie van versnelers vereisen.
Zie het [qubits-voor beeld](#borrowing-qubits-example) hieronder om een voor beeld te zien van het gebruik in Q # of de papier [*factor die gebruikmaakt van 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler en Svore 2017) voor een algoritme die gebruikmaakt van geleed qubits.


## <a name="intrinsic-operations"></a>Intrinsieke bewerkingen

Zodra de toewijzing is toegewezen, kan een Qubit worden door gegeven aan functies en bewerkingen.
In sommige zin is dit alles wat een Q #-programma kan doen met een Qubit, omdat de acties die kunnen worden uitgevoerd, allemaal als bewerkingen worden gedefinieerd.
Deze bewerkingen worden in meer detail weer gegeven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), maar we noemen nu enkele nuttige bewerkingen die kunnen worden gebruikt om te communiceren met qubits.

Eerst worden de Pauli-Opera tors met één Qubit $X $, $Y $ en $Z $ weer gegeven in Q # door de intrinsieke bewerkingen `X` , `Y` en `Z` , die elk type hebben `(Qubit => Unit is Adj + Ctl)` .
Zoals beschreven in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude), kunnen we $X $ en dus `X` als een bits-Flip-bewerking of niet-poort beschouwen.
`X`Met deze bewerking kunnen wij statussen van de vorm $ \ket{s_0 s_1 \dots s_n} $ voor een klassieke-bits teken reeks $s $ voorbereiden:

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

We kunnen ook staten voorbereiden zoals $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ en $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ door gebruik te maken van de Hadamard Transform $H $, die wordt weer gegeven in Q # door de intrinsieke bewerking `H : (Qubit => Unit is Adj + Ctl)` :

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

Door gebruik te maken van de `Measure` bewerking, een ingebouwde intrinsieke, niet-unitary bewerking, kunnen we klassieke informatie uit een object van het type ophalen `Qubit` en een klassieke waarde als resultaat toewijzen, die een gereserveerd type heeft `Result` . Dit geeft aan dat het resultaat geen Quantum status meer is.
De invoer naar `Measure` is een Pauli-as op de Bloch-bol, vertegenwoordigd door een waarde van het type `Pauli` (bijvoorbeeld ' instance ' `PauliX` ) en een waarde van het type `Qubit` .

Een eenvoudig voor beeld is de volgende bewerking, die één Qubit toewijst in de $ \ket {0} $-status, vervolgens een Hadamard-bewerking toepast `H` op de waarde en het resultaat op basis daarvan meet `PauliZ` .

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

## <a name="borrowing-qubits-example"></a>Lenen van qubits-voor beeld

In de Canon zijn voor beelden die gebruikmaken `borrowing` van het tref woord, bijvoorbeeld de functie die `MultiControlledXBorrow` hieronder is gedefinieerd.
Als `controls` u het besturings element qubits dat moet worden toegevoegd aan een `X` bewerking, wordt er een totaal van een `Length(controls)-2` groot aantal gewijzigde ancillas toegevoegd door deze implementatie.

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

Houd er rekening mee dat uitgebreid gebruik van de `With` Combinator----in het formulier dat van toepassing is op bewerkingen die adjoint ondersteunen, dat wil zeggen `WithA` ---is gemaakt in dit voor beeld.
Dit is een goede programmeer stijl, omdat het besturings element wordt toegevoegd aan structuren waarbij `With` alleen de interne bewerking wordt door gegeven aan de besturings elementen.
Daarnaast `body` is de implementatie van de hoofd tekst van de bewerking niet alleen van toepassing op `controlled` een instructie, maar u kunt er ook voor kiezen `controlled auto` .
De reden hiervoor is dat we van de structuur van het circuit weten hoe u eenvoudig extra besturings elementen kunt toevoegen die nuttig zijn ten opzichte van het toevoegen van controle aan elke afzonderlijke poort in de `body` . 

Het is een goed proces om deze code te vergelijken met een andere Canon `MultiControlledXClean` -functie die hetzelfde doel heeft voor het implementeren van een `X` door een besturings systeem beheerde bewerking, maar die gebruikmaakt van verschillende schone qubits met behulp van het `using` mechanisme. 

## <a name="next-steps"></a>Volgende stappen

Meer informatie over [controle stroom](xref:microsoft.quantum.guide.controlflow) in Q #.