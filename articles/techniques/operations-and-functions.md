---
title: 'Q # bewerkingen en functies'
description: 'Meer informatie over de bewerkingen en functies van Q # en hoe deze worden toegepast in een Quantum programma.'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 43f0cf2da192a607e514d0c7de57a9bdd067faf7
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907661"
---
# <a name="q-operations-and-functions"></a>Q # bewerkingen en functies

Q # Program ma's bestaan uit een of meer *bewerkingen* die aan de hand van neven effecten de Quantum bewerkingen kunnen hebben op Quantum gegevens en een of meer *functies* die wijzigingen in klassieke gegevens toestaan. In tegens telling tot bewerkingen worden functies gebruikt om louter klassiek gedrag te beschrijven en geen effecten te hebben, behalve het berekenen van klassieke uitvoer waarden.

Elke bewerking die is gedefinieerd in Q # kan vervolgens een wille keurig aantal andere bewerkingen aanroepen, met inbegrip van de ingebouwde intrinsieke bewerkingen die zijn gedefinieerd door de taal. De specifieke manier waarop deze intrinsieke bewerkingen worden gedefinieerd, is afhankelijk van de doel computer. Bij compilatie wordt elke bewerking weer gegeven als een .NET-klassetype dat kan worden geleverd aan doel computers.

## <a name="defining-new-operations"></a>Nieuwe bewerkingen definiëren

Zoals hierboven beschreven, is de meest eenvoudige bouw steen van een Quantum programma dat is geschreven in Q # een *bewerking*, die kan worden aangeroepen vanuit klassieke .NET-toepassingen, bijvoorbeeld met behulp van een Simulator of door andere bewerkingen binnen Q #.
Elke bewerking neemt een invoer, produceert een uitvoer en geeft de implementatie aan voor een of meer bewerkings-specials.
Met de volgende bewerking wordt bijvoorbeeld alleen een standaard hoofdtekst voor de hoofd tekst gedefinieerd en wordt één Qubit als invoer gebruikt. vervolgens wordt de ingebouwde `X` bewerking voor die invoer aangeroepen:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

Met het tref woord `operation` wordt de bewerkings definitie gestart en gevolgd door de naam; `BitFlip`.
Vervolgens wordt het type van de invoer gedefinieerd als `Qubit`, samen met een naam `target` dat verwijst naar de invoer in de nieuwe bewerking.
Op dezelfde manier definieert de `Unit` dat de uitvoer van de bewerking leeg is.
Dit wordt op dezelfde manier gebruikt als C# `void` in en andere dwingende talen, en is gelijk F# aan `unit` in en andere functionele talen.

> [!NOTE]
> Hieronder wordt meer gedetailleerde informatie gegeven, maar elke bewerking in Q # heeft precies één invoer en retourneert precies één uitvoer.
> Meerdere invoer en uitvoer worden vervolgens weer gegeven met behulp van *Tuples*, waarbij meerdere waarden worden verzameld in één waarde.
> We zeggen dat Q # een ' tuple-in ' tuple-out ' is.
> Na dit concept moet `()` worden gelezen als de ' lege ' tuple, die het type `Unit`heeft.

Binnen de nieuwe bewerking kan de implementatie direct worden opgegeven in de declaratie als alleen de implementatie van de standaard hoofd code specialize expliciet moet worden opgegeven. Daarnaast is het mogelijk om de implementaties van, bijvoorbeeld een of meer `functor` bewerkingen, te definiëren, zoals hieronder wordt beschreven. In het bovenstaande voor beeld is de enige instructie om de ingebouwde <xref:microsoft.quantum.intrinsic.x>Q #-bewerking aan te roepen.

Bewerkingen kunnen ook interessante typen retour neren dan `Unit`.
Zo retourneert de <xref:microsoft.quantum.intrinsic.m>-bewerking een uitvoer van het type `Result`die een meting heeft uitgevoerd. U kunt de uitvoer van een bewerking naar een andere bewerking door geven of u kunt deze gebruiken met het sleutel woord `let` om een nieuwe variabele te definiëren.
<!-- Link to UID for superdense conceptual and example documentation. -->
Dit maakt het mogelijk om klassieke berekeningen aan te duiden die met Quantum bewerkingen op een laag niveau reageren, zoals bij de code ring van de functie:

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a>Functors, adjoint en beheerd
Als een bewerking een unitary-trans formatie implementeert, is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt. Met een adjoint specialisatie van een bewerking wordt aangegeven hoe deze in omgekeerde volg orde reageert, terwijl een beheerde specialisatie aangeeft hoe een bewerking reageert wanneer de status van een Quantum register wordt toegepast.
Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking: `is Adj + Ctl` in het volgende voor beeld. De bijbehorende implementatie voor elke impliciet gedeclareerde specialisatie wordt vervolgens door de compiler gegenereerd. 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> Veel bewerkingen in Q # vertegenwoordigen unitary Gates.
> Als $U $ de unitary-poort is die wordt weer gegeven door een bewerking `U`, vertegenwoordigt `Adjoint U` de unitary-poort $U ^ \dagger $.

Als de implementatie niet kan worden gegenereerd door de compiler, kan deze expliciet worden opgegeven. Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte instructie voor het genereren of een door de gebruiker gedefinieerde implementatie. De code in `PrepareEntangledPair` hierboven is bijvoorbeeld gelijk aan de onderstaande code met expliciete declaraties voor specialisatie: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
Het sleutel woord `auto` geeft aan dat de compiler moet bepalen hoe u de implementatie van de specialisatie wilt genereren.
Als de compiler de implementatie voor een bepaalde specialisatie niet automatisch kan genereren of als er een efficiëntere implementatie kan worden verleend, kan de implementatie ook hand matig worden gedefinieerd.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
In het bovenstaande voor beeld geeft `adjoint invert;` aan dat de adjoint-specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie te omkeren.

Er worden meer voor beelden weer gegeven in een [hogere controle stroom](xref:microsoft.quantum.concepts.control-flow).

Als u een specialisatie van een bewerking wilt aanroepen, gebruikt u de sleutel woorden `Adjoint` of `Controlled`.
Zo kan het bovenstaande voor beeld van de code ring van de bovenstaande sleutel sneller worden geschreven met behulp van de adjoint van `PrepareEntangledPair` om de Entangled-status terug te zetten in een unentangled paar qubits:

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

Er zijn een aantal belang rijke beperkingen waarmee u rekening moet houden bij het ontwerpen van bewerkingen voor gebruik met functors.
De meeste van de voor delen van een bewerking die de uitvoer waarde van een andere bewerking gebruikt, kan niet automatisch worden gegenereerd door de compiler, omdat het niet eenduidig is hoe u de instructies in een dergelijke bewerking opnieuw ordent om hetzelfde effect te verkrijgen.


## <a name="defining-new-functions"></a>Nieuwe functies definiëren

Q # biedt ook de mogelijkheid om *functies*te definiëren die verschillend zijn van bewerkingen in dat ze geen effect mogen hebben op het berekenen van een uitvoer waarde.
Met name functies kunnen geen bewerkingen aanroepen, reageren op qubits, voor beelden van wille keurige getallen of op andere wijze, afhankelijk van de invoer waarde voor een functie.
Als gevolg hiervan zijn Q #-functies *puur*, in dat ze altijd dezelfde invoer waarden toewijzen aan dezelfde uitvoer waarden.
Hiermee kan de Q #-compiler veilig de volg orde wijzigen van hoe en wanneer-functies worden aangeroepen bij het genereren van bewerkings-specials.

Het definiëren van een functie werkt op dezelfde manier als het definiëren van een bewerking, behalve dat er geen adjoint of beheerde Specials kunnen worden gedefinieerd voor een functie.
Bijvoorbeeld:

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
Wanneer het mogelijk is om dit te doen, is het handig om klassieke logica te schrijven in termen van functies in plaats van bewerkingen, zodat deze gemakkelijk vanuit bewerkingen kan worden gebruikt.
Als we `Square` als een bewerking hebben geschreven, zou de compiler niet kunnen garanderen dat het aanroepen van deze met dezelfde invoer consequent dezelfde uitvoer produceert.

Als u het verschil tussen functies en bewerkingen wilt onderstrepen, moet u rekening houden met het probleem van klassieke steek proeven voor een wille keurig getal in een Q #-bewerking:

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Elke keer dat `U` wordt aangeroepen, heeft het een andere actie op `target`.
Met name kan de compiler niet garanderen dat als we een `adjoint auto` specialisatie-declaratie aan `U`hebben toegevoegd, vervolgens `U(target); Adjoint U(target);` als identiteit fungeert (dat wil zeggen, als niet op).
Dit schendt de definitie van de adjoint die we hebben gezien in [vectoren en matrices](xref:microsoft.quantum.concepts.vectors), waardoor het automatisch genereren van een adjoint-specialisatie in een bewerking waarbij we de <xref:microsoft.quantum.math.randomreal> bewerking hebben aangeroepen, de door de compiler geboden garanties kan verstoren. <xref:microsoft.quantum.math.randomreal> is een bewerking waarvoor geen adjoint of gecontroleerde versie bestaat.

Daarentegen is het mogelijk om functie aanroepen zoals `Square` veilig te maken, omdat de compiler er zeker van kan zijn dat de invoer alleen moet worden behouden voor `Square` om de uitvoer stabiel te houden.
Door zo veel mogelijk klassieke logica in functies te isoleren, is het eenvoudig om die logica in andere functies en bewerkingen hetzelfde te hergebruiken.

## <a name="control-flow"></a>Controlestroom

Binnen een bewerking of functie wordt elke instructie in volg orde uitgevoerd, vergelijkbaar met de meest voorkomende verplichte klassieke talen.
Deze controle stroom kan echter op drie verschillende manieren worden gewijzigd:

- `if`-instructies
- `for` lussen
- `repeat`-`until` lussen

We stellen de bespreking van deze laatste uit tot we [herhalen tot succes (RUS)-](xref:microsoft.quantum.techniques.qubits#measurements) circuits.
De constructies van de controle stroom `if` en `for` gaan echter door in een vertrouwde zin voor de meeste klassieke programmeer talen.
Met name een `if`-instructie kan een voor waarde aannemen, gevolgd door een of meer `elif`-instructies, en kan eindigen met een `else`:

```qsharp
if (pauli == PauliX) {
    X(qubit);
} elif (pauli == PauliY) {
    Y(qubit);
} elif (pauli == PauliZ) {
    Z(qubit);
} else {
    fail "Cannot use PauliI here.";
}
```

Op dezelfde manier geven `for` lussen een herhaling aan voor een bereik met gehele getallen of over de elementen van een matrix:

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

Belang rijk: `for` lussen en `if`-instructies kunnen zelfs worden gebruikt in bewerkingen waarvoor specials automatisch worden gegenereerd. In dat geval wordt de adjoint van een `for` loop de richting omkeren en wordt de adjoint van elke iteratie gebruikt.
Dit is het principe ' schoenen en SOCKS ': als u het uitvoeren van een SOCKS ongedaan wilt maken en vervolgens schoenen wilt maken, moet u het op schoenen opzetten en vervolgens op SOCKS ongedaan maken.
Het werkt minder goed om uw SOCKS uit te proberen terwijl u nog steeds uw schoenen afdraagt!

## <a name="operations-and-functions-as-first-class-values"></a>Bewerkingen en functies als waarden voor de eerste klasse

Een van de essentiële technieken voor het opwegen van de controle stroom en klassieke logica met behulp van functies in plaats van bewerkingen is het gebruik van die bewerkingen en functies in Q # zijn de *eerste klasse*.
Dat wil zeggen dat ze elke waarde in de taal in hun eigen recht zijn.
Het volgende is bijvoorbeeld een zeer geldige Q #-code, als een beetje indirect:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

De waarde van de variabele `ourH` in het bovenstaande fragment is dan de bewerking <xref:microsoft.quantum.intrinsic.h>, zodat de waarde kan worden aangeroepen, zoals elke andere bewerking.
Hierdoor kunnen we bewerkingen schrijven die bewerkingen als onderdeel van hun invoer doen, waardoor de controle stroom concepten met een hogere volg orde kunnen worden uitgevoerd.
We kunnen bijvoorbeeld Voorst Ellen om een bewerking te ' Square ' door deze twee keer op dezelfde doel-Qubit toe te passen.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

In dit voor beeld wordt met de pijl `=>` die wordt weer gegeven in het type `(Qubit => Unit)` aangegeven dat het invoer veld `op` een bewerking is die als invoer wordt gebruikt voor het type `Qubit` en wordt er een lege tuple gegenereerd als uitvoer.
Daarnaast geven we de kenmerken van het betreffende bewerkings type op, die de informatie bevatten over welke functors worden ondersteund.
Een bewerking van het type `(Qubit => Unit)` ondersteunt noch de `Adjoint` noch de `Controlled` functor. Als we willen aangeven dat een bewerking van dit type moet worden ondersteund, bijvoorbeeld het `Adjoint` functor, moeten we het declareren als adjointable. Dit wordt gedaan met behulp van de aantekening `is Adj` voor het type. Op dezelfde manier geeft `(Qubit => Unit is Ctl)` aan dat een bewerking van dat type de `Controlled` functor ondersteunt. We zullen dit verder verkennen wanneer we [typen in Q # meer in](xref:microsoft.quantum.language.type-model) het algemeen bespreken.

We benadrukken nu dat we ook bewerkingen kunnen retour neren als onderdeel van uitvoer, zodat we een aantal van de klassieke voorwaardelijke logica kunnen isoleren als een klassieke functie waarmee een beschrijving van een Quantum programma wordt geretourneerd in de vorm van een bewerking.
Als eenvoudig voor beeld kunt u het voor beeld van teleportie overwegen, waarbij de partij die een twee-bits klassiek bericht ontvangt, het bericht moet gebruiken om hun Qubit te decoderen naar de juiste teleportal-status.
We kunnen dit schrijven in termen van een functie die deze twee klassieke bits accepteert en de juiste decodeer bewerking retourneert.

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

Deze nieuwe functie is inderdaad een functie. als we deze aanroepen met dezelfde waarden van `hereBit` en `thereBit`, krijgen we altijd dezelfde bewerking.
Het is dus mogelijk dat de decoder veilig kan worden uitgevoerd binnen bewerkingen zonder dat dit de reden hoeft te zijn van de manier waarop de decodeer logica communiceert met de definities van de verschillende bewerkings-specials.
Dat wil zeggen dat we de klassieke logica binnen een functie hebben geïsoleerd, zodat de compiler kan worden gevolgd met impunity, zolang de invoer wordt bewaard.

We kunnen ook functies behandelen als waarden voor de eerste klasse, aangezien we meer details zien wanneer we [bewerkingen en functie typen](#operations-and-functions-as-first-class-values)bespreken.

## <a name="partially-applying-operations-and-functions"></a>Bewerkingen en functies gedeeltelijk Toep assen

We kunnen aanzienlijk meer doen met functies die bewerkingen retour neren met behulp van *gedeeltelijke toepassing*, waarbij we een of meer delen van de invoer kunnen bieden aan een functie of bewerking zonder dat deze daad werkelijk wordt aangeroepen. Als u bijvoorbeeld het bovenstaande `ApplyTwice`-voor beeld aanroept, kunnen we aangeven dat we niet meteen willen opgeven dat Qubit de invoer bewerking moet worden toegepast:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

In dit geval bevat de lokale variabele `twiceOp` de gedeeltelijk toegepaste bewerking `ApplyTwice(op, _)`, waarbij delen van de invoer die nog niet zijn opgegeven, worden aangegeven door `_`.
Wanneer we `twiceOp` op de volgende regel daad werkelijk aanroepen, geven we de invoer door aan de gedeeltelijk toegepaste bewerking van alle resterende delen van de invoer voor de oorspronkelijke bewerking.
Het bovenstaande code fragment is dus in feite identiek aan het direct aanroepen van `ApplyTwice(op, target)`, opslaan voor dat we een nieuwe lokale variabele hebben geïntroduceerd waarmee we de oproep kunnen vertragen terwijl sommige onderdelen van de invoer worden vertraagd.

Omdat een bewerking die gedeeltelijk is toegepast, niet daad werkelijk wordt aangeroepen totdat de volledige invoer is opgegeven, kunnen we bewerkingen gedeeltelijk Toep assen, zelfs binnen functies.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

In principe zou de klassieke logica binnen `SquareOperation` veel meer betrokken kunnen zijn, maar nog steeds geïsoleerd van de rest van een bewerking door de garanties dat de compiler over functies kan bieden.
Deze benadering wordt gebruikt in de standaard bibliotheek van Q # voor het uitdrukken van de klassieke controle stroom op een manier die eenvoudig kan worden gebruikt binnen Quantum Program ma's.
