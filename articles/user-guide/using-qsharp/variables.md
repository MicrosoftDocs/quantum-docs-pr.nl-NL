---
title: 'Variabelen in Q #'
description: Beschrijving van opvulling
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 407b4ff3570816eb7bdc323a5c5b77dac2d951af
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430897"
---
# <a name="variables-in-q"></a>Variabelen in Q #

Q # onderscheidt tussen onveranderlijke en onveranderlijke symbolen, of ' variabelen ', die gebonden zijn/toegewezen aan expressies.
In het algemeen wordt het gebruik van onveranderbare symbolen aanbevolen omdat de compiler meer optimalisaties kan uitvoeren.

De linkerkant van een binding bestaat uit een symbool-tuple en de rechter kant van een expressie.

## <a name="immutable-variables"></a>Onveranderbare variabelen

Een waarde van elk type in Q # kan worden toegewezen aan een variabele voor hergebruik in een bewerking of functie met behulp van het `let` sleutel woord.

Een onveranderlijke binding bestaat uit het tref woord `let` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen moeten worden verbonden en een punt komma als scheidings teken.

Bijvoorbeeld:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Hiermee wijst u een bepaalde matrix van Pauli-Opera tors toe aan de naam van de variabele (of het symbool), `measurementOperator` .

> [!NOTE]
> We hoeven het type van de nieuwe variabele niet expliciet op te geven, omdat de expressie aan de rechter kant van de `let` instructie ondubbelzinnig is en het type wordt afgeleid door de compiler. 

Variabelen die zijn gedefinieerd met kunnen `let` *onveranderbaar*zijn, wat betekent dat wanneer deze eenmaal is gedefinieerd, deze niet meer op een wille keurige manier kan worden gewijzigd.
Dit maakt een aantal gunstige optimalisaties mogelijk, waaronder de optimalisatie van de klassieke logica die wordt toegepast op variabelen voor het Toep assen `Adjoint` van de variant van een bewerking.

## <a name="mutable-variables"></a>Onveranderlijke variabelen

Als alternatief voor het maken van een variabele met wordt met `let` het `mutable` tref woord een onveranderlijke variabele gemaakt die opnieuw *kan* worden gebonden nadat deze in eerste instantie is gemaakt met behulp van het `set` sleutel woord.

Symbolen die zijn gedeclareerd en gebonden als onderdeel van een `mutable` instructie, kunnen later in de code opnieuw worden gebonden aan een andere waarde. Als een symbool later in de code wordt gebonden, wordt het type ervan niet gewijzigd en moet de zojuist gekoppelde waarde compatibel zijn met dat type.

### <a name="rebinding-of-mutable-symbols"></a>Rebinding van onveranderlijke symbolen

Een onveranderlijke variabele kan worden gekoppeld met behulp van een- `set` instructie.
Een herbinding bestaat uit het tref woord `set` , gevolgd door een symbool of symbool tuple, een gelijkteken `=` , een expressie waarmee de symbolen opnieuw worden verbonden en een punt komma.

Hier bieden we enkele mogelijke voor beelden van de technieken voor het opnieuw binden van een instructie

### <a name="apply-and-reassign-statements"></a>Instructies Toep assen en opnieuw toewijzen

Een bepaalde soort `set` instructie wordt verwezen naar een instructie *Apply-and-reassign, en* biedt een handige manier om samen te voegen als de rechter kant bestaat uit de toepassing van een binaire operator en het resultaat moet worden gekoppeld aan het argument links voor de operator. Bijvoorbeeld:
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
verhoogt de waarde van het prestatie meter item `counter` in elke herhaling van de `for` lus. De bovenstaande code is gelijk aan 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

Soort gelijke instructies zijn beschikbaar voor alle binaire Opera tors waarin het type van de linkerkant van het expressie type overeenkomt. Dit biedt bijvoorbeeld een handige manier om waarden te verzamelen.

Supposing `qubits` is bijvoorbeeld een regsiter van qubits:
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a>Instructies bijwerken en opnieuw toewijzen

Er bestaat een soort gelijke samen voeging voor [expressies voor kopiëren en bijwerken](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) aan de rechter kant.
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

In het geval van matrices [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) biedt de standaard bibliotheken de benodigde hulpprogram ma's voor veel algemene matrix initialisatie-en bewerkings behoeften. zo voor komt u dat u matrix items in de eerste plaats hoeft bij te werken. 

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

Met de bibliotheek hulpprogramma's voor matrices die zijn opgegeven in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , kunnen we bijvoorbeeld eenvoudig een functie definiëren die een matrix van PAULIS retourneert waarbij de Pauli bij index `i` de opgegeven waarde krijgt en alle andere vermeldingen de identiteit zijn.

Hier vindt u twee definities van een dergelijke functie, met het tweede gebruik van de hulpprogram ma's voor onze afstoting.

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

In plaats van elke index in de matrix te herhalen en het beleid voorwaardelijk in te stellen op `PauliI` of `Pauli` , kunnen we in plaats daarvan een `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) matrix van maken `PauliI` en vervolgens gewoon een kopie-en-update-expressie retour neren waarin we de specifc-waarde bij index hebben gewijzigd `location` :

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a>Ontbouw van tuple

Naast het toewijzen van één variabele, de `let` `mutable` sleutel woorden---of in feite een andere bindings constructie, zoals `set` (hieronder beschreven)---kunt u ook de inhoud van een [tuple-type](xref:microsoft.quantum.guide.types#tuple-types)uitpakken.
Een toewijzing van dit formulier wordt genoemd om de elementen van die tuple te *ontconstrueren* .

Als de rechter kant van de binding een tuple is, kan die tuple worden ontbouwd bij toewijzing.
Deze ontbouwingen kunnen geneste Tuples omvatten en een volledige of gedeeltelijke ontbouwing is geldig zolang de vorm van de tuple aan de rechter kant compatibel is met de vorm van de symbool-tuple.

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
- Alle drie delen van een `repeat` / `until` lus (de hoofd tekst, de test en de reparatie) worden behandeld als één bereik, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en in de reparatie.

Voor beide typen lussen wordt elke pass-through-lus uitgevoerd in een eigen bereik, waardoor bindingen van een eerdere Passes niet meer beschikbaar zijn in een latere fase.
Meer informatie over deze lussen vindt u in de [controle stroom](xref:microsoft.quantum.guide.controlflow).

Symbool bindingen van de buitenste blokken worden overgenomen door binnenste blokken.
Een symbool mag slechts eenmaal per blok zijn gebonden; het is niet toegestaan om een symbool te definiëren met dezelfde naam als een ander symbool dat zich binnen het bereik bevindt (geen "schaduw").
De volgende reeksen zijn juridisch:

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

## <a name="whats-next"></a>Hoe nu verder?
Meer informatie over het [werken met qubits](xref:microsoft.quantum.guide.qubits) in Q #.