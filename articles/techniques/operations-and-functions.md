---
title: 'Q # technieken-bewerkingen en functies | Microsoft Docs'
description: 'Q # technieken-bewerkingen en functies'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 06da09dc9c6e0ba0331db6bc0cd3d2ddeb287113
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183451"
---
# <a name="q-operations-and-functions"></a><span data-ttu-id="734c5-103">Q # bewerkingen en functies</span><span class="sxs-lookup"><span data-stu-id="734c5-103">Q# Operations and Functions</span></span>

<span data-ttu-id="734c5-104">Q # Program ma's bestaan uit een of meer *bewerkingen* die aan de hand van neven effecten de Quantum bewerkingen kunnen hebben op Quantum gegevens en een of meer *functies* die wijzigingen in klassieke gegevens toestaan.</span><span class="sxs-lookup"><span data-stu-id="734c5-104">Q# programs consist of one or more *operations* that describe side effects quantum operations can have on quantum data, and one or more *functions* that allow modifications to classical data.</span></span> <span data-ttu-id="734c5-105">In tegens telling tot bewerkingen worden functies gebruikt om louter klassiek gedrag te beschrijven en geen effecten te hebben, behalve het berekenen van klassieke uitvoer waarden.</span><span class="sxs-lookup"><span data-stu-id="734c5-105">In contrast to operations, functions are used to describe purely classical behavior and do not have any effects besides computing classical output values.</span></span>

<span data-ttu-id="734c5-106">Elke bewerking die is gedefinieerd in Q # kan vervolgens een wille keurig aantal andere bewerkingen aanroepen, met inbegrip van de ingebouwde intrinsieke bewerkingen die zijn gedefinieerd door de taal.</span><span class="sxs-lookup"><span data-stu-id="734c5-106">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="734c5-107">De specifieke manier waarop deze intrinsieke bewerkingen worden gedefinieerd, is afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="734c5-107">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span> <span data-ttu-id="734c5-108">Bij compilatie wordt elke bewerking weer gegeven als een .NET-klassetype dat kan worden geleverd aan doel computers.</span><span class="sxs-lookup"><span data-stu-id="734c5-108">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="734c5-109">Nieuwe bewerkingen definiëren</span><span class="sxs-lookup"><span data-stu-id="734c5-109">Defining New Operations</span></span>

<span data-ttu-id="734c5-110">Zoals hierboven beschreven, is de meest eenvoudige bouw steen van een Quantum programma dat is geschreven in Q # een *bewerking*, die kan worden aangeroepen vanuit klassieke .NET-toepassingen, bijvoorbeeld met behulp van een Simulator of door andere bewerkingen binnen Q #.</span><span class="sxs-lookup"><span data-stu-id="734c5-110">As described above, the most basic building block of a quantum program written in Q# is an *operation*, which can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="734c5-111">Elke bewerking neemt een invoer, produceert een uitvoer en geeft de implementatie aan voor een of meer bewerkings-specials.</span><span class="sxs-lookup"><span data-stu-id="734c5-111">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="734c5-112">Met de volgende bewerking wordt bijvoorbeeld alleen een standaard hoofdtekst voor de hoofd tekst gedefinieerd en wordt één Qubit als invoer gebruikt. vervolgens wordt de ingebouwde `X` bewerking voor die invoer aangeroepen:</span><span class="sxs-lookup"><span data-stu-id="734c5-112">For instance, the following operation defines only a default body specialization and takes a single qubit as its input, then calls the built-in `X` operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="734c5-113">Met het tref woord `operation` wordt de bewerkings definitie gestart en gevolgd door de naam; `BitFlip`.</span><span class="sxs-lookup"><span data-stu-id="734c5-113">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="734c5-114">Vervolgens wordt het type van de invoer gedefinieerd als `Qubit`, samen met een naam `target` dat verwijst naar de invoer in de nieuwe bewerking.</span><span class="sxs-lookup"><span data-stu-id="734c5-114">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="734c5-115">Op dezelfde manier definieert de `Unit` dat de uitvoer van de bewerking leeg is.</span><span class="sxs-lookup"><span data-stu-id="734c5-115">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="734c5-116">Dit wordt op dezelfde manier gebruikt als C# `void` in en andere dwingende talen, en is gelijk F# aan `unit` in en andere functionele talen.</span><span class="sxs-lookup"><span data-stu-id="734c5-116">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

> [!NOTE]
> <span data-ttu-id="734c5-117">Hieronder wordt meer gedetailleerde informatie gegeven, maar elke bewerking in Q # heeft precies één invoer en retourneert precies één uitvoer.</span><span class="sxs-lookup"><span data-stu-id="734c5-117">We will explore this in more detail below, but each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="734c5-118">Meerdere invoer en uitvoer worden vervolgens weer gegeven met behulp van *Tuples*, waarbij meerdere waarden worden verzameld in één waarde.</span><span class="sxs-lookup"><span data-stu-id="734c5-118">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="734c5-119">We zeggen dat Q # een ' tuple-in ' tuple-out ' is.</span><span class="sxs-lookup"><span data-stu-id="734c5-119">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="734c5-120">Na dit concept moet `()` worden gelezen als de ' lege ' tuple, die het type `Unit`heeft.</span><span class="sxs-lookup"><span data-stu-id="734c5-120">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

<span data-ttu-id="734c5-121">Binnen de nieuwe bewerking kan de implementatie direct worden opgegeven in de declaratie als alleen de implementatie van de standaard hoofd code specialize expliciet moet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="734c5-121">Within the new operation, the implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to be specified explicitly.</span></span> <span data-ttu-id="734c5-122">Daarnaast is het mogelijk om de implementaties van, bijvoorbeeld een of meer `functor` bewerkingen, te definiëren, zoals hieronder wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="734c5-122">Additionally, it is possible to define the implementations of, for example, one or more `functor` operations, as elaborated below.</span></span> <span data-ttu-id="734c5-123">In het bovenstaande voor beeld is de enige instructie om de ingebouwde <xref:microsoft.quantum.intrinsic.x>Q #-bewerking aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="734c5-123">In the example above, the only statement is to call the built-in Q# operation <xref:microsoft.quantum.intrinsic.x>.</span></span>

<span data-ttu-id="734c5-124">Bewerkingen kunnen ook interessante typen retour neren dan `Unit`.</span><span class="sxs-lookup"><span data-stu-id="734c5-124">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="734c5-125">Zo retourneert de <xref:microsoft.quantum.intrinsic.m>-bewerking een uitvoer van het type `Result`die een meting heeft uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="734c5-125">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="734c5-126">U kunt de uitvoer van een bewerking naar een andere bewerking door geven of u kunt deze gebruiken met het sleutel woord `let` om een nieuwe variabele te definiëren.</span><span class="sxs-lookup"><span data-stu-id="734c5-126">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>
<!-- Link to UID for superdense conceptual and example documentation. -->
<span data-ttu-id="734c5-127">Dit maakt het mogelijk om klassieke berekeningen aan te duiden die met Quantum bewerkingen op een laag niveau reageren, zoals bij de code ring van de functie:</span><span class="sxs-lookup"><span data-stu-id="734c5-127">This allows for representing classical computation that interacts with quantum operations at a low level, such as in superdense coding:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a><span data-ttu-id="734c5-128">Functors, adjoint en beheerd</span><span class="sxs-lookup"><span data-stu-id="734c5-128">Functors, adjoint and controlled</span></span>
<span data-ttu-id="734c5-129">Als een bewerking een unitary-trans formatie implementeert, is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt.</span><span class="sxs-lookup"><span data-stu-id="734c5-129">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="734c5-130">Met een adjoint specialisatie van een bewerking wordt aangegeven hoe deze in omgekeerde volg orde reageert, terwijl een beheerde specialisatie aangeeft hoe een bewerking reageert wanneer de status van een Quantum register wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="734c5-130">An adjoint specialization of an operation specifies how it acts when run in reverse, while a controlled specialization specifies how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="734c5-131">Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking: `is Adj + Ctl` in het volgende voor beeld.</span><span class="sxs-lookup"><span data-stu-id="734c5-131">The existence of these specializations can be declared as part of the operation signature: `is Adj + Ctl` in the following example.</span></span> <span data-ttu-id="734c5-132">De bijbehorende implementatie voor elke impliciet gedeclareerde specialisatie wordt vervolgens door de compiler gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="734c5-132">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> <span data-ttu-id="734c5-133">Veel bewerkingen in Q # vertegenwoordigen unitary Gates.</span><span class="sxs-lookup"><span data-stu-id="734c5-133">Many operations in Q# represent unitary gates.</span></span>
> <span data-ttu-id="734c5-134">Als $U $ de unitary-poort is die wordt weer gegeven door een bewerking `U`, vertegenwoordigt `Adjoint U` de unitary-poort $U ^ \dagger $.</span><span class="sxs-lookup"><span data-stu-id="734c5-134">If $U$ is the unitary gate represented by an operation `U`, then `Adjoint U` represents the unitary gate $U^\dagger$.</span></span>

<span data-ttu-id="734c5-135">Als de implementatie niet kan worden gegenereerd door de compiler, kan deze expliciet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="734c5-135">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="734c5-136">Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte instructie voor het genereren of een door de gebruiker gedefinieerde implementatie.</span><span class="sxs-lookup"><span data-stu-id="734c5-136">Such explicit specialization declarations can consist of a suitable generation directive or a user defined implementation.</span></span> <span data-ttu-id="734c5-137">De code in `PrepareEntangledPair` hierboven is bijvoorbeeld gelijk aan de onderstaande code met expliciete declaraties voor specialisatie:</span><span class="sxs-lookup"><span data-stu-id="734c5-137">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

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
<span data-ttu-id="734c5-138">Het sleutel woord `auto` geeft aan dat de compiler moet bepalen hoe u de implementatie van de specialisatie wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="734c5-138">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="734c5-139">Als de compiler de implementatie voor een bepaalde specialisatie niet automatisch kan genereren of als er een efficiëntere implementatie kan worden verleend, kan de implementatie ook hand matig worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="734c5-139">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

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
<span data-ttu-id="734c5-140">In het bovenstaande voor beeld geeft `adjoint invert;` aan dat de adjoint specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie.</span><span class="sxs-lookup"><span data-stu-id="734c5-140">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="734c5-141">Er worden meer voor beelden weer gegeven in een [hogere controle stroom](xref:microsoft.quantum.concepts.control-flow).</span><span class="sxs-lookup"><span data-stu-id="734c5-141">We will see more examples of this in [Higher-Order Control Flow](xref:microsoft.quantum.concepts.control-flow).</span></span>

<span data-ttu-id="734c5-142">Als u een specialisatie van een bewerking wilt aanroepen, gebruikt u de sleutel woorden `Adjoint` of `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="734c5-142">To call a specialization of an operation, use the `Adjoint` or `Controlled` keywords.</span></span>
<span data-ttu-id="734c5-143">Zo kan het bovenstaande voor beeld van de code ring van de bovenstaande sleutel sneller worden geschreven met behulp van de adjoint van `PrepareEntangledPair` om de Entangled-status terug te zetten in een unentangled paar qubits:</span><span class="sxs-lookup"><span data-stu-id="734c5-143">For example, the superdense coding example above can be written more compactly by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="734c5-144">Er zijn een aantal belang rijke beperkingen waarmee u rekening moet houden bij het ontwerpen van bewerkingen voor gebruik met functors.</span><span class="sxs-lookup"><span data-stu-id="734c5-144">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="734c5-145">De meeste van de voor delen van een bewerking die de uitvoer waarde van een andere bewerking gebruikt, kan niet automatisch worden gegenereerd door de compiler, omdat het niet eenduidig is hoe u de instructies in een dergelijke bewerking opnieuw ordent om hetzelfde effect te verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="734c5-145">Most critically, specializations for an operation that uses the output value of any other operation cannot be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>


## <a name="defining-new-functions"></a><span data-ttu-id="734c5-146">Nieuwe functies definiëren</span><span class="sxs-lookup"><span data-stu-id="734c5-146">Defining New Functions</span></span>

<span data-ttu-id="734c5-147">Q # biedt ook de mogelijkheid om *functies*te definiëren die verschillend zijn van bewerkingen in dat ze geen effect mogen hebben op het berekenen van een uitvoer waarde.</span><span class="sxs-lookup"><span data-stu-id="734c5-147">Q# also allows for defining *functions*, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="734c5-148">Met name functies kunnen geen bewerkingen aanroepen, reageren op qubits, voor beelden van wille keurige getallen of op andere wijze, afhankelijk van de invoer waarde voor een functie.</span><span class="sxs-lookup"><span data-stu-id="734c5-148">In particular, functions cannot call operations, act on qubits, sample random numbers, or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="734c5-149">Als gevolg hiervan zijn Q #-functies *puur*, in dat ze altijd dezelfde invoer waarden toewijzen aan dezelfde uitvoer waarden.</span><span class="sxs-lookup"><span data-stu-id="734c5-149">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="734c5-150">Hiermee kan de Q #-compiler veilig de volg orde wijzigen van hoe en wanneer-functies worden aangeroepen bij het genereren van bewerkings-specials.</span><span class="sxs-lookup"><span data-stu-id="734c5-150">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="734c5-151">Het definiëren van een functie werkt op dezelfde manier als het definiëren van een bewerking, behalve dat er geen adjoint of beheerde Specials kunnen worden gedefinieerd voor een functie.</span><span class="sxs-lookup"><span data-stu-id="734c5-151">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="734c5-152">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="734c5-152">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
<span data-ttu-id="734c5-153">Wanneer het mogelijk is om dit te doen, is het handig om klassieke logica te schrijven in termen van functies in plaats van bewerkingen, zodat deze gemakkelijk vanuit bewerkingen kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="734c5-153">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="734c5-154">Als we `Square` als een bewerking hebben geschreven, zou de compiler niet kunnen garanderen dat het aanroepen van deze met dezelfde invoer consequent dezelfde uitvoer produceert.</span><span class="sxs-lookup"><span data-stu-id="734c5-154">If we had written `Square` as an operation, for example, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="734c5-155">Als u het verschil tussen functies en bewerkingen wilt onderstrepen, moet u rekening houden met het probleem van klassieke steek proeven voor een wille keurig getal in een Q #-bewerking:</span><span class="sxs-lookup"><span data-stu-id="734c5-155">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="734c5-156">Elke keer dat `U` wordt aangeroepen, heeft het een andere actie op `target`.</span><span class="sxs-lookup"><span data-stu-id="734c5-156">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="734c5-157">Met name kan de compiler niet garanderen dat als we een `adjoint auto` specialisatie-declaratie aan `U`hebben toegevoegd, vervolgens `U(target); Adjoint U(target);` als identiteit fungeert (dat wil zeggen, als niet op).</span><span class="sxs-lookup"><span data-stu-id="734c5-157">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="734c5-158">Dit schendt de definitie van de adjoint die we hebben gezien in [vectoren en matrices](xref:microsoft.quantum.concepts.vectors), waardoor het automatisch genereren van een adjoint-specialisatie in een bewerking waarbij we de <xref:microsoft.quantum.math.randomreal> bewerking hebben aangeroepen, de door de compiler geboden garanties kan verstoren. ; <xref:microsoft.quantum.math.randomreal> is een bewerking waarvoor geen adjoint of gecontroleerde versie bestaat.</span><span class="sxs-lookup"><span data-stu-id="734c5-158">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="734c5-159">Daarentegen is het mogelijk om functie aanroepen zoals `Square` veilig te maken, omdat de compiler er zeker van kan zijn dat de invoer alleen moet worden behouden voor `Square` om de uitvoer stabiel te houden.</span><span class="sxs-lookup"><span data-stu-id="734c5-159">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="734c5-160">Door zo veel mogelijk klassieke logica in functies te isoleren, is het eenvoudig om die logica in andere functies en bewerkingen hetzelfde te hergebruiken.</span><span class="sxs-lookup"><span data-stu-id="734c5-160">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>

## <a name="control-flow"></a><span data-ttu-id="734c5-161">Controlestroom</span><span class="sxs-lookup"><span data-stu-id="734c5-161">Control Flow</span></span>

<span data-ttu-id="734c5-162">Binnen een bewerking of functie wordt elke instructie in volg orde uitgevoerd, vergelijkbaar met de meest voorkomende verplichte klassieke talen.</span><span class="sxs-lookup"><span data-stu-id="734c5-162">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="734c5-163">Deze controle stroom kan echter op drie verschillende manieren worden gewijzigd:</span><span class="sxs-lookup"><span data-stu-id="734c5-163">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="734c5-164">`if`-instructies</span><span class="sxs-lookup"><span data-stu-id="734c5-164">`if` Statements</span></span>
- <span data-ttu-id="734c5-165">`for` lussen</span><span class="sxs-lookup"><span data-stu-id="734c5-165">`for` Loops</span></span>
- <span data-ttu-id="734c5-166">`repeat`-`until` lussen</span><span class="sxs-lookup"><span data-stu-id="734c5-166">`repeat`-`until` Loops</span></span>

<span data-ttu-id="734c5-167">We stellen de bespreking van deze laatste uit tot we [herhalen tot succes (RUS)-](xref:microsoft.quantum.techniques.qubits#measurements) circuits.</span><span class="sxs-lookup"><span data-stu-id="734c5-167">We defer discussion of the latter until we discuss [Repeat Until Success (RUS)](xref:microsoft.quantum.techniques.qubits#measurements) circuits.</span></span>
<span data-ttu-id="734c5-168">De constructies van de controle stroom `if` en `for` gaan echter door in een vertrouwde zin voor de meeste klassieke programmeer talen.</span><span class="sxs-lookup"><span data-stu-id="734c5-168">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>
<span data-ttu-id="734c5-169">Met name een `if`-instructie kan een voor waarde aannemen, gevolgd door een of meer `elif`-instructies, en kan eindigen met een `else`:</span><span class="sxs-lookup"><span data-stu-id="734c5-169">In particular, an `if` statement can take a condition, may be followed by one or more `elif` statements, and may end with an `else`:</span></span>

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

<span data-ttu-id="734c5-170">Op dezelfde manier geven `for` lussen een herhaling aan voor een bereik met gehele getallen of over de elementen van een matrix:</span><span class="sxs-lookup"><span data-stu-id="734c5-170">Similarly, `for` loops indicate iteration over a range of integers or over the elements of an array:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

<span data-ttu-id="734c5-171">Belang rijk: `for` lussen en `if`-instructies kunnen zelfs worden gebruikt in bewerkingen waarvoor specials automatisch worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="734c5-171">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="734c5-172">In dat geval wordt de adjoint van een `for` loop de richting omkeren en wordt de adjoint van elke iteratie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="734c5-172">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="734c5-173">Dit is het principe ' schoenen en SOCKS ': als u het uitvoeren van een SOCKS ongedaan wilt maken en vervolgens schoenen wilt maken, moet u het op schoenen opzetten en vervolgens op SOCKS ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="734c5-173">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="734c5-174">Het werkt minder goed om uw SOCKS uit te proberen terwijl u nog steeds uw schoenen afdraagt!</span><span class="sxs-lookup"><span data-stu-id="734c5-174">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="operations-and-functions-as-first-class-values"></a><span data-ttu-id="734c5-175">Bewerkingen en functies als waarden voor de eerste klasse</span><span class="sxs-lookup"><span data-stu-id="734c5-175">Operations and Functions as First-Class Values</span></span>

<span data-ttu-id="734c5-176">Een van de essentiële technieken voor het opwegen van de controle stroom en klassieke logica met behulp van functies in plaats van bewerkingen is het gebruik van die bewerkingen en functies in Q # zijn de *eerste klasse*.</span><span class="sxs-lookup"><span data-stu-id="734c5-176">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="734c5-177">Dat wil zeggen dat ze elke waarde in de taal in hun eigen recht zijn.</span><span class="sxs-lookup"><span data-stu-id="734c5-177">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="734c5-178">Het volgende is bijvoorbeeld een zeer geldige Q #-code, als een beetje indirect:</span><span class="sxs-lookup"><span data-stu-id="734c5-178">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="734c5-179">De waarde van de variabele `ourH` in het bovenstaande fragment is dan de bewerking <xref:microsoft.quantum.intrinsic.h>, zodat de waarde kan worden aangeroepen, zoals elke andere bewerking.</span><span class="sxs-lookup"><span data-stu-id="734c5-179">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="734c5-180">Hierdoor kunnen we bewerkingen schrijven die bewerkingen als onderdeel van hun invoer doen, waardoor de controle stroom concepten met een hogere volg orde kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="734c5-180">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="734c5-181">We kunnen bijvoorbeeld Voorst Ellen om een bewerking te ' Square ' door deze twee keer op dezelfde doel-Qubit toe te passen.</span><span class="sxs-lookup"><span data-stu-id="734c5-181">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="734c5-182">In dit voor beeld wordt met de pijl `=>` die wordt weer gegeven in het type `(Qubit => Unit)` aangegeven dat het invoer veld `op` een bewerking is die als invoer wordt gebruikt voor het type `Qubit` en wordt er een lege tuple gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="734c5-182">In this example, the `=>` arrow that appears in the type `(Qubit => Unit)` denotes that the input field `op` is an operation which takes as its input the type `Qubit` and produces an empty tuple as its output.</span></span>
<span data-ttu-id="734c5-183">Daarnaast geven we de kenmerken van het betreffende bewerkings type op, die de informatie bevatten over welke functors worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="734c5-183">Additionally we specify the characteristics of that operation type, which contain the information about which functors are supported.</span></span>
<span data-ttu-id="734c5-184">Een bewerking van het type `(Qubit => Unit)` ondersteunt noch de `Adjoint` noch de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="734c5-184">An operation of type `(Qubit => Unit)` supports neither the `Adjoint` nor the `Controlled` functor.</span></span> <span data-ttu-id="734c5-185">Als we willen aangeven dat een bewerking van dit type moet worden ondersteund, bijvoorbeeld het `Adjoint` functor, moeten we het declareren als adjointable.</span><span class="sxs-lookup"><span data-stu-id="734c5-185">If we want to indicate that an operation of that type has to support e.g. the `Adjoint` functor, we have to declare it as being adjointable.</span></span> <span data-ttu-id="734c5-186">Dit wordt gedaan met behulp van de aantekening `is Adj` voor het type.</span><span class="sxs-lookup"><span data-stu-id="734c5-186">This is done by using the annotation `is Adj` to the type.</span></span> <span data-ttu-id="734c5-187">Op dezelfde manier geeft `(Qubit => Unit is Ctl)` aan dat een bewerking van dat type de `Controlled` functor ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="734c5-187">Similarly, `(Qubit => Unit is Ctl)` denotes that an operation of that type supports the `Controlled` functor.</span></span> <span data-ttu-id="734c5-188">We zullen dit verder verkennen wanneer we [types in Q #] (XREF: micro soft. Quantum. language. type-model) in het algemeen bespreken.</span><span class="sxs-lookup"><span data-stu-id="734c5-188">We will explore this further when we discuss [types in Q#] (xref:microsoft.quantum.language.type-model) more generally.</span></span>

<span data-ttu-id="734c5-189">We benadrukken nu dat we ook bewerkingen kunnen retour neren als onderdeel van uitvoer, zodat we een aantal van de klassieke voorwaardelijke logica kunnen isoleren als een klassieke functie waarmee een beschrijving van een Quantum programma wordt geretourneerd in de vorm van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="734c5-189">For now, we emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="734c5-190">Als eenvoudig voor beeld kunt u het voor beeld van teleportie overwegen, waarbij de partij die een twee-bits klassiek bericht ontvangt, het bericht moet gebruiken om hun Qubit te decoderen naar de juiste teleportal-status.</span><span class="sxs-lookup"><span data-stu-id="734c5-190">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="734c5-191">We kunnen dit schrijven in termen van een functie die deze twee klassieke bits accepteert en de juiste decodeer bewerking retourneert.</span><span class="sxs-lookup"><span data-stu-id="734c5-191">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

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

<span data-ttu-id="734c5-192">Deze nieuwe functie is inderdaad een functie. als we deze aanroepen met dezelfde waarden van `hereBit` en `thereBit`, krijgen we altijd dezelfde bewerking.</span><span class="sxs-lookup"><span data-stu-id="734c5-192">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="734c5-193">Het is dus mogelijk dat de decoder veilig kan worden uitgevoerd binnen bewerkingen zonder dat dit de reden hoeft te zijn van de manier waarop de decodeer logica communiceert met de definities van de verschillende bewerkings-specials.</span><span class="sxs-lookup"><span data-stu-id="734c5-193">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="734c5-194">Dat wil zeggen dat we de klassieke logica binnen een functie hebben geïsoleerd, zodat de compiler kan worden gevolgd met impunity, zolang de invoer wordt bewaard.</span><span class="sxs-lookup"><span data-stu-id="734c5-194">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>

<span data-ttu-id="734c5-195">We kunnen ook functies behandelen als waarden voor de eerste klasse, aangezien we meer details zien wanneer we [bewerkingen en functie typen](#operations-and-functions-as-first-class-values)bespreken.</span><span class="sxs-lookup"><span data-stu-id="734c5-195">We can also treat functions as first-class values, as we will see in more detail when we discuss [operations and function types](#operations-and-functions-as-first-class-values).</span></span>

## <a name="partially-applying-operations-and-functions"></a><span data-ttu-id="734c5-196">Bewerkingen en functies gedeeltelijk Toep assen</span><span class="sxs-lookup"><span data-stu-id="734c5-196">Partially Applying Operations and Functions</span></span>

<span data-ttu-id="734c5-197">We kunnen aanzienlijk meer doen met functies die bewerkingen retour neren met behulp van *gedeeltelijke toepassing*, waarbij we een of meer delen van de invoer kunnen bieden aan een functie of bewerking zonder dat deze daad werkelijk wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="734c5-197">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="734c5-198">Als u bijvoorbeeld het bovenstaande `ApplyTwice`-voor beeld aanroept, kunnen we aangeven dat we niet meteen willen opgeven dat Qubit de invoer bewerking moet worden toegepast:</span><span class="sxs-lookup"><span data-stu-id="734c5-198">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="734c5-199">In dit geval bevat de lokale variabele `twiceOp` de gedeeltelijk toegepaste bewerking `ApplyTwice(op, _)`, waarbij delen van de invoer die nog niet zijn opgegeven, worden aangegeven door `_`.</span><span class="sxs-lookup"><span data-stu-id="734c5-199">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="734c5-200">Wanneer we `twiceOp` op de volgende regel daad werkelijk aanroepen, geven we de invoer door aan de gedeeltelijk toegepaste bewerking van alle resterende delen van de invoer voor de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="734c5-200">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="734c5-201">Het bovenstaande code fragment is dus in feite identiek aan het direct aanroepen van `ApplyTwice(op, target)`, opslaan voor dat we een nieuwe lokale variabele hebben geïntroduceerd waarmee we de oproep kunnen vertragen terwijl sommige onderdelen van de invoer worden vertraagd.</span><span class="sxs-lookup"><span data-stu-id="734c5-201">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="734c5-202">Omdat een bewerking die gedeeltelijk is toegepast, niet daad werkelijk wordt aangeroepen totdat de volledige invoer is opgegeven, kunnen we bewerkingen gedeeltelijk Toep assen, zelfs binnen functies.</span><span class="sxs-lookup"><span data-stu-id="734c5-202">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="734c5-203">In principe zou de klassieke logica binnen `SquareOperation` veel meer betrokken kunnen zijn, maar nog steeds geïsoleerd van de rest van een bewerking door de garanties dat de compiler over functies kan bieden.</span><span class="sxs-lookup"><span data-stu-id="734c5-203">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="734c5-204">Deze benadering wordt gebruikt in de standaard bibliotheek van Q # voor het uitdrukken van de klassieke controle stroom op een manier die eenvoudig kan worden gebruikt binnen Quantum Program ma's.</span><span class="sxs-lookup"><span data-stu-id="734c5-204">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>
