---
title: Variabelen in Q#
description: Meer informatie over het werken met verschillende variabelen in Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
no-loc:
- Q#
- $$v
ms.openlocfilehash: bb87f36d3c9b7df195f64e85151e833d494ea945
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835873"
---
# <a name="variables-in-no-locq"></a>Variabelen in Q#

Q# maakt onderscheid tussen onveranderlijke en onveranderlijke symbolen, of *variabelen*, die gebonden zijn/toegewezen aan expressies.
In het algemeen wordt het gebruik van onveranderbare symbolen aanbevolen omdat de compiler meer optimalisaties kan uitvoeren.

De linkerkant van een binding bestaat uit een symbool-tuple en de rechter kant van een expressie.

## <a name="immutable-variables"></a>Onveranderbare variabelen

U kunt een waarde van elk type in Q# een variabele toewijzen voor hergebruik binnen een bewerking of functie met behulp van het `let` sleutel woord. 

Een onveranderlijke binding bestaat uit het tref woord `let` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen moeten worden verbonden en een punt komma als scheidings teken.

Bijvoorbeeld:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Hiermee wijst u een bepaalde matrix van Pauli-Opera tors toe aan de naam van de variabele (of het symbool), `measurementOperator` .

> [!NOTE]
> In het vorige voor beeld is het niet nodig expliciet het type van de nieuwe variabele op te geven, omdat de expressie aan de rechter kant van de `let` instructie ondubbelzinnig is en de compiler het juiste type afleidt. 

Variabelen die zijn gedefinieerd met kunnen `let` *onveranderbaar*zijn, wat inhoudt dat u deze niet meer kunt wijzigen wanneer u deze hebt gedefinieerd.
Dit maakt een aantal gunstige optimalisaties mogelijk, waaronder de optimalisatie van de klassieke logica die op variabelen wordt toegepast voor het Toep assen `Adjoint` van de variant van een bewerking.

## <a name="mutable-variables"></a>Onveranderlijke variabelen

Als alternatief voor het maken van een variabele met `let` , `mutable` maakt het sleutel woord een onveranderlijke variabele die na de eerste keer dat deze is gemaakt met behulp van het sleutel woord, *kan* worden ontbonden `set` .

U kunt symbolen die zijn gedeclareerd en gebonden als onderdeel van een `mutable` instructie opnieuw koppelen aan een andere waarde verderop in de code. Als een symbool later in de code wordt gebonden, wordt het type ervan niet gewijzigd en moet de zojuist gekoppelde waarde compatibel zijn met dat type.

### <a name="rebinding-of-mutable-symbols"></a>Rebinding van onveranderlijke symbolen

U kunt een onveranderlijke variabele opnieuw binden met behulp van een `set` instructie.
Een herbinding bestaat uit het tref woord `set` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen opnieuw worden verbonden en een punt komma.

Hier volgen enkele voor beelden van methoden voor het opnieuw binden van een instructie.

#### <a name="apply-and-reassign-statements"></a>Instructies Toep assen en opnieuw toewijzen

Een bepaald type `set` instructie, de instructie *Apply-and-reassign* , biedt een handige manier om samen te voegen als de rechter kant de toepassing van een binaire operator is en het resultaat moet worden gekoppeld aan het argument links voor de operator. Bijvoorbeeld:

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
verhoogt de waarde van het prestatie meter item `counter` in elke herhaling van de `for` lus. De vorige code is gelijk aan 

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

Soort gelijke instructies zijn beschikbaar voor alle binaire Opera tors waarin het type van de linkerkant overeenkomt met het expressie type. Deze instructies bieden een handige manier om waarden samen te voegen.

Supposing `qubits` is bijvoorbeeld een REGI ster van qubits:
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

#### <a name="update-and-reassign-statements"></a>Instructies bijwerken en opnieuw toewijzen

Er bestaat een soort gelijke samen voeging voor de [expressies voor kopiëren en bijwerken](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) aan de rechter kant.
Daarnaast bestaan er instructies voor *bijwerken en opnieuw toewijzen* voor *benoemde items* in door de gebruiker gedefinieerde typen en voor *matrix items*.  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

In het geval van matrices [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) beschikt u in de Q# Standard-bibliotheek over de benodigde hulpprogram ma's voor veel algemene matrix initialisatie en bewerkings behoeften. zo voor komt u dat u de matrix items in de eerste plaats hoeft bij te werken. 

Instructies update-en-reassign bieden een alternatief als dat nodig is:

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

Met de bibliotheek hulpprogramma's voor matrices die zijn opgegeven in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , kunt u bijvoorbeeld eenvoudig een functie definiëren die een matrix van `Pauli` typen retourneert waarbij het element op index `i` een gegeven `Pauli` waarde krijgt en alle andere vermeldingen de identiteit () zijn `PauliI` .

Hier vindt u twee definities van een dergelijke functie, met het tweede gebruik van de hulpprogram ma's voor onze afstoting.

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli if index==location and PauliI if not
    }    
    return pauliArray;
}
```

In plaats van elke index in de matrix te herhalen en deze voorwaardelijk in te stellen op `PauliI` of de opgegeven `pauli` , kunt u in plaats daarvan `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) een matrix van `PauliI` typen maken en vervolgens gewoon een kopie-en-update-expressie retour neren waarin u de specifieke waarde op index hebt gewijzigd `location` :

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a>Ontbouw van tuple

Naast het toewijzen van één variabele kunt u de `let` `mutable` sleutel woorden en of een andere bindings constructie gebruiken, zoals `set` -om de inhoud van een [tuple-type](xref:microsoft.quantum.guide.types#tuple-types)uit te pakken.
Een toewijzing van dit formulier wordt genoemd om de elementen van die tuple te *ontconstrueren* .

Als de rechter kant van de binding een tuple is, kunt u die tupel tijdens toewijzing ontkoppelen.
Deze ontbouwingen kunnen gebruikmaken van geneste Tuples en een volledige of gedeeltelijke ontbouwing is geldig zolang de vorm van de tuple aan de rechter kant compatibel is met de vorm van de symbool-tuple.

Bijvoorbeeld:

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a>Bindings bereiken

Over het algemeen gaan symbool bindingen zich buiten het bereik en worden ze niet meer aan het einde van het instructie blok weer gegeven waarin ze zich bevinden.
Er zijn twee uitzonde ringen op deze regel:

- De binding van de lus-variabele van een `for` lus bevindt zich in het bereik voor de hoofd tekst van de lus for, maar niet na het einde van de lus.
- Alle drie delen van een `repeat` / `until` lus (de hoofd tekst, de test en de reparatie) fungeren als één bereik, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en de reparatie.

Voor beide typen lussen wordt elke pass-through-lus uitgevoerd in een eigen bereik, waardoor bindingen vanuit een eerdere fase niet meer beschikbaar zijn in een latere fase.
Zie [controle stroom](xref:microsoft.quantum.guide.controlflow)voor meer informatie over deze lussen.

Binnenste blokken nemen symbool bindingen over van de buitenste blokken.
U kunt slechts eenmaal per blok een symbool binden; het is niet toegestaan om een symbool te definiëren met dezelfde naam als een ander symbool dat zich binnen het bereik bevindt (geen "schaduw").
De volgende reeksen zijn geldig:

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

en

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

Maar dit is niet toegestaan:

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

Zo zou:

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a>Volgende stappen

Meer informatie over het [werken met qubits](xref:microsoft.quantum.guide.qubits) in Q# .