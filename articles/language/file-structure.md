---
title: Bestands structuur | Microsoft Docs
description: 'Q # bestands structuur'
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 40b2e7ddf5def6285250dffe130b152429dce1f8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185185"
---
# <a name="file-structure"></a><span data-ttu-id="86312-103">Bestandsstructuur</span><span class="sxs-lookup"><span data-stu-id="86312-103">File Structure</span></span>

<span data-ttu-id="86312-104">Een Q #-bestand bestaat uit een reeks naam ruimte declaraties.</span><span class="sxs-lookup"><span data-stu-id="86312-104">A Q# file consists of a sequence of namespace declarations.</span></span>
<span data-ttu-id="86312-105">Elke naam ruimte declaratie bevat declaraties voor door de gebruiker gedefinieerde typen, bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="86312-105">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="86312-106">Een naam ruimte declaratie kan elk wille keurig aantal van elk type declaratie en in een wille keurige volg orde bevatten.</span><span class="sxs-lookup"><span data-stu-id="86312-106">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="86312-107">De enige tekst die buiten een naam ruimte declaratie kan worden weer gegeven, is opmerkingen.</span><span class="sxs-lookup"><span data-stu-id="86312-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="86312-108">In het bijzonder worden documentatie opmerkingen voor een naam ruimte voorafgaat aan de declaratie.</span><span class="sxs-lookup"><span data-stu-id="86312-108">In particular, documentation comments for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="86312-109">Naam ruimte declaraties</span><span class="sxs-lookup"><span data-stu-id="86312-109">Namespace Declarations</span></span>

<span data-ttu-id="86312-110">Een Q #-bestand heeft normaal gesp roken precies één naam ruimte declaratie, maar kan geen hebben (en mag niet leeg zijn of alleen opmerkingen bevatten) of kan meerdere naam ruimten bevatten.</span><span class="sxs-lookup"><span data-stu-id="86312-110">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="86312-111">Naam ruimte declaraties mogen niet worden genest.</span><span class="sxs-lookup"><span data-stu-id="86312-111">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="86312-112">Dezelfde naam ruimte kan worden gedeclareerd in meerdere Q #-bestanden die samen worden gecompileerd, zolang er geen type, bewerking of functie declaraties met dezelfde naam zijn.</span><span class="sxs-lookup"><span data-stu-id="86312-112">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="86312-113">Het is met name ongeldig om hetzelfde type in dezelfde naam ruimte in meerdere bestanden te definiëren, zelfs als de declaraties identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="86312-113">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="86312-114">Een naam ruimte declaratie bestaat uit het tref woord `namespace`, gevolgd door de naam van de naam ruimte, een open accolade `{`, de declaraties in de naam ruimte en een sluitende accolade `}`.</span><span class="sxs-lookup"><span data-stu-id="86312-114">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="86312-115">Naam ruimte namen volgen het .NET-patroon van een reeks van een of meer juridische symbolen, gescheiden door punten `.`.</span><span class="sxs-lookup"><span data-stu-id="86312-115">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="86312-116">Zo zijn `MyQuantumStuff` en `Microsoft.Quantum.Canon` geldige naam ruimte namen.</span><span class="sxs-lookup"><span data-stu-id="86312-116">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Canon` are valid namespace names.</span></span>
<span data-ttu-id="86312-117">Per Conventie worden de symbolen in de naam van een naam ruimte gekapitaliseerd, maar dit is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="86312-117">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="86312-118">Declaraties kunnen in een wille keurige volg orde worden weer gegeven in een naam ruimte declaratie.</span><span class="sxs-lookup"><span data-stu-id="86312-118">Declarations may appear in any order in a namespace declaration.</span></span>
<span data-ttu-id="86312-119">Verwijzingen naar typen of callables die verder in een bestand worden aangegeven, worden op de juiste wijze opgelost. het is niet nodig om een verwijzing naar het type, de bewerking of de functie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="86312-119">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="86312-120">Open instructies</span><span class="sxs-lookup"><span data-stu-id="86312-120">Open Directives</span></span>

<span data-ttu-id="86312-121">Binnen een naam ruimte blok kan de `open`-instructie worden gebruikt voor het importeren van alle typen en callables die in een bepaalde naam ruimte zijn gedefinieerd en deze te raadplegen op basis van de niet-gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="86312-121">Within a namespace block, the `open` directive may be used to import all types and callables defined in a certain namespace and refer to them by their unqualified name.</span></span> 

<span data-ttu-id="86312-122">Een dergelijke `open`-instructie bestaat uit het sleutel woord `open`, gevolgd door de naam ruimte die moet worden geopend en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="86312-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

<span data-ttu-id="86312-123">Bijvoorbeeld,</span><span class="sxs-lookup"><span data-stu-id="86312-123">For instance,</span></span>

```qsharp
open Microsoft.Quantum.Canon;
```

<span data-ttu-id="86312-124">Een korte naam voor de naam ruimte kan eventueel worden gedefinieerd, zodat alle elementen van die naam ruimte kunnen (en moeten) worden gekwalificeerd door de gedefinieerde korte naam.</span><span class="sxs-lookup"><span data-stu-id="86312-124">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="86312-125">Een dergelijke korte naam wordt gedefinieerd door het tref woord `as` gevolgd door de gewenste korte naam vóór de punt komma in een `open`-instructie toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="86312-125">Such a short name is defined by adding the keyword `as` followed by the desired short name before the semicolon in an `open` directive:</span></span>

```qsharp
open Microsoft.Quantum.Math as Math;
```

<span data-ttu-id="86312-126">Alle `open`-instructies moeten vóór een `function`, `operation`of `newtype` declaraties in het naam ruimte blok worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="86312-126">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>
<span data-ttu-id="86312-127">De `open`-instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.</span><span class="sxs-lookup"><span data-stu-id="86312-127">The `open` directive applies to the entire namespace block within a file.</span></span>

## <a name="user-defined-type-declarations"></a><span data-ttu-id="86312-128">Door de gebruiker gedefinieerde type declaraties</span><span class="sxs-lookup"><span data-stu-id="86312-128">User-Defined Type Declarations</span></span>

<span data-ttu-id="86312-129">Q # biedt gebruikers een manier om nieuwe door de gebruiker gedefinieerde typen te declareren, zoals beschreven in de sectie [Q # type model](xref:microsoft.quantum.language.type-model) .</span><span class="sxs-lookup"><span data-stu-id="86312-129">Q# provides a way for users to declare new user-defined types, as described in the [Q# type model](xref:microsoft.quantum.language.type-model) section.</span></span>
<span data-ttu-id="86312-130">Door de gebruiker gedefinieerde typen zijn verschillend, zelfs als de basis typen identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="86312-130">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="86312-131">In het bijzonder is er geen automatische conversie tussen waarden van twee door de gebruiker gedefinieerde typen, zelfs als de onderliggende typen identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="86312-131">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

<span data-ttu-id="86312-132">Een door de gebruiker gedefinieerde type declaratie bestaat uit het tref woord `newtype`, gevolgd door de naam van het door de gebruiker gedefinieerde type, een `=`, een geldige type specificatie en een afsluitende punt komma.</span><span class="sxs-lookup"><span data-stu-id="86312-132">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="86312-133">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="86312-133">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="86312-134">Elk Q #-bron bestand kan elk gewenst aantal door de gebruiker gedefinieerde typen declareren.</span><span class="sxs-lookup"><span data-stu-id="86312-134">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="86312-135">Type namen moeten uniek zijn binnen een naam ruimte en kunnen geen conflict veroorzaken met de namen van bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="86312-135">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="86312-136">Het is niet mogelijk om circulaire afhankelijkheden tussen door de gebruiker gedefinieerde typen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="86312-136">It is not possible to define circular dependencies between user defined types.</span></span> <span data-ttu-id="86312-137">Recursieve typen zijn daarom niet mogelijk binnen Q #.</span><span class="sxs-lookup"><span data-stu-id="86312-137">Recursive types are thus not possible within Q#.</span></span>

## <a name="operation-declarations"></a><span data-ttu-id="86312-138">Bewerkings declaraties</span><span class="sxs-lookup"><span data-stu-id="86312-138">Operation Declarations</span></span>

<span data-ttu-id="86312-139">Bewerkingen zijn de kern van Q #, ongeveer vergelijkbaar met functies in andere talen.</span><span class="sxs-lookup"><span data-stu-id="86312-139">Operations are the core of Q#, roughly analogous to functions in other languages.</span></span>
<span data-ttu-id="86312-140">Elk Q #-bron bestand kan een wille keurig aantal bewerkingen definiëren.</span><span class="sxs-lookup"><span data-stu-id="86312-140">Each Q# source file may define any number of operations.</span></span>

<span data-ttu-id="86312-141">Bewerkings namen moeten uniek zijn binnen een naam ruimte en kunnen niet conflicteren met type-en functie namen.</span><span class="sxs-lookup"><span data-stu-id="86312-141">Operation names must be unique within a namespace and may not conflict with type and function names.</span></span>

<span data-ttu-id="86312-142">Een bewerkings declaratie bestaat uit het tref woord `operation`, gevolgd door het symbool dat de naam van de bewerking is, een getypte id-tuple waarmee de argumenten voor de bewerking worden gedefinieerd, een dubbele punt `:`, een type aantekening die het resultaat type van de bewerking beschrijft, optioneel een aantekening met de bewerkings kenmerken, een open accolade `{`, de hoofd tekst van de bewerkings declaratie en een uiteindelijke sluitings accolade `}`.</span><span class="sxs-lookup"><span data-stu-id="86312-142">An operation declarations consists of the keyword `operation`, followed by the symbol that is the operation’s name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation’s result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="86312-143">De hoofd tekst van de bewerkings declaratie bestaat uit de standaard implementatie of van een lijst met specials.</span><span class="sxs-lookup"><span data-stu-id="86312-143">The body of the operation declaration either consists of the default implementation or of a list of specializations.</span></span>
<span data-ttu-id="86312-144">De standaard implementatie kan rechtstreeks in de declaratie worden opgegeven als alleen de implementatie van de standaard hoofd code specialize expliciet moet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="86312-144">The default implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to specified explicitly.</span></span>
<span data-ttu-id="86312-145">In dit geval is een aantekening met de bewerkings kenmerken in de declaratie handig om ervoor te zorgen dat de compiler automatisch andere specials wordt gegenereerd op basis van de standaard implementatie.</span><span class="sxs-lookup"><span data-stu-id="86312-145">In this case, an annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="86312-146">Bijvoorbeeld</span><span class="sxs-lookup"><span data-stu-id="86312-146">For example</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

<span data-ttu-id="86312-147">Met bewerkings kenmerken wordt gedefinieerd welke soorten functors kunnen worden toegepast op de gedeclareerde bewerking en welk effect ze hebben.</span><span class="sxs-lookup"><span data-stu-id="86312-147">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="86312-148">Als een bewerking een unitary-trans formatie implementeert, is het mogelijk om te definiëren hoe de bewerking optreedt wanneer *adjointed* of *beheerd*wordt.</span><span class="sxs-lookup"><span data-stu-id="86312-148">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span>
<span data-ttu-id="86312-149">Het bestaan van deze specials kan worden gedeclareerd als onderdeel van de hand tekening van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="86312-149">The existence of these specializations can be declared as part of the operation signature.</span></span> <span data-ttu-id="86312-150">De bijbehorende implementatie voor elke impliciet gedeclareerde specialisatie wordt vervolgens door de compiler gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="86312-150">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> <span data-ttu-id="86312-151">In het bovenstaande voor beeld worden een adjoint, een beheerde en beheerde adjoint-specialisatie gegenereerd door de compiler.</span><span class="sxs-lookup"><span data-stu-id="86312-151">In the example above, an adjoint, a controlled, and a controlled adjoint specialization are generated by the compiler.</span></span> 

<span data-ttu-id="86312-152">Als de implementatie niet kan worden gegenereerd door de compiler, kan deze expliciet worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="86312-152">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="86312-153">Dergelijke expliciete specialisatie declaraties kunnen bestaan uit een geschikte generatie-instructie die verduidelijkt hoe een bepaalde specialisatie moet worden gebouwd of een door de gebruiker gedefinieerde implementatie.</span><span class="sxs-lookup"><span data-stu-id="86312-153">Such explicit specialization declarations can either consist of a suitable generation directive that clarify how a certain specialization is to be built, or a user defined implementation.</span></span> <span data-ttu-id="86312-154">De code in `PrepareEntangledPair` hierboven is bijvoorbeeld gelijk aan de onderstaande code met expliciete declaraties voor specialisatie:</span><span class="sxs-lookup"><span data-stu-id="86312-154">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

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
<span data-ttu-id="86312-155">Het sleutel woord `auto` geeft aan dat de compiler moet bepalen hoe u de implementatie van de specialisatie wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="86312-155">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="86312-156">Als de compiler de implementatie voor een bepaalde specialisatie niet kan genereren zonder verdere instructies, zoals een nauw keurigere generatie-instructie, of als er een efficiëntere implementatie kan worden verleend, kan de implementatie ook hand matig worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="86312-156">If the compiler cannot generate the implementation for a certain specialization without further instructions - like a more precise generation directive -, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

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

<span data-ttu-id="86312-157">In het bovenstaande voor beeld geeft `adjoint invert;` aan dat de adjoint specialisatie moet worden gegenereerd door de implementatie van de hoofd tekst te omkeren en `controlled adjoint invert;` geeft aan dat de beheerde adjoint-specialisatie moet worden gegenereerd door de opgegeven implementatie van de beheerde specialisatie.</span><span class="sxs-lookup"><span data-stu-id="86312-157">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="86312-158">Voor een bewerking ter ondersteuning van de toepassing van de `Adjoint` en/of `Controlled` functor moet het retour type per se worden `Unit`.</span><span class="sxs-lookup"><span data-stu-id="86312-158">For an operation to support application of the `Adjoint` and/or `Controlled` functor, its return type necessarily needs to be `Unit`.</span></span> 


### <a name="explicit-specialization-declarations"></a><span data-ttu-id="86312-159">Expliciete specialisatie declaraties</span><span class="sxs-lookup"><span data-stu-id="86312-159">Explicit Specialization Declarations</span></span>

<span data-ttu-id="86312-160">Q #-bewerkingen kunnen de volgende expliciete specialisatie declaraties bevatten:</span><span class="sxs-lookup"><span data-stu-id="86312-160">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="86312-161">Met de `body` specialize wordt de implementatie van de bewerking opgegeven waarvoor geen functors is toegepast.</span><span class="sxs-lookup"><span data-stu-id="86312-161">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="86312-162">Met de `adjoint` specialize wordt de implementatie van de bewerking opgegeven waarop de `Adjoint` functor is toegepast.</span><span class="sxs-lookup"><span data-stu-id="86312-162">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="86312-163">Met de `controlled` specialize wordt de implementatie van de bewerking opgegeven waarop de `Controlled` functor is toegepast.</span><span class="sxs-lookup"><span data-stu-id="86312-163">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="86312-164">Met de `controlled adjoint` specialize wordt de implementatie van de bewerking opgegeven met zowel de `Adjoint` als `Controlled` functors toegepast.</span><span class="sxs-lookup"><span data-stu-id="86312-164">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="86312-165">Deze specialisatie kan ook worden benoemd `adjoint controlled`, omdat de twee functors werkend zijn.</span><span class="sxs-lookup"><span data-stu-id="86312-165">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="86312-166">Een specialisatie bewerking bestaat uit de code voor specialisatie (zoals bijvoorbeeld `body`of `adjoint`enzovoort), gevolgd door een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="86312-166">An operation specialization consists of the specialization tag (like e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="86312-167">Een expliciete declaratie zoals hieronder wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="86312-167">An explicit declaration as described below.</span></span>
- <span data-ttu-id="86312-168">Een instructie die de compiler vertelt hoe de specialisatie moet worden gegenereerd, een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="86312-168">A directive that tells the compiler how to generate the specialization, one of:</span></span>
  - <span data-ttu-id="86312-169">`intrinsic`, wat aangeeft dat de specialisatie wordt verschaft door de doel computer.</span><span class="sxs-lookup"><span data-stu-id="86312-169">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="86312-170">`distribute`, die kan worden gebruikt met de `controlled` en `controlled adjoint` specials.</span><span class="sxs-lookup"><span data-stu-id="86312-170">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="86312-171">Bij gebruik in combi natie met `controlled`geeft het aan dat de compiler de specialisatie moet berekenen door `Controlled` toe te passen op alle bewerkingen in de `body`.</span><span class="sxs-lookup"><span data-stu-id="86312-171">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="86312-172">Bij gebruik in combi natie met `controlled adjoint`geeft het aan dat de compiler de specialisatie moet berekenen door `Controlled` toe te passen op alle bewerkingen in de `adjoint` specialisatie.</span><span class="sxs-lookup"><span data-stu-id="86312-172">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="86312-173">`invert`, wat aangeeft dat de compiler de `adjoint` specialisatie moet berekenen door de `body`te omkeren, dat wil zeggen de volg orde van de bewerkingen en het Toep assen van de adjoint.</span><span class="sxs-lookup"><span data-stu-id="86312-173">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="86312-174">In combi natie met `adjoint controlled`geeft dit aan dat de compiler de specialisatie moet berekenen door de `controlled` specialisatie te omkeren.</span><span class="sxs-lookup"><span data-stu-id="86312-174">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="86312-175">`self`, om aan te geven dat de adjoint specialize hetzelfde is als de `body` specialize.</span><span class="sxs-lookup"><span data-stu-id="86312-175">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="86312-176">Dit is juridisch voor de `adjoint` en `adjoint controlled` specials.</span><span class="sxs-lookup"><span data-stu-id="86312-176">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="86312-177">Voor `adjoint controlled`impliceert `self` dat de `adjoint controlled` specialize hetzelfde is als de specialisatie `controlled`.</span><span class="sxs-lookup"><span data-stu-id="86312-177">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="86312-178">`auto`, om aan te geven dat de compiler een geschikte richt lijn moet selecteren om toe te passen.</span><span class="sxs-lookup"><span data-stu-id="86312-178">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="86312-179">`auto` mag niet worden gebruikt voor de `body` specialize.</span><span class="sxs-lookup"><span data-stu-id="86312-179">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="86312-180">De instructies en `auto` alle vereisen een sluitende punt komma `;`.</span><span class="sxs-lookup"><span data-stu-id="86312-180">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="86312-181">De `auto`-instructie wordt omgezet in de volgende generatie-instructie als een expliciete declaratie van de `body` wordt gegeven:</span><span class="sxs-lookup"><span data-stu-id="86312-181">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="86312-182">De `adjoint` specialisatie wordt gegenereerd volgens de richt lijn `invert`.</span><span class="sxs-lookup"><span data-stu-id="86312-182">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="86312-183">De `controlled` specialisatie wordt gegenereerd volgens de richt lijn `distribute`.</span><span class="sxs-lookup"><span data-stu-id="86312-183">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="86312-184">De `adjoint controlled` specialisatie wordt gegenereerd volgens de richt lijn `invert` als een expliciete declaratie voor `controlled` wordt gegeven, maar niet een voor `adjoint`, en `distribute` anders.</span><span class="sxs-lookup"><span data-stu-id="86312-184">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="86312-185">Als een bewerking zelf adjoint is, geeft u expliciet de adjoint of de bewaakte adjoint-specialisatie op via de generatie-instructie `self` zodat de compiler gebruik kan maken van die gegevens voor optimaliserings doeleinden.</span><span class="sxs-lookup"><span data-stu-id="86312-185">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="86312-186">Een specialisatie declaratie met een door de gebruiker gedefinieerde implementatie bestaat uit een argument tuple gevolgd door een instructie blok met de Q #-code die de specialisatie implementeert.</span><span class="sxs-lookup"><span data-stu-id="86312-186">A specialization declaration containing a user defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="86312-187">In de lijst met argumenten wordt `...` gebruikt om de argumenten weer te geven die zijn gedeclareerd voor de bewerking als geheel.</span><span class="sxs-lookup"><span data-stu-id="86312-187">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="86312-188">Voor `body` en `adjoint`moet de lijst met argumenten altijd worden `(...)`; voor `controlled` en `adjoint controlled`moet de lijst met argumenten een symbool zijn dat de matrix van besturings element qubits, gevolgd door `...`, tussen haakjes. bijvoorbeeld `(controls,...)`.</span><span class="sxs-lookup"><span data-stu-id="86312-188">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

<span data-ttu-id="86312-189">Als een of meer specialisaties naast de standaard hoofd tekst expliciet moeten worden gedeclareerd, moet de implementatie voor de standaard hoofd tekst ook worden ingepakt in een geschikte specialisatie declaratie.</span><span class="sxs-lookup"><span data-stu-id="86312-189">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qs: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (q in qs) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="adjoint"></a><span data-ttu-id="86312-190">Adjoint</span><span class="sxs-lookup"><span data-stu-id="86312-190">Adjoint</span></span>

<span data-ttu-id="86312-191">Met de adjoint van een bewerking wordt aangegeven hoe de complexe geconjugeerde van de bewerking wordt geïmplementeerd, dat wil zeggen hoe de bewerking optreedt als ' in omgekeerde volg orde ' wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="86312-191">The adjoint of an operation specifies how the complex conjugate transpose of the operation is implemented, i.e. how the operation acts when "run in reverse".</span></span>
<span data-ttu-id="86312-192">Het is wettelijk om een bewerking zonder adjoint op te geven. meting bewerkingen hebben bijvoorbeeld geen adjoint, omdat ze niet omkeerbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="86312-192">It is legal to specify an operation with no adjoint; for instance, measurement operations have no adjoint because they are not invertible.</span></span>
<span data-ttu-id="86312-193">Een bewerking ondersteunt de `Adjoint` functor als de bijbehorende declaratie een impliciete of expliciete declaratie van een adjoint specialize bevat.</span><span class="sxs-lookup"><span data-stu-id="86312-193">An operation supports the `Adjoint` functor if its declaration contains an implicit or explicit declaration of an adjoint specialization.</span></span>
<span data-ttu-id="86312-194">Een expliciet gedeclareerde beheerde adjoint specialisatie impliceert dat er een adjoint-specialisatie bestaat.</span><span class="sxs-lookup"><span data-stu-id="86312-194">An explicitly declared controlled adjoint specialization implies the existence of an adjoint specialization.</span></span> 

<span data-ttu-id="86312-195">Voor een bewerking waarvan de hoofd tekst herhalen-tot-succes-lussen bevat, stelt u instructies, metingen, retour overzichten of aanroepen naar andere bewerkingen die de `Adjoint` functor niet ondersteunen, het automatisch genereren van een adjoint-specialisatie na de `invert` of @no__ de instructie t_2_ is niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="86312-195">For operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

### <a name="controlled"></a><span data-ttu-id="86312-196">Gelijkrichter</span><span class="sxs-lookup"><span data-stu-id="86312-196">Controlled</span></span>

<span data-ttu-id="86312-197">Met de gecontroleerde versie van een bewerking wordt aangegeven hoe een door een Quantum beheerde versie van de bewerking wordt geïmplementeerd, d.w.z. hoe een bewerking reageert wanneer deze wordt toegepast op de status van een Quantum register.</span><span class="sxs-lookup"><span data-stu-id="86312-197">The controlled version of an operation specifies how a quantum-controlled version of the operation is implemented, i.e. how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="86312-198">Een gedetailleerde beschrijving vindt u in de sectie [Controlled](xref:microsoft.quantum.language.type-model#controlled) .</span><span class="sxs-lookup"><span data-stu-id="86312-198">A more complete description is provided in the [Controlled](xref:microsoft.quantum.language.type-model#controlled) section.</span></span>

<span data-ttu-id="86312-199">Het is wettelijk om een bewerking zonder gecontroleerde versie op te geven. meting bewerkingen hebben bijvoorbeeld geen beheerde versie, omdat ze niet kunnen worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="86312-199">It is legal to specify an operation with no controlled version; for instance, measurement operations have no controlled version because they are not controllable.</span></span>
<span data-ttu-id="86312-200">Een bewerking ondersteunt de `Controlled` functor indien en alleen als de declaratie ervan een impliciete of expliciete declaratie van een beheerde specialisatie bevat.</span><span class="sxs-lookup"><span data-stu-id="86312-200">An operation supports the `Controlled` functor if and only if its declaration contains an implicit or explicit declaration of a controlled specialization.</span></span>
<span data-ttu-id="86312-201">Een expliciet gedeclareerde beheerde adjoint specialisatie impliceert dat er een beheerde specialisatie bestaat.</span><span class="sxs-lookup"><span data-stu-id="86312-201">An explicitly declared controlled adjoint specialization implies the existence of a controlled specialization.</span></span> 

<span data-ttu-id="86312-202">Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen ondersteuning bieden voor de `Controlled` functor, wordt het automatisch genereren van een gecontroleerde specialisatie volgens de `distribute` of `auto`-instructie niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="86312-202">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

### <a name="controlled-adjoint"></a><span data-ttu-id="86312-203">Beheerde adjoint</span><span class="sxs-lookup"><span data-stu-id="86312-203">Controlled Adjoint</span></span>

<span data-ttu-id="86312-204">De gecontroleerde adjoint-versie van een bewerking geeft aan hoe een Quantum versie van de adjoint van de bewerking wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="86312-204">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="86312-205">Het is niet toegestaan een bewerking op te geven zonder beheerde adjoint-versie. meting bewerkingen hebben bijvoorbeeld geen beheerde adjoint-versie omdat ze niet kunnen worden ingesteld of omkeerbaar.</span><span class="sxs-lookup"><span data-stu-id="86312-205">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="86312-206">Een beheerde adjoint-specialisatie voor een bewerking moet bestaan als en alleen als zowel een adjoint als een beheerde specialisatie bestaan.</span><span class="sxs-lookup"><span data-stu-id="86312-206">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="86312-207">In dat geval wordt het bestaan van de beheerde adjoint-specialisatie afgeleid en wordt er een geschikte specialisatie gegenereerd door de compiler als er expliciet geen implementatie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="86312-207">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="86312-208">Voor een bewerking waarvan de hoofd tekst aanroepen naar andere bewerkingen bevat die geen beheerde adjoint-versie hebben, kunt u het automatisch genereren van een adjoint-specialisatie volgens de `invert`, `distribute` of `auto`-instructie niet mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="86312-208">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="examples"></a><span data-ttu-id="86312-209">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="86312-209">Examples</span></span>

<span data-ttu-id="86312-210">Een bewerkings declaratie kan zo eenvoudig zijn als het volgende, wat de primitieve Pauli X-bewerking definieert:</span><span class="sxs-lookup"><span data-stu-id="86312-210">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (q : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

<span data-ttu-id="86312-211">Het volgende definieert de bewerking teleporteer.</span><span class="sxs-lookup"><span data-stu-id="86312-211">The following defines the teleport operation.</span></span>

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation EPR (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        EPR(target, ancilla);

        // Do the teleportation
        Adjoint EPR (ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a><span data-ttu-id="86312-212">Functie declaraties</span><span class="sxs-lookup"><span data-stu-id="86312-212">Function Declarations</span></span>

<span data-ttu-id="86312-213">Functions zijn louter klassieke routines in Q #.</span><span class="sxs-lookup"><span data-stu-id="86312-213">Functions are purely classical routines in Q#.</span></span>
<span data-ttu-id="86312-214">Elk Q #-bron bestand kan een wille keurig aantal functies definiëren.</span><span class="sxs-lookup"><span data-stu-id="86312-214">Each Q# source file may define any number of functions.</span></span>

<span data-ttu-id="86312-215">Een functie declaratie bestaat uit het tref woord `function`, gevolgd door het symbool dat de naam van de functie, een getypeerde id-tuple, een type aantekening is die het retour type van de functie beschrijft, en een instructie blok waarmee de implementatie van de functieassembly.</span><span class="sxs-lookup"><span data-stu-id="86312-215">A function declaration consists of the keyword `function`, followed by the symbol that is the function’s name, a typed identifier tuple, a type annotation that describes the function's return type, and a statement block that describes the implementation of the function.</span></span>

<span data-ttu-id="86312-216">Het instructie blok dat een functie definieert, moet zijn Inge sloten in `{` en `}` als een ander instructie blok.</span><span class="sxs-lookup"><span data-stu-id="86312-216">The statement block defining a function must be enclosed in `{` and `}` like any other statement block.</span></span>

<span data-ttu-id="86312-217">Functie namen moeten uniek zijn binnen een naam ruimte en kunnen een conflict veroorzaken met bewerkingen en type namen.</span><span class="sxs-lookup"><span data-stu-id="86312-217">Function names must be unique within a namespace and may not conflict with operation and type names.</span></span>
<span data-ttu-id="86312-218">Functies mogen geen qubits toewijzen of lenen, of aanroepen.</span><span class="sxs-lookup"><span data-stu-id="86312-218">Functions may not allocate or borrow qubits, or call operations.</span></span> <span data-ttu-id="86312-219">Gedeeltelijke toepassing van bewerkingen of het door geven van getypte waarden is nauw keurig.</span><span class="sxs-lookup"><span data-stu-id="86312-219">Partial application of operations or passing around operation typed values is fine.</span></span>

<span data-ttu-id="86312-220">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="86312-220">For example,</span></span>

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```
