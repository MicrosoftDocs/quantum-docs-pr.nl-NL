---
title: 'Q #-instructies | Microsoft Docs'
description: 'Q #-instructies'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 9a6f5d53ec21090d0c13f4369e0270d264cd1e9b
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036488"
---
# <a name="statements-and-other-constructs"></a>Instructies en andere constructs

## <a name="comments"></a>Opmerkingen

Opmerkingen beginnen met twee slashes, `//`en door gaan tot het einde van de regel.
Een opmerking kan ergens in een Q #-bron bestand worden weer gegeven.

### <a name="documentation-comments"></a>Documentatie opmerkingen

Opmerkingen die beginnen met drie slashes, `///`, worden speciaal door de compiler behandeld wanneer ze direct vóór een naam ruimte, bewerking, specialisatie, functie of type definitie worden weer gegeven.
In dat geval wordt de inhoud ervan als documentatie voor het gedefinieerde aanroepende of door de gebruiker gedefinieerde type beschouwd, net als bij andere .NET-talen.

Binnen `///` opmerkingen wordt tekst die als onderdeel van de API-documentatie wordt weer gegeven, opgemaakt als een [prijs](https://daringfireball.net/projects/markdown/syntax)opgave, waarbij verschillende delen van de documentatie worden aangegeven door middel van speciaal benoemde kopteksten.
Als uitbrei ding van de prijs informatie kunnen kruis verwijzingen naar bewerkingen, functies en door de gebruiker gedefinieerde typen in Q # worden opgenomen met behulp van de `@"<ref target>"`, waarbij `<ref target>` wordt vervangen door de volledig gekwalificeerde naam van het code-object waarnaar wordt verwezen.
Een documentatie-engine kan eventueel ook extra kortings uitbreidingen ondersteunen.

Bijvoorbeeld:

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

De volgende namen worden herkend als documentatie opmerkings koppen.

- **Samen vatting**: een korte samen vatting van het gedrag van een functie of bewerking, of van het doel van een type. De eerste alinea van de samen vatting wordt gebruikt voor het aanwijzen van informatie. Dit moet tekst zonder opmaak zijn.
- **Beschrijving**: een beschrijving van het gedrag van een functie of bewerking, of van het doel van een type. De samen vatting en beschrijving worden samengevoegd om het gegenereerde documentatie bestand te vormen voor de functie, bewerking of het type.
  De beschrijving mag in-line-symbolen en-vergelijkingen in LaTeX-indeling bevatten.
- **Invoer**: een beschrijving van de invoer-tuple voor een bewerking of functie.
  Kan aanvullende subsecties van de korting bevatten die elk afzonderlijk element van de invoer-tuple aangeven.
- **Output**: een beschrijving van de tuple die wordt geretourneerd door een bewerking of functie.
- **Type parameters**: een lege sectie die één extra subsectie bevat voor elke algemene type parameter.
- **Voor beeld**: een kort voor beeld van het gebruik van de bewerking, functie of het type.
- **Opmerkingen**: diverse Prose die een aspect van de bewerking, functie of type beschrijven.
- **Zie ook**: een lijst met volledig gekwalificeerde namen die betrekking hebben op gerelateerde functies, bewerkingen of door de gebruiker gedefinieerde typen.
- **Verwijzingen**: een lijst met verwijzingen en bron vermeldingen voor het item dat wordt gedocumenteerd.

## <a name="namespaces"></a>Naamruimten

Elke Q #-bewerking,-functie en een door de gebruiker gedefinieerd type worden binnen een naam ruimte gedefinieerd.
Q # volgt dezelfde regels als voor naam als andere .NET-talen.
Q # biedt echter geen ondersteuning voor relatieve verwijzingen naar naam ruimten.
Dat wil zeggen, als de naam ruimte `a.b` is geopend, een verwijzing naar een bewerkings naam `c.d` niet wordt omgezet naar een bewerking met volledige naam `a.b.c.d`.

Binnen een naam ruimte blok kan de `open`-instructie worden gebruikt voor het importeren van alle typen en callables die zijn gedeclareerd in een bepaalde naam ruimte en deze te verwijzen naar de niet-gekwalificeerde naam. Een korte naam voor de naam ruimte kan eventueel worden gedefinieerd, zodat alle elementen van die naam ruimte kunnen (en moeten) worden gekwalificeerd door de gedefinieerde korte naam. De `open`-instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.

Er moet naar een type of aanroepbaar worden gedefinieerd in een andere naam ruimte die niet in de huidige naam ruimte wordt geopend, met de volledig gekwalificeerde naam.
Een bewerking met de naam `Op` in de naam ruimte `X.Y` moet bijvoorbeeld verwijzen naar de volledig gekwalificeerde naam `X.Y.Op`, tenzij de `X.Y` naam ruimte eerder in het huidige blok is geopend. Zoals hierboven vermeld, is het niet mogelijk om te verwijzen naar de bewerking als `Y.Op`, zelfs als de naam ruimte `X` is geopend.
Als er een korte naam `Z` voor `X.Y` is gedefinieerd in die naam ruimte en het bestand, moet `Op` worden aangeduid als `Z.Op`. 

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

Het is doorgaans beter om een naam ruimte op te maken met behulp van een `open`-instructie.
Het gebruik van een volledig gekwalificeerde naam is vereist als twee naam ruimten constructies met dezelfde naam definiëren. voor de huidige bron worden constructies van beide gebruikt.

## <a name="formatting"></a>Opmaak

De meeste Q #-instructies en de instructies eindigen met een punt komma, `;`.
Instructies en aangiften, zoals `for` en `operation` die eindigen op een instructie blok, hebben geen afsluitende punt komma.
Elke instructie bevat een beschrijving van de vraag of de afsluit punt komma is vereist.

Instructies, zoals expressies, declaraties en instructies, kunnen worden verdeeld over meerdere regels.
Meerdere instructies op één regel moeten worden vermeden.

## <a name="statement-blocks"></a>Instructie blokken

Q #-instructies worden gegroepeerd in instructie blokken.
Een instructie blok begint met een openings `{` en eindigt met een sluit `}`.

Een overzichts blok dat is inge sloten in een ander blok, wordt beschouwd als een subblok van het container blok; contains-en sub-blokken worden ook outer-en Inner-blokken genoemd.

## <a name="symbol-binding-and-assignment"></a>Symbool binding en toewijzing

Q # onderscheidt tussen onveranderlijke en onveranderlijke symbolen.
In het algemeen wordt het gebruik van onveranderbare symbolen aanbevolen omdat de compiler meer optimalisaties kan uitvoeren.

De linkerkant van de binding bestaat uit een symbool-tuple en de rechter kant van een expressie.

Aangezien alle typen Q # waardetypen zijn, is het qubits van een enigszins speciale rol, formeel een ' kopie ' gemaakt wanneer een waarde is gebonden aan een symbool of wanneer een symbool wordt losgekoppeld. Dat wil zeggen dat het gedrag van Q # hetzelfde is als wanneer er een kopie is gemaakt voor de toewijzing. Dit bevat met name ook matrices. Natuurlijk worden alleen de relevante onderdelen, indien nodig, feitelijk opnieuw gemaakt. 

### <a name="tuple-deconstruction"></a>Ontbouw van tuple

Als de rechter kant van de binding een tuple is, kan die tuple worden ontbouwd bij toewijzing.
Deze ontbouwingen kunnen geneste Tuples omvatten en een volledige of gedeeltelijke ontbouwing is geldig zolang de vorm van de tuple aan de rechter kant compatibel is met de vorm van de symbool-tuple.
Het ontbouwen van een tupel kan met name ook worden gebruikt wanneer de rechter kant van de `=` een tuple-expressie is.

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a>Onveranderbare symbolen

Onveranderbare symbolen zijn gekoppeld met behulp van de `let`-instructie.
Dit is ongeveer gelijk aan de declaratie van variabelen en initialisatie in talen zoals C#, behalve dat Q #-symbolen, zodra deze is gebonden, mag niet worden gewijzigd. `let` bindingen zijn onveranderbaar.

Een onveranderlijke binding bestaat uit het tref woord `let`, gevolgd door een symbool of symbool tuple, een gelijkteken `=`, een expressie om de symbolen te binden aan en een punt komma.
Het type van de afhankelijke symbolen wordt afgeleid op basis van de expressie aan de rechter kant.

### <a name="mutable-symbols"></a>Onveranderbare symbolen

Onveranderbare symbolen worden gedefinieerd en geïnitialiseerd met behulp van de `mutable`-instructie.
Symbolen die zijn gedeclareerd en gebonden als onderdeel van een `mutable` instructie, kunnen later in de code aan een andere waarde worden gekoppeld. 

Een onveranderlijke bindings instructie bestaat uit het tref woord `mutable`, gevolgd door een symbool of symbool tuple, een gelijkteken `=`, een expressie om de symbolen te binden aan en een punt komma.
Het type van de afhankelijke symbolen wordt afgeleid op basis van de expressie aan de rechter kant. Als een symbool later in de code wordt gebonden, wordt het type ervan niet gewijzigd en moet de gebonden waarde compatibel zijn met dat type.

### <a name="rebinding-of-mutable-symbols"></a>Rebinding van onveranderlijke symbolen

Een onveranderlijke variabele kan worden gekoppeld met behulp van een `set`-instructie.
Een herbinding bestaat uit het tref woord `set`, gevolgd door een symbool of symbool tuple, een gelijkteken `=`, een expressie waarmee de symbolen opnieuw worden verbonden en een punt komma.
De waarde moet compatibel zijn met het type (n) van de symbolen waaraan deze is gekoppeld.

#### <a name="apply-and-reassign-statement"></a>Instructie apply-and-assign

Een bepaald soort set-instructie waarnaar wordt verwezen als een instructie apply-and-reassign, biedt een handige manier om samen te voegen als de rechter kant bestaat uit de toepassing van een binaire operator en het resultaat moet worden gekoppeld aan het argument links voor de operator. Bijvoorbeeld:
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
verhoogt de waarde van de teller `counter` in elke iteratie van de `for`-lus. De bovenstaande code is gelijk aan 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
Soort gelijke instructies zijn beschikbaar voor alle binaire Opera tors waarin het type van de linkerkant van het expressie type overeenkomt. Dit biedt bijvoorbeeld een handige manier om waarden op te tellen:
```qsharp
mutable results = new Result[0];
for (qubit in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a>Instructie update-and-assign

Er bestaat een soort gelijke samen voeging voor expressies voor kopiëren en bijwerken aan de rechter kant. Daarnaast bestaan er instructies voor bijwerken en opnieuw toewijzen voor benoemde items in door de gebruiker gedefinieerde typen en voor matrix items.  

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

In het geval van matrices bevatten onze standaard bibliotheken de benodigde hulpprogram ma's voor veel algemene matrix initialisatie en bewerkings behoeften. zo voor komt u dat u matrix items in de eerste plaats hoeft bij te werken. Instructies update-en-reassign bieden een alternatief als dat nodig is:

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

> [!TIP]   
> Vermijd onnodig gebruik van instructies voor bijwerken en opnieuw toewijzen met behulp van de hulpprogram ma's in <xref:microsoft.quantum.arrays>.

De functie
```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];
    for (index in 0 .. length - 1) {
        set pauliArray w/= index <- 
            index == location ? pauli | PauliI;
    }    
    return pauliArray;
}
```
u kunt bijvoorbeeld eenvoudig eenvoudiger met de functie `ConstantArray` in `Microsoft.Quantum.Arrays`en een Kopieer-en-update-expressie retour neren:

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

### <a name="binding-scopes"></a>Bindings bereiken

Over het algemeen gaan symbool bindingen zich buiten het bereik en worden ze niet meer aan het einde van het instructie blok weer gegeven waarin ze zich bevinden.
Er zijn twee uitzonde ringen op deze regel:

- De binding van de lus-variabele van een `for`-lus bevindt zich in het bereik van de hoofd tekst van de lus for, maar niet na het einde van de lus.
- Alle drie delen van een `repeat`/`until` lus (de hoofd tekst, de test en de reparatie) worden behandeld als één bereik, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en in de reparatie.

Voor beide typen lussen wordt elke pass-through-lus uitgevoerd in een eigen bereik, waardoor bindingen van een eerdere Passes niet meer beschikbaar zijn in een latere fase.

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

## <a name="control-flow"></a>Controlestroom

### <a name="for-loop"></a>For-lus

De instructie `for` ondersteunt herhalingen over een geheel getal of een matrix.
De instructie bestaat uit het tref woord `for`, een open haakje `(`, gevolgd door een symbool of symbool tuple, het tref woord `in`, een expressie van het type `Range` of matrix, een haakje sluiten `)`en een instructie blok.

Het instructie blok (de hoofd tekst van de lus) wordt herhaaldelijk uitgevoerd, met de gedefinieerde symbolen (een of meer lussen) die zijn gekoppeld aan elke waarde in het bereik of de matrix.
Houd er rekening mee dat als de expressie Range resulteert in een leeg bereik of een lege matrix, de hoofd tekst helemaal niet wordt uitgevoerd.
De expressie is volledig geëvalueerd voordat de lus wordt ingevoerd en wordt niet gewijzigd terwijl de lus wordt uitgevoerd.

De binding van de gedeclareerde symbolen is onveranderbaar en volgt dezelfde regels als andere variabele bindingen. Het is met name mogelijk om de struct te ontleden, bijvoorbeeld om matrix items te bepalen voor een herhaling over een matrix bij toewijzing aan de lus-variabele (n).

Bijvoorbeeld:

```qsharp
// ...
for (qubit in qubits) { // qubits contains a Qubit[]
    H(qubit);
}

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {
    set results w/= index <- (index, M(qubits[index]));
}

mutable accumulated = 0;
for ((index, measured) in results) {
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

De lus-variabele is bij elke toegang aan de hoofd tekst van de lus gebonden en ontbond aan het einde van de hoofd tekst.
Met name de lus-variabele is niet gebonden nadat de for-lus is voltooid.

### <a name="repeat-until-success-loop"></a>Herhalen-tot-succes-lus

De instructie `repeat` ondersteunt het patroon ' herhalen tot geslaagd '.
Het bestaat uit het tref woord `repeat`, gevolgd door een instructie blok (de hoofd tekst van de _lus_ ), het tref woord `until`, een booleaanse expressie en een scheidings punt of het tref woord `fixup` gevolgd door een ander instructie blok (de _reparatie_).
De hoofd tekst van de lus, de voor waarde en de reparatie worden beschouwd als één bereik, dus de symbolen die in de hoofd tekst zijn gebonden, zijn beschikbaar in de voor waarde en correctie.

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

De hoofd tekst van de lus wordt uitgevoerd en vervolgens wordt de voor waarde geëvalueerd.
Als de voor waarde waar is, wordt de instructie voltooid. anders wordt de reparatie uitgevoerd en wordt de instructie opnieuw uitgevoerd, te beginnen met de hoofd tekst van de lus.
Houd er rekening mee dat het volt ooien van de uitvoering van de reparatie het bereik voor de instructie beëindigt, zodat symbool bindingen die zijn gemaakt tijdens de hoofd tekst of reparatie, niet beschikbaar zijn in volgende herhalingen.

De volgende code is bijvoorbeeld een Probabilistic-circuit waarmee een belang rijke rotatie poort wordt geïmplementeerd $V _3 = (\boldone + 2 i Z)/\sqrt{5}$ met behulp van de Hadamard en T-poorten.
De lus eindigt in $ \frac{8}{5}$ herhalingen op gemiddeld.
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

> [!TIP]   
> Vermijd het gebruik van herhalingen tot geslaagde lussen binnen functions. De bijbehorende functionaliteit wordt gegeven door-lussen in-functies. 

### <a name="while-loop"></a>Lus while

Herhalen-tot-succes-patronen hebben een zeer Quantum specifieke connotation. Ze worden veel gebruikt in bepaalde klassen van Quantum algoritmen, dus de speciale taal construct in Q #. Lussen die op basis van een voor waarde worden uitgevoerd en waarvan de uitvoerings lengte daarom onbekend is tijdens de compilatie, moeten worden behandeld met een speciale Care in een Quantum runtime. Het gebruik ervan in functions is niet probleemend, omdat deze alleen code bevatten die op conventionele hardware (niet-Quantum) wordt uitgevoerd. 

Q # ondersteunt daarom alleen het gebruik van while-lussen in-functies. Een `while`-instructie bestaat uit het sleutel woord `while`, een haakje openen `(`, een voor waarde (een booleaanse expressie), een haakje sluiten `)`en een instructie blok.
Het instructie blok (de hoofd tekst van de lus) wordt uitgevoerd zolang de voor waarde wordt geëvalueerd als `true`.

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a>Voorwaardelijke instructie

De instructie `if` ondersteunt voorwaardelijke uitvoering.
Het bestaat uit het tref woord `if`, een open haakje `(`, een Boole-expressie, een haakje sluiten `)`en een instructie blok (de _vervolgens_ blok kering).
Dit kan worden gevolgd door een wille keurig aantal else-if-componenten, die elk bestaan uit het tref woord `elif`, een open haakje `(`, een booleaanse expressie, een haakje sluiten `)`en een instructie blok (het _else-if-_ blok).
Ten slotte kan de instructie eventueel eindigen met een else-component, die bestaat uit het tref woord `else` gevolgd door een ander instructie blok (het _else_ -blok).
De voor waarde wordt geëvalueerd, en als deze waar is, wordt de blok kering uitgevoerd.
Als de voor waarde ONWAAR is, wordt de eerste else-if-voor waarde geëvalueerd; Als de waarde True is, wordt het blok Else-If uitgevoerd.
Anders wordt het tweede else-if-blok getest en vervolgens de derde, enzovoort, totdat een component met de voor waarde True wordt aangetroffen of omdat er geen else-if-componenten zijn.
Als de component origineel als voor waarde en alle else-if resulteert in ONWAAR, wordt het else-blok uitgevoerd als er een is opgegeven.

Houd er rekening mee dat welk blok wordt uitgevoerd in een eigen bereik.
Bindingen die zijn gemaakt binnen een then-, else-if-of else-blok zijn niet zichtbaar na het einde van de if-instructie.

Bijvoorbeeld:

```qsharp
if (result == One) {
    X(target);
} 
```

of

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a>Opvragen

De instructie return beëindigt de uitvoering van een bewerking of functie en retourneert een waarde naar de aanroeper.
Het bestaat uit het tref woord `return`, gevolgd door een expressie van het juiste type en een punt komma als scheidings tekens.

Een aanroepable die een lege tuple retourneert, `()`, heeft geen instructie return nodig.
Als een vroege afsluiting gewenst is, kan `return ()` in dit geval worden gebruikt.
Callables die een wille keurig ander type retour neren, moeten een laatste Return-instructie hebben.

Er is geen maximum aantal retour instructies in een bewerking.
De compiler kan een waarschuwing verzenden als de instructies een instructie return in een blok volgen.

Bijvoorbeeld:

```qsharp
return 1;
```

of

```qsharp
return ();
```

of

```qsharp
return (results, qubits);
```

### <a name="fail"></a>Mislukt

De instructie Fail beëindigt de uitvoering van een bewerking en retourneert een fout waarde naar de aanroeper.
Het bestaat uit het tref woord `fail`, gevolgd door een teken reeks en een punt komma.
De teken reeks wordt geretourneerd naar het klassieke stuur programma als het fout bericht.

Er is geen beperking voor het aantal mislukte instructies in een bewerking.
De compiler kan een waarschuwing verzenden als de instructies een mislukte instructie binnen een blok volgen.

Bijvoorbeeld:

```qsharp
fail $"Impossible state reached";
```

of

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a>Qubit-beheer

Houd er rekening mee dat geen van deze instructies zijn toegestaan in de hoofd tekst van een functie.
Ze zijn alleen geldig in-bewerkingen.

### <a name="clean-qubits"></a>Qubits opschonen

De instructie `using` wordt gebruikt om nieuwe qubits te verkrijgen voor gebruik tijdens een instructie blok.
De qubits worden gegarandeerd geïnitialiseerd voor de reken `Zero`-status.
De qubits moet zich in de reken kundige `Zero` status bekomen aan het einde van het instructie blok; simulatoren worden aangemoedigd om dit af te dwingen.

De instructie bestaat uit het tref woord `using`, gevolgd door een haakje openen `(`, een binding, een haakje sluiten `)`en het instructie blok waarbinnen de qubits beschikbaar is.
De binding volgt hetzelfde patroon als `let`-instructies: een enkel symbool of een tuple van symbolen, gevolgd door een gelijkteken `=`en een enkele waarde of een overeenkomende tuple van initializers.
Initialisatie functies zijn beschikbaar voor één Qubit, aangeduid als `Qubit()`, of een matrix van qubits, aangegeven door `Qubit[`, een `Int`-expressie en `]`.

Bijvoorbeeld:

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="borrowed-qubits"></a>Geleed qubits

De instructie `borrowing` wordt gebruikt om qubits te verkrijgen voor tijdelijk gebruik. De instructie bestaat uit het tref woord `borrowing`, gevolgd door een haakje openen `(`, een binding, een haakje sluiten `)`en het instructie blok waarbinnen de qubits beschikbaar is.
De binding volgt hetzelfde patroon en dezelfde regels als in een `using`-instructie.

Bijvoorbeeld:

```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

De geleende qubits bevinden zich in een onbekende status en het vervalt buiten het bereik aan het einde van het instructie blok.
De lenende door Voer om de qubits te verlaten in dezelfde staat waarin ze zich bevonden toen ze werden uitgeleend, d.w.z. hun status aan het begin en aan het einde van het blok van de verklaring, wordt naar verwachting hetzelfde.
Deze status is in het bijzonder niet noodzakelijkerwijs een klassieke staat, zoals in de meeste gevallen, het lenen van scopes mag geen metingen bevatten. 

Bekijk [*factoring met behulp van 2n + 2 qubits met modulaire vermenigvuldiging op basis van Toffoli*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler en Svore 2017) voor een voor beeld van een geleend Qubit-gebruik.

Wanneer qubits wordt uitgeleend, probeert het systeem eerst de aanvraag in te vullen vanuit qubits die in gebruik zijn, maar niet worden geopend tijdens de hoofd tekst van de `borrowing`-instructie.
Als er onvoldoende qubits zijn, wordt er nieuwe qubits toegewezen om de aanvraag te volt ooien.

## <a name="conjugations"></a>Conjugations

In tegens telling tot klassieke bits is het vrijgeven van Quantum geheugen iets resterend omdat het blind opnieuw instellen van qubits mogelijk ongewenste gevolgen heeft voor de resterende berekening als de qubits nog steeds Entangled zijn. Dit kan worden vermeden door de uitgevoerde berekeningen op de juiste manier uit te voeren voordat het geheugen wordt vrijgegeven. Een gemeen schappelijk patroon in de Quantum Computing is daarom het volgende: 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

: Nieuw: vanaf onze 0,9-versie bieden we ondersteuning voor een conjugation-instructie die de bovenstaande trans formatie implementeert. Met deze instructie kan de bewerkings `ApplyWith` op de volgende manier worden geïmplementeerd:

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
Een dergelijke conjugation-instructie is natuurlijk veel handiger als de buitenste en de binnenste trans formatie niet onmiddellijk beschikbaar zijn als bewerkingen, maar in plaats daarvan handiger zijn om te beschrijven door een blok bestaande uit verschillende instructies. 

De inverse trans formatie voor de instructies die in het binnen-blok zijn gedefinieerd, wordt automatisch gegenereerd door de compiler en uitgevoerd nadat de Apply-Block is voltooid. Omdat alle onveranderlijke variabelen die als onderdeel van de binnen-blok kering worden gebruikt, niet in het apply-blok kunnen worden gebonden, is de gegenereerde trans formatie gegarandeerd de adjoint van de berekening in het binnen-blok. 

## <a name="expression-evaluation-statements"></a>Expressie-evaluatie-instructies

Een aanroep expressie van het type `Unit` kan worden gebruikt als een instructie.
Dit wordt voornamelijk gebruikt bij het aanroepen van bewerkingen op qubits die `Unit` retour neren, omdat het doel van de instructie is om de impliciete Quantum status te wijzigen.
Voor expressie-evaluatie-instructies is een afsluit punt komma vereist.

Bijvoorbeeld:

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
