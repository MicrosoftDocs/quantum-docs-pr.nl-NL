---
title: 'V # standaard bibliotheken-besturings element en stroom | Microsoft Docs'
description: 'Q # standaard bibliotheken-besturings element en stroom'
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 5e865dbb48029724b6f507ecb63b85d10d80c9a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185644"
---
# <a name="higher-order-control-flow"></a>Controle stroom met hogere volg orde #

Een van de primaire rollen van de standaard bibliotheek is om het eenvoudiger te maken om zeer belang rijke ideeën in te stellen als [Quantum Program ma's](https://en.wikipedia.org/wiki/Quantum_programming).
Daarom biedt Q # Canon diverse verschillende constructies voor datatransport besturing, die allemaal zijn geïmplementeerd met behulp van gedeeltelijke toepassing van functies en bewerkingen.
Als u direct naar een voor beeld gaat, moet u rekening houden met het geval waarin één ' CNOT ladder ' moet worden gemaakt in een REGI ster:

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

We kunnen dit patroon uitdrukken met behulp van iteratie en `for` lussen:

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

Uitgedrukt in termen van <xref:microsoft.quantum.canon.applytoeachca>-en array-manipulatie functies, zoals <xref:microsoft.quantum.arrays.zip>, is dit echter veel korter en eenvoudiger te lezen:

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

In de rest van deze sectie bieden we een aantal voor beelden van het gebruik van de verschillende Flow Control-bewerkingen en-functies die door de Canon worden geboden om de Quantum Program ma's te comprimeren.

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a>Bewerkingen en functies Toep assen op matrices en bereiken ##

Een van de primaire abstracties van de Canon is die van iteratie.
Denk bijvoorbeeld aan een unitary van het formulier $U \otimes U \otimes \cdots \otimes U $ voor een single-Qubit unitary $U $.
In Q # kunnen we <xref:microsoft.quantum.arrays.indexrange> gebruiken om dit als een `for` lus voor een REGI ster te vertegenwoordigen:

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation HAll(register : Qubit[]) : Unit 
is Adj + Ctl {

    for (qubit in register) {
        H(qubit);
    }
}
```

We kunnen deze nieuwe bewerking vervolgens gebruiken als `HAll(register)` om $H \otimes H \otimes \cdots \otimes H $ toe te passen.

Dit is een lastigere, maar met name in een groter algoritme.
Deze benadering is bovendien gespecialiseerd in de specifieke bewerking die we op elke qubit willen Toep assen.
We kunnen het feit gebruiken dat bewerkingen een eerste klasse zijn om dit algoritmen-concept explicieter te maken:

```qsharp
ApplyToEachCA(H, register);
```

Hier geeft het achtervoegsel `CA` aan dat het aanroepen van `ApplyToEach` zichzelf adjointable en kan worden bestuurd.
Als `U` `Adjoint` en `Controlled`ondersteunt, zijn de volgende regels dus gelijkwaardig:

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

Dit betekent met name dat aanroepen naar `ApplyToEachCA` kunnen worden weer gegeven in bewerkingen waarvoor een adjoint-specialisatie automatisch wordt gegenereerd.
<xref:microsoft.quantum.canon.applytoeachindex> is ook nuttig voor het weer geven van patronen van het formulier `U(0, targets[0]); U(1, targets[1]); ...`en biedt versies voor elke combi natie van functors die wordt ondersteund door de invoer.

> [!TIP]
> `ApplyToEach` is type para meters, zodat deze kan worden gebruikt met bewerkingen die andere invoer dan `Qubit`hebben.
> Stel bijvoorbeeld dat `codeBlocks` een matrix is met <xref:microsoft.quantum.errorcorrection.logicalregister> waarden die moeten worden hersteld.
> Vervolgens past `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` de code voor de fout correctie `code` en de herstel functie `recoveryFn` aan elk blok afzonderlijk toe.
> Dit geldt ook voor klassieke invoer: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` past een rotatie toe van $ \pi/$2 over $X $, gevolgd door een rotatie van $pi/$3 over $Y $.

De Q # Canon biedt ook ondersteuning voor klassieke inventarisatie patronen die bekend zijn met functionele programmering.
<xref:microsoft.quantum.arrays.fold> implementeert bijvoorbeeld het patroon $f (f (f (s\_{\Text{Initial}}, x\_0), x\_1), \dots) $ voor het verkleinen van een functie over een lijst.
Dit patroon kan worden gebruikt voor het implementeren van sommen, producten, minima, maxima en andere dergelijke functies:

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

Op dezelfde manier kunnen functies als <xref:microsoft.quantum.arrays.mapped> en <xref:microsoft.quantum.arrays.mappedbyindex> worden gebruikt om functionele Programmeer concepten in Q # te expressren.

## <a name="composing-operations-and-functions"></a>Bewerkingen en functies samen stellen ##

De constructies van de besturings stroom die door de Canon worden aangeboden, nemen activiteiten en functies als invoer, zodat het handig is om verschillende bewerkingen of functies in te stellen in één aanroepable.
Het patroon $UVU ^ {\dagger} $ is bijvoorbeeld zeer gebruikelijk in Quantum Program ma's, zodat de Canon de bewerking <xref:microsoft.quantum.canon.applywith> als een abstractie van dit patroon.
Deze abstractie biedt ook een efficiëntere naleving van circuits, omdat `Controlled` op de volg orde van `U(qubit); V(qubit); Adjoint U(qubit);` geen actie hoeft te ondernemen op elke `U`.
Als u dit wilt zien, laat u $c (U) $ de unitary voor `Controlled U([control], target)` en laat u $c (V) op dezelfde manier worden gedefinieerd.
Klik vervolgens voor een wille keurige status $ \ket{\psi} $, \begin{align} c (U) c (V) c (U) ^ \dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU ^ {\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes U) (c (V)) (\boldone \otimes U ^ \dagger) \ Ket{1} \otimes \ket{\psi}.
\end{align} op basis van de definitie van `Controlled`.
Anderzijds \begin{align} c (U) c (V) c (U) ^ \dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \otimes (UU ^ \dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c ( V)) (\boldone \otimes U ^ \dagger) \ket{0} \otimes \ket{\psi}.
\end{align} op basis van lineariteit kunnen we concluderen dat $U $ op deze manier kan worden gefactord voor alle invoer Staten.
Dat wil zeggen, $c (UVU ^ \dagger) = U c (V) U ^ \dagger $.
Omdat het beheren van bewerkingen erg kostbaar kan zijn, kunt u het aantal controle-functors dat moet worden toegepast, beperken met behulp van beheerde varianten zoals `WithC` en `WithCA`.

> [!NOTE]
> Een andere consequentie van het factor maken van $U $ is dat we niet eens weten hoe u de `Controlled` functor moet Toep assen op `U`.
> `ApplyWithCA` heeft daarom een zwakkere hand tekening dan verwacht:
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

Op dezelfde manier <xref:microsoft.quantum.canon.bind> bewerkingen genereren waarbij een reeks andere bewerkingen op zijn beurt wordt toegepast.
Het volgende is bijvoorbeeld gelijkwaardig:

```qsharp
H(qubit); X(qubit);
Bind([H, X], qubit);
```

Combi neren met iteratie patronen kan dit met name nuttig maken:

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bind([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a>Samen stelling met time-bestelling ###

We kunnen nog steeds verder gaan met de Datatransport besturing in termen van gedeeltelijke toepassing en klassieke functies, en kunnen zelfs redelijk geraffineerde Quantum concepten model leren in termen van klassiek stroom beheer.
Deze analogeie wordt nauw keurig gemaakt door de herkenning die unitary-Opera tors precies overeenkomen met de neven effecten van aanroepende activiteiten, zodat een degelijkheid van unitary-Opera tors in termen van andere unitary-Opera tors overeenkomt met het maken van een bepaalde aanroepende volg orde voor klassieke subroutines die instructies verzenden om te fungeren als bepaalde unitary-Opera tors.
In deze weer gave is `Bind` nauw keurig de weer gave van het matrix product, omdat `Bind([A, B])(target)` gelijk is aan `A(target); B(target);`, die op zijn beurt de aanroep volgorde is die overeenkomt met $BA $.

Een geavanceerd voor beeld is de [Trotter – Suzuki-uitbrei ding](https://arxiv.org/abs/math-ph/0506007v1).
Zoals beschreven in de sectie voor het weer geven van dynamische Generator van [gegevens structuren](xref:microsoft.quantum.libraries.data-structures), biedt de Trotter-Suzuki-uitbrei ding een bijzonder nuttige manier om matrix-exponentiëlen uit te geven.
Bijvoorbeeld: het Toep assen van de uitbrei ding met het laagste Volg nummer dat voor Opera tors $A $ en $B $ zodanig is dat $A = A ^ \dagger $ en $B = B ^ \dagger $, \begin{align} \tag{★} \label{EQ: Trotter-Suzuki-0} \exp (i [A + B] t) = \lim_{n\to\infty} \left (\exp (i A t/n) \exp (i B t ) \right) ^ n.
\end{align} Colloquially, dit geeft aan dat we ongeveer een staat kunnen ontwikkelen onder $A + B $ door zich op een andere wijze te ontwikkelen onder $A $ en $B $ alleen.
Als we de evolutie onder $A $ vertegenwoordigen door een bewerking `A : (Double, Qubit[]) => Unit` die $e ^ {i t A} $ toepast, wordt de representatie van de Trotter-Suzuki-uitbrei ding voor het opnieuw indelen van aanroepende reeksen duidelijk.
Gezien een bewerking `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` zo dat `A = U(0, _, _)` en `B = U(1, _, _)`, kunnen we een nieuwe bewerking definiëren waarmee de integraal van `U` op tijdstip $t $ wordt aangegeven door het genereren van reeksen van het formulier

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

Op dit moment kunnen we nu de oorzaak van de Trotter – Suzuki-uitbrei ding *zonder verwijzing naar Quantum monteurs*.
De uitbrei ding is in feite een zeer specifiek herhalings patroon dat wordt gemotiveerd door $ \eqref{EQ: Trotter-Suzuki-0} $.
Dit herhalings patroon wordt geïmplementeerd door <xref:microsoft.quantum.canon.decomposeintotimestepsca>:

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

De hand tekening van `DecomposeIntoTimeStepsCA` volgt een gemeen schappelijk patroon in Q #, waarbij verzamelingen waarvan een back-up kan worden gemaakt, worden weer gegeven door middel van een of meer gegevens die op de positie worden berekend door Tuples waarvan de eerste elementen zijn `Int` waarden die de lengte van de items aangeven.

## <a name="putting-it-together-controlling-operations"></a>Samen te brengen: bewerkingen beheren ##

Ten slotte bouwt de Canon op het `Controlled` functor door extra manieren te bieden voor het afwegen van Quantum bewerkingen.
Het is gebruikelijk, met name bij Quantum wiskundige bewerkingen, tot voor waarden voor de berekening van andere berekenings statussen dan $ \ket{0\cdots 0} $.
Met behulp van de besturings elementen en functies die hierboven worden geïntroduceerd, kunnen we meer algemene Quantum voorwaarden in één instructie hebben.
We gaan door naar de manier waarop <xref:microsoft.quantum.canon.controlledonbitstring> dit doet (type para meters van san's), waarna de onderdelen één voor één worden opgesplitst.
Het eerste wat u moet doen, is het definiëren van een bewerking die werkelijk het zware werk van het beheer op basis van een wille keurige reken status heeft.
Deze bewerking wordt echter niet rechtstreeks aangeroepen, maar daarom voegen we `_` toe aan het begin van de naam om aan te geven dat het een implementatie van een andere construct elders is.

```qsharp
operation _ControlledOnBitString(
        bits : Bool[],
        oracle: (Qubit[] => Unit is Adj + Ctl),
        controlRegister : Qubit[],
        targetRegister: Qubit[]) 
: Unit 
is Adj + Ctl {
```

Houd er rekening mee dat we een reeks bits gebruiken die wordt weer gegeven als een `Bool` matrix, waarmee we de voor waarden opgeven die we willen Toep assen op de bewerking `oracle` die we hebben opgegeven.
Aangezien deze bewerking rechtstreeks de toepassing doet, moeten we ook het besturings element en de doel registers volgen, die hier worden weer gegeven als `Qubit[]`.

Vervolgens zien we dat het bepalen van de berekening van de berekenings status $ \ket{\vec{s}} = \ket{s\_0 s\_1 \dots s\_{n-1}} $ voor een bits-teken reeks $ \vec{s} $ kan worden gerealiseerd door $ \ket{\vec{s}} $ te transformeren naar $ \ket{0\cdots 0} $.
Met name $ \ket{\vec{s}} = X ^ {s\_0} \otimes X ^ {s\_1} \otimes \cdots \otimes X ^ {s\_{n-1}} \ket{0\cdots 0} $.
Sinds $X ^ {\dagger} = X $, betekent dit dat $ \ket{0\dots 0} = X ^ {s\_0} \otimes X ^ {s\_1} \otimes \cdots \otimes X ^ {s\_{n-1}} \ket{\vec{s}} $.
Daarom kunnen we $P Toep assen = X ^ {s\_0} \otimes X ^ {s\_1} \otimes \cdots \otimes X ^ {s\_{n-1}} $, `Controlled oracle`Toep assen en terugconverteren naar $ \vec{s} $.
Deze constructie is nauw keurig `ApplyWith`, dus schrijft we de hoofd tekst van de nieuwe bewerking dienovereenkomstig:

```qsharp
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

Hier hebben we <xref:microsoft.quantum.canon.applypaulifrombitstring> gebruikt voor het Toep assen van $P $, die deels van toepassing zijn op het doel voor gebruik met `ApplyWith`.
Houd er echter rekening mee dat het *controle* register moet worden getransformeerd naar het gewenste formulier, dus we passen de binnenste bewerkings `(Controlled oracle)` op het *doel*gedeeltelijk toe.
Dit laat `ApplyWith` zich voordoen om het controle register met $P $ te sluiten, precies zoals gewenst.

Op dit moment kunnen we worden uitgevoerd, maar het lijkt erop dat onze nieuwe bewerking niet lijkt, zoals het Toep assen van de `Controlled` functor.
Daarom volt ooien we het nieuwe controle stroom concept door een functie te schrijven waarmee de Oracle wordt gecontroleerd en een nieuwe bewerking wordt geretourneerd.
Op deze manier ziet onze nieuwe functie er zeer veel uit als `Controlled`, waarbij u kunt zien dat we eenvoudig krachtige nieuwe besturings stroom constructies kunnen definiëren met Q # en de Canon samen:

```qsharp
function ControlledOnBitString(
        bits : Bool[],
        oracle: (Qubit[] => Unit is Adj + Ctl)) 
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
