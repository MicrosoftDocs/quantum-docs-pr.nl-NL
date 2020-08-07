---
title: Typen inQ#
description: Meer informatie over de verschillende typen die in de Q# programmeer taal worden gebruikt.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: b034af0b1d3b967b5680403341813407e4412f93
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869593"
---
# <a name="types-in-no-locq"></a><span data-ttu-id="556df-103">Typen inQ#</span><span class="sxs-lookup"><span data-stu-id="556df-103">Types in Q#</span></span>

<span data-ttu-id="556df-104">In dit artikel worden het Q# type model en de syntaxis voor het opgeven en werken met typen beschreven.</span><span class="sxs-lookup"><span data-stu-id="556df-104">This article describes the Q# type model and the syntax for specifying and working with types.</span></span> <span data-ttu-id="556df-105">Zie [type expressies](xref:microsoft.quantum.guide.expressions)voor meer informatie over het maken en uitvoeren van expressies van deze typen.</span><span class="sxs-lookup"><span data-stu-id="556df-105">For details on how to create and operate on expressions of these types, see [Type Expressions](xref:microsoft.quantum.guide.expressions).</span></span>

<span data-ttu-id="556df-106">Q#Het is een *sterk getypeerde* taal, zodat het gebruik van deze typen zorgvuldig kan helpen de compiler om sterke garanties te bieden voor Q# Program ma's tijdens het compileren.</span><span class="sxs-lookup"><span data-stu-id="556df-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="556df-107">Om de krach tigste garanties te bieden, moeten conversies tussen typen in Q# expliciet worden aangeroepen met behulp van aanroepen naar functions die deze converteren.</span><span class="sxs-lookup"><span data-stu-id="556df-107">To provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> 
<span data-ttu-id="556df-108">Q#biedt diverse functies als onderdeel van de <xref:microsoft.quantum.convert> naam ruimte.</span><span class="sxs-lookup"><span data-stu-id="556df-108">Q# provides a variety of such functions as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="556df-109">Een upcast naar compatibele typen, anderzijds gebeurt impliciet.</span><span class="sxs-lookup"><span data-stu-id="556df-109">Upcasts to compatible types, on the other hand, happen implicitly.</span></span> 

<span data-ttu-id="556df-110">Q#biedt zowel primitieve typen, die rechtstreeks worden gebruikt, als verschillende manieren om nieuwe typen van andere typen te maken.</span><span class="sxs-lookup"><span data-stu-id="556df-110">Q# provides both primitive types, which are used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="556df-111">We beschrijven elk in de rest van dit artikel.</span><span class="sxs-lookup"><span data-stu-id="556df-111">We describe each in the rest of this article.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="556df-112">Primitieve typen</span><span class="sxs-lookup"><span data-stu-id="556df-112">Primitive Types</span></span>

<span data-ttu-id="556df-113">De Q# taal biedt de volgende *primitieve typen*, die allemaal rechtstreeks in Program ma's kunnen worden gebruikt Q# .</span><span class="sxs-lookup"><span data-stu-id="556df-113">The Q# language provides the following *primitive types*, all of which you can use directly in Q# programs.</span></span> <span data-ttu-id="556df-114">U kunt deze primitieve typen ook gebruiken om nieuwe typen te maken.</span><span class="sxs-lookup"><span data-stu-id="556df-114">You can also use these primitive types to construct new types.</span></span>

- <span data-ttu-id="556df-115">Het `Int` type vertegenwoordigt een 64-bits geheel getal met teken, bijvoorbeeld,, `2` `107` , `-5` .</span><span class="sxs-lookup"><span data-stu-id="556df-115">The `Int` type represents a 64-bit signed integer, for example, `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="556df-116">Het `BigInt` type vertegenwoordigt een ondertekende integer met een wille keurige grootte, bijvoorbeeld,, `2L` `107L` `-5L` .</span><span class="sxs-lookup"><span data-stu-id="556df-116">The `BigInt` type represents a signed integer of arbitrary size, for example, `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="556df-117">Dit type is gebaseerd op .NET<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="556df-117">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="556df-118">voert.</span><span class="sxs-lookup"><span data-stu-id="556df-118">type.</span></span>

- <span data-ttu-id="556df-119">Het `Double` type vertegenwoordigt een drijvende-komma getal met dubbele precisie, bijvoorbeeld, `0.0` , `-1.3` , `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="556df-119">The `Double` type represents a double-precision floating-point number, for example, `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="556df-120">Het `Bool` type vertegenwoordigt een Booleaanse waarde van ofwel `true` of `false` .</span><span class="sxs-lookup"><span data-stu-id="556df-120">The `Bool` type represents a Boolean value of either `true` or `false`.</span></span>
- <span data-ttu-id="556df-121">Het `Range` type vertegenwoordigt een reeks gehele getallen, aangeduid door `start..step..stop` , waarbij de stap optioneel wordt aangeduid.</span><span class="sxs-lookup"><span data-stu-id="556df-121">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="556df-122">Bijvoorbeeld, `start .. stop` correspondeert met `start..1..stop` en `1..2..7` staat voor de reeks $ \{ 1, 3, 5, 7 \} $.</span><span class="sxs-lookup"><span data-stu-id="556df-122">For example, `start .. stop` corresponds to `start..1..stop`, and `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="556df-123">Het `String` type is een opeenvolging van Unicode-tekens die ondoorzichtig is voor de gebruiker nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="556df-123">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="556df-124">Gebruik het `string` type om berichten te rapporteren aan een klassieke host in het geval van een fout of diagnostische gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="556df-124">Use the `string` type to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="556df-125">Het `Unit` type kan slechts één waarde hebben, `()` .</span><span class="sxs-lookup"><span data-stu-id="556df-125">The `Unit` type can have only one value, `()`.</span></span> 
  <span data-ttu-id="556df-126">Gebruik dit type om aan te geven dat Q# er geen gegevens worden geretourneerd door een functie of bewerking.</span><span class="sxs-lookup"><span data-stu-id="556df-126">Use this type to indicate that a Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="556df-127">Het `Qubit` type vertegenwoordigt een Quantum bit of Qubit.</span><span class="sxs-lookup"><span data-stu-id="556df-127">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="556df-128">`Qubit`s ondoorzichtig voor de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="556df-128">`Qubit`s are opaque to the user.</span></span> <span data-ttu-id="556df-129">De enige bewerking die kan worden uitgevoerd, met uitzonde ring van deze aan een andere bewerking door gegeven, is om te testen op identiteit (gelijkheid).</span><span class="sxs-lookup"><span data-stu-id="556df-129">The only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="556df-130">Uiteindelijk implementeert u acties op `Qubit` s door het aanroepen van intrinsieke instructies op een Quantum processor (of een Quantum Simulator).</span><span class="sxs-lookup"><span data-stu-id="556df-130">Ultimately, you implement actions on `Qubit`s by calling intrinsic instructions on a quantum processor (or a quantum simulator).</span></span>
- <span data-ttu-id="556df-131">Het `Pauli` type vertegenwoordigt een van de vier Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="556df-131">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="556df-132">Gebruik dit type om de basis bewerking voor rotaties aan te duiden en het waarneem bare gemeten te bepalen.</span><span class="sxs-lookup"><span data-stu-id="556df-132">Use this type to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="556df-133">Het is een opgesomd type met vier mogelijke waarden: `PauliI` , `PauliX` , `PauliY` , en `PauliZ` , constanten van het type `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="556df-133">It is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="556df-134">Het `Result` type vertegenwoordigt het resultaat van een meting.</span><span class="sxs-lookup"><span data-stu-id="556df-134">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="556df-135">Het is een opgesomd type met twee mogelijke waarden: `One` en `Zero` , die constanten van het type zijn `Result` .</span><span class="sxs-lookup"><span data-stu-id="556df-135">It is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="556df-136">`Zero`geeft aan dat de + 1-eigenvalue is gemeten; `One`geeft aan dat de eigenvalue-1 is gemeten.</span><span class="sxs-lookup"><span data-stu-id="556df-136">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue was measured.</span></span>

<span data-ttu-id="556df-137">De constanten `true` , `false` ,,,,, `PauliI` `PauliX` `PauliY` `PauliZ` `One` en `Zero` zijn alle gereserveerde symbolen in Q# .</span><span class="sxs-lookup"><span data-stu-id="556df-137">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="556df-138">Matrix typen</span><span class="sxs-lookup"><span data-stu-id="556df-138">Array Types</span></span>

* <span data-ttu-id="556df-139">Voor elk geldig Q# type is er een type dat een matrix met waarden van dat type vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="556df-139">For any valid Q# type, there is a type that represents an array of values of that type.</span></span>
    <span data-ttu-id="556df-140">`Qubit[]`En `(Bool, Pauli)[]` vertegenwoordigen bijvoorbeeld matrices van `Qubit` waarden en `(Bool, Pauli)` tuple-waarden.</span><span class="sxs-lookup"><span data-stu-id="556df-140">For example, `Qubit[]` and `(Bool, Pauli)[]` represent arrays of `Qubit` values and `(Bool, Pauli)` tuple values.</span></span>

* <span data-ttu-id="556df-141">Een matrix met matrices is ook geldig.</span><span class="sxs-lookup"><span data-stu-id="556df-141">An array of arrays is also valid.</span></span> <span data-ttu-id="556df-142">Uitvouwen in het vorige voor beeld: er wordt een matrix met `(Bool, Pauli)` matrices aangeduid `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="556df-142">Expanding on the previous example, an array of `(Bool, Pauli)` arrays is denoted `(Bool, Pauli)[][]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="556df-143">Dit voor beeld `(Bool, Pauli)[][]` vertegenwoordigt een mogelijk gekartelde matrix van matrices en geen rechthoekige tweedimensionale matrix.</span><span class="sxs-lookup"><span data-stu-id="556df-143">This example, `(Bool, Pauli)[][]`, represents a potentially jagged array of arrays and not a rectangular two-dimensional array.</span></span> <span data-ttu-id="556df-144">Q#biedt geen ondersteuning voor rechthoekige matrices met meerdere dimensies.</span><span class="sxs-lookup"><span data-stu-id="556df-144">Q# does not support rectangular multi-dimensional arrays.</span></span>

* <span data-ttu-id="556df-145">Een matrix waarde kan worden geschreven in Q# de bron code met behulp van rechte haken rond de elementen van een matrix, zoals in `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="556df-145">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="556df-146">Het algemene basis type van alle items in de matrix bepaalt het type van een matrix letterlijke waarde.</span><span class="sxs-lookup"><span data-stu-id="556df-146">The common base type of all items in the array determines the type of an array literal.</span></span> <span data-ttu-id="556df-147">Het maken van een matrix met elementen die geen gemeen schappelijk basis type hebben, veroorzaakt daarom een fout.</span><span class="sxs-lookup"><span data-stu-id="556df-147">Hence, constructing an array with elements that have no common base type raises an error.</span></span>  
<span data-ttu-id="556df-148">Zie [matrices van callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables)voor een voor beeld.</span><span class="sxs-lookup"><span data-stu-id="556df-148">For an example, see [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span></span>

    > [!WARNING]
    > <span data-ttu-id="556df-149">Nadat de elementen van een matrix zijn gemaakt, kunnen ze niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="556df-149">Once created, the elements of an array cannot be changed.</span></span>
    > <span data-ttu-id="556df-150">Als u een aangepaste matrix wilt maken, gebruikt u de [instructies update-en-reassign](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) of [kopiëren-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="556df-150">To construct a modified array, use [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span>

* <span data-ttu-id="556df-151">U kunt een matrix ook maken op basis van de grootte met behulp van het `new` sleutel woord:</span><span class="sxs-lookup"><span data-stu-id="556df-151">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* <span data-ttu-id="556df-152">Gebruik de functie kern `Length` om het aantal elementen van een matrix als een te verkrijgen `Int` .</span><span class="sxs-lookup"><span data-stu-id="556df-152">Use the core function `Length` to obtain the number of elements from an array as an `Int`.</span></span>
* <span data-ttu-id="556df-153">Matrices kunnen worden ondergeschreven om afzonderlijke elementen of nieuwe matrices te verkrijgen die een subset van de elementen van een matrix bevatten.</span><span class="sxs-lookup"><span data-stu-id="556df-153">Arrays can be subscripted to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="556df-154">De subscripts van matrices zijn gebaseerd op nul en moeten type `Int` of type zijn `Range` :</span><span class="sxs-lookup"><span data-stu-id="556df-154">The subscripts of arrays are zero-based and must be type `Int` or type `Range`:</span></span>

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a><span data-ttu-id="556df-155">Tuple-typen</span><span class="sxs-lookup"><span data-stu-id="556df-155">Tuple Types</span></span>

<span data-ttu-id="556df-156">Tuples zijn een krachtig concept dat door wordt gebruikt Q# voor het verzamelen van waarden in één waarde, waardoor het eenvoudiger wordt om ze te passeren.</span><span class="sxs-lookup"><span data-stu-id="556df-156">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="556df-157">Met name voor het gebruik van de tuple-notatie kunt u zien dat elke bewerking en aanroepable precies één invoer hebben en er precies één uitvoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="556df-157">In particular, using tuple notation, you can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

* <span data-ttu-id="556df-158">Als er geen of meer verschillende typen `T0` , `T1` ,..., worden opgegeven, `Tn` kunt u een nieuw *tuple-type* aanduiden als `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="556df-158">Given zero or more different types `T0`, `T1`, ..., `Tn`, you can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="556df-159">De typen die worden gebruikt voor het maken van een nieuw tuple-type kunnen Tuples zijn, zoals in `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="556df-159">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="556df-160">Deze geneste is altijd eindig, maar aangezien tuple-typen niet in elke situatie zichzelf kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="556df-160">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

* <span data-ttu-id="556df-161">De waarden van het nieuwe tuple-type zijn Tuples die worden gevormd door reeksen waarden van elk type in de tuple.</span><span class="sxs-lookup"><span data-stu-id="556df-161">The values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="556df-162">`(3, false)`Is bijvoorbeeld een tuple waarvan het type het type tuple is `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="556df-162">For example, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="556df-163">Het is mogelijk om matrices met Tuples, Tuples van matrices, Tuples van sub-Tuples, enzovoort te maken.</span><span class="sxs-lookup"><span data-stu-id="556df-163">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, and so on.</span></span>

* <span data-ttu-id="556df-164">Vanaf Q# 0,3, `Unit` is de naam van het *type* van de lege tuple; `()` wordt gebruikt voor de *waarde* van de lege tuple.</span><span class="sxs-lookup"><span data-stu-id="556df-164">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the *value* of the empty tuple.</span></span>

* <span data-ttu-id="556df-165">Tuple-instanties zijn onveranderbaar.</span><span class="sxs-lookup"><span data-stu-id="556df-165">Tuple instances are immutable.</span></span>
<span data-ttu-id="556df-166">Q#biedt geen mechanisme om de inhoud van een tuple te wijzigen nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="556df-166">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>



### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="556df-167">Singleton-tuple-equivalentie</span><span class="sxs-lookup"><span data-stu-id="556df-167">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="556df-168">Het is mogelijk om een singleton-tuple (één element) `('T1)` te maken, zoals `(5)` of `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="556df-168">It is possible to create a singleton (single-element) tuple `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="556df-169">Behandelt echter Q# een singleton-tuple als equivalent aan een waarde van het Inge sloten type.</span><span class="sxs-lookup"><span data-stu-id="556df-169">However, Q# treats a singleton tuple as equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="556df-170">Dat wil zeggen dat er geen verschil is tussen en `5` `(5)` , of tussen en of tussen en `5` `(((5)))` `(5, (6))` `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="556df-170">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="556df-171">Het is net zo geldig als het schrijven van een `(5)+3` Schrijf bewerking `5+3` ; beide expressies evalueren naar `8` .</span><span class="sxs-lookup"><span data-stu-id="556df-171">It is just as valid to write `(5)+3` as it is to write `5+3`; both expressions evaluate to `8`.</span></span>

<span data-ttu-id="556df-172">Deze gelijkwaardigheid geldt voor alle doel einden, inclusief toewijzing en expressies.</span><span class="sxs-lookup"><span data-stu-id="556df-172">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="556df-173">Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.</span><span class="sxs-lookup"><span data-stu-id="556df-173">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="556df-174">`(7)`Is bijvoorbeeld een expressie van het type `Int` , `([1,2,3])` is een expressie van het type `Int[]` en `((1,2))` is een expressie van het type `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="556df-174">For example, `(7)` is an expression of type `Int`, `([1,2,3])` is an expression of type `Int[]`, and `((1,2))` is an expression of type `(Int, Int)`.</span></span>

<span data-ttu-id="556df-175">Dit betekent met name dat u een bewerking of functie kunt bekijken waarvan het type tuple of uitvoer tuple één veld heeft om één argument te maken of een enkele waarde te retour neren.</span><span class="sxs-lookup"><span data-stu-id="556df-175">In particular, this means that you can view an operation or function whose input tuple or output tuple type has one field as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="556df-176">We verwijzen naar deze eigenschap als _Singleton-tuple-equivalentie_.</span><span class="sxs-lookup"><span data-stu-id="556df-176">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="556df-177">Door de gebruiker gedefinieerde typen</span><span class="sxs-lookup"><span data-stu-id="556df-177">User-Defined Types</span></span>

<span data-ttu-id="556df-178">Een door de gebruiker gedefinieerde type declaratie bestaat uit het tref woord `newtype` , gevolgd door de naam van het door de gebruiker gedefinieerde type, een `=` , een geldige type specificatie en een afsluitende punt komma.</span><span class="sxs-lookup"><span data-stu-id="556df-178">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="556df-179">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="556df-179">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* <span data-ttu-id="556df-180">Elk Q# bron bestand kan een wille keurig aantal door de gebruiker gedefinieerde typen declareren.</span><span class="sxs-lookup"><span data-stu-id="556df-180">Each Q# source file may declare any number of user-defined types.</span></span>
* <span data-ttu-id="556df-181">Type namen moeten uniek zijn binnen een naam ruimte en kunnen geen conflict veroorzaken met de namen van bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="556df-181">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>
* <span data-ttu-id="556df-182">Door de gebruiker gedefinieerde typen zijn verschillend, zelfs als de basis typen identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="556df-182">User-defined types are distinct, even if the base types are identical.</span></span>
<span data-ttu-id="556df-183">In het bijzonder is er geen automatische conversie tussen de waarden van twee door de gebruiker gedefinieerde typen, zelfs als de onderliggende typen identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="556df-183">In particular, there is no automatic conversion between the values of two user-defined types, even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="556df-184">Benoemde versus anonieme items</span><span class="sxs-lookup"><span data-stu-id="556df-184">Named vs. anonymous items</span></span>

<span data-ttu-id="556df-185">Een Q# bestand kan een nieuw benoemd type definiëren dat één waarde van elk juridisch type bevat.</span><span class="sxs-lookup"><span data-stu-id="556df-185">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="556df-186">Voor elk type tuple `T` kunt u een nieuw door de gebruiker gedefinieerd type declareren dat een subtype is van `T` met de `newtype` instructie.</span><span class="sxs-lookup"><span data-stu-id="556df-186">For any tuple type `T`, you can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="556df-187">In de @"microsoft.quantum.math" naam ruimte worden bijvoorbeeld complexe getallen gedefinieerd als een door de gebruiker gedefinieerd type:</span><span class="sxs-lookup"><span data-stu-id="556df-187">In the @"microsoft.quantum.math" namespace, for example, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="556df-188">Met deze instructie maakt u een nieuw type met twee anonieme items van het type `Double` .</span><span class="sxs-lookup"><span data-stu-id="556df-188">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="556df-189">Door de gebruiker gedefinieerde typen bieden ook ondersteuning voor *benoemde items* van anonieme items, vanaf Q# versie 0,7 of hoger.</span><span class="sxs-lookup"><span data-stu-id="556df-189">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="556df-190">U kunt bijvoorbeeld de items een naam geven `Re` voor de dubbele waarde van het werkelijke deel van een complex getal en `Im` voor het imaginaire deel:</span><span class="sxs-lookup"><span data-stu-id="556df-190">For example, you could name the items to `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="556df-191">De naam van een item in een door de gebruiker gedefinieerd type betekent niet dat alle items moeten worden benoemd: elke combi natie van benoemde en niet-benoemde items wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="556df-191">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="556df-192">Daarnaast kunnen interne items ook een naam hebben.</span><span class="sxs-lookup"><span data-stu-id="556df-192">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="556df-193">Het type `Nested` , zoals hieronder gedefinieerd, heeft bijvoorbeeld een onderliggend type `(Double, (Int, String))` , waarvan alleen het item van het type de `Int` naam heeft en alle andere items anoniem zijn.</span><span class="sxs-lookup"><span data-stu-id="556df-193">The type `Nested`, as defined below for example, has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named, and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="556df-194">Benoemde items hebben het voor deel dat ze rechtstreeks kunnen worden geopend via de *toegangs operator* `::` .</span><span class="sxs-lookup"><span data-stu-id="556df-194">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="556df-195">Naast het bieden van korte aliassen voor mogelijk gecompliceerde tuple-typen, is een belang rijk voor deel van het definiëren van dergelijke typen dat ze de bedoeling van een bepaalde waarde kunnen documenteren.</span><span class="sxs-lookup"><span data-stu-id="556df-195">In addition to providing short aliases for potentially complicated tuple types, a significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="556df-196">Als u terugkeert naar het voor beeld van `Complex` , kunt u een 2D polaire coördinaten ook als een door de gebruiker gedefinieerd type hebben gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="556df-196">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="556df-197">Hoewel beide `Complex` en `Polar` beide een onderliggend type hebben `(Double, Double)` , zijn de twee typen volledig incompatibel in Q# , waarmee het risico wordt geminimaliseerd dat per ongeluk een complexe wiskundige functie aanroept met polaire coördinaten en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="556df-197">Even though both `Complex` and `Polar` both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="556df-198">Toegang tot anonieme items met de operator voor uitpakken</span><span class="sxs-lookup"><span data-stu-id="556df-198">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="556df-199">Als u toegang wilt krijgen tot anonieme items, moet u eerst de ingepakte waarde ophalen met de operator achtervoegsel `!` .</span><span class="sxs-lookup"><span data-stu-id="556df-199">To access anonymous items, first extract the wrapped value using the postfix operator `!`.</span></span>
<span data-ttu-id="556df-200">Met de operator ' uitpakken ' `!` kunt u de waarde die is opgenomen in een door de gebruiker gedefinieerd type extra heren.</span><span class="sxs-lookup"><span data-stu-id="556df-200">With the "unwrap" operator, `!`, you can extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="556df-201">Het type van een dergelijke expressie voor ' uitpakken ' is het onderliggende type van het door de gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="556df-201">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="556df-202">Eén regel voor uitpakken van de operator deloopt één laag terugloop.</span><span class="sxs-lookup"><span data-stu-id="556df-202">A single unwrap operator unwraps one layer of wrapping.</span></span> <span data-ttu-id="556df-203">Meerdere opera tors voor uitpakken gebruiken om toegang te krijgen tot een waarde met vermenigvuldiging.</span><span class="sxs-lookup"><span data-stu-id="556df-203">Use multiple unwrap operators to access a multiply-wrapped value.</span></span>

<span data-ttu-id="556df-204">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="556df-204">For example:</span></span>

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

<span data-ttu-id="556df-205">Zie [type expressies in Q# ](xref:microsoft.quantum.guide.expressions)voor meer informatie over de operator voor uitpakken.</span><span class="sxs-lookup"><span data-stu-id="556df-205">For more details on the unwrap operator, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="556df-206">Waarden maken van door de gebruiker gedefinieerde typen</span><span class="sxs-lookup"><span data-stu-id="556df-206">Creating values of user-defined types</span></span>

<span data-ttu-id="556df-207">Maak waarden van een door de gebruiker gedefinieerd type door de bijbehorende type-constructor aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="556df-207">Create values of a user-defined type by calling the corresponding type constructor:</span></span>

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="556df-208">U kunt ook nieuwe waarden maken op basis van een bestaande waarde met behulp van [Copy-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="556df-208">Alternatively, you can create new values from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="556df-209">Net zoals bij matrices, kopiëren-en-update-expressies worden alle item waarden van de oorspronkelijke expressie gekopieerd, met uitzonde ring van de opgegeven benoemde items.</span><span class="sxs-lookup"><span data-stu-id="556df-209">Just as they do with arrays, copy-and-update expressions copy all item values of the original expression, except for the specified named items.</span></span> <span data-ttu-id="556df-210">Voor deze uitzonde ringen zijn de waarden van deze items de waarden die aan de rechter kant van de expressie zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="556df-210">For these exceptions, the values of these items are the values defined on the right-hand side of the expression.</span></span> <span data-ttu-id="556df-211">Alle andere taal constructies die beschikbaar zijn voor matrix items, zoals [instructies update en opnieuw toewijzen](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), bestaan ook uit benoemde items in door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="556df-211">Any other language constructs that are available for array items, for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), exist for named-items in user-defined types as well.</span></span>

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

* <span data-ttu-id="556df-212">U kunt door de gebruiker gedefinieerde typen overal gebruiken waar u andere typen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="556df-212">You can use user-defined types anywhere you use any other types.</span></span>
<span data-ttu-id="556df-213">Het is met name mogelijk een matrix van een door de gebruiker gedefinieerd type te definiëren en een door de gebruiker gedefinieerd type op te geven als element van een tuple-type.</span><span class="sxs-lookup"><span data-stu-id="556df-213">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

* <span data-ttu-id="556df-214">Het is niet mogelijk om recursieve type structuren te maken.</span><span class="sxs-lookup"><span data-stu-id="556df-214">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="556df-215">Dat wil zeggen, het type dat een door de gebruiker gedefinieerd type definieert, kan geen tuple-type zijn dat een element van het door de gebruiker gedefinieerde type bevat.</span><span class="sxs-lookup"><span data-stu-id="556df-215">That is, the type that defines a user-defined type cannot be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="556df-216">Meer in het algemeen zijn door de gebruiker gedefinieerde typen mogelijk geen cyclische afhankelijkheden van elkaar, waardoor de volgende sets type definities ongeldig zijn:</span><span class="sxs-lookup"><span data-stu-id="556df-216">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions are invalid:</span></span>

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a><span data-ttu-id="556df-217">Bewerkings-en functie typen</span><span class="sxs-lookup"><span data-stu-id="556df-217">Operation and Function Types</span></span>

<span data-ttu-id="556df-218">Op basis van de typen `'Tinput` en `'Tresult` :</span><span class="sxs-lookup"><span data-stu-id="556df-218">Given the types `'Tinput` and `'Tresult`:</span></span>

* <span data-ttu-id="556df-219">`('Tinput => 'Tresult)`is het basis type voor een wille keurige *bewerking*, bijvoorbeeld `((Qubit, Pauli) => Result)` .</span><span class="sxs-lookup"><span data-stu-id="556df-219">`('Tinput => 'Tresult)` is the basic type for any *operation*, for example `((Qubit, Pauli) => Result)`.</span></span>
* <span data-ttu-id="556df-220">`('Tinput -> 'Tresult)`is het basis type voor een *functie*, bijvoorbeeld `(Int -> Int)` .</span><span class="sxs-lookup"><span data-stu-id="556df-220">`('Tinput -> 'Tresult)` is the basic type for any *function*, for example `(Int -> Int)`.</span></span> 

<span data-ttu-id="556df-221">Deze worden de *hand tekening* van de aanroepable genoemd.</span><span class="sxs-lookup"><span data-stu-id="556df-221">These are called the *signature* of the callable.</span></span>

* <span data-ttu-id="556df-222">Alle Q# callables nemen één waarde als invoer en retour neren één waarde als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="556df-222">All Q# callables take a single value as input and return a single value as output.</span></span>
* <span data-ttu-id="556df-223">U kunt Tuples gebruiken voor zowel de invoer-als uitvoer waarden.</span><span class="sxs-lookup"><span data-stu-id="556df-223">You can use tuples for both the input and output values.</span></span>
* <span data-ttu-id="556df-224">Callables die geen resultaat hebben, retour neren `Unit` .</span><span class="sxs-lookup"><span data-stu-id="556df-224">Callables that have no result, return `Unit`.</span></span>
* <span data-ttu-id="556df-225">Callables die geen invoer hebben, hebben de lege tuple als invoer.</span><span class="sxs-lookup"><span data-stu-id="556df-225">Callables that have no input take the empty tuple as input.</span></span>

### <a name="functors"></a><span data-ttu-id="556df-226">Functors</span><span class="sxs-lookup"><span data-stu-id="556df-226">Functors</span></span>

<span data-ttu-id="556df-227">*Functie* typen zijn volledig opgegeven met hun hand tekening.</span><span class="sxs-lookup"><span data-stu-id="556df-227">*Function* types are completely specified by their signature.</span></span> <span data-ttu-id="556df-228">Een functie die bijvoorbeeld de sinus van een hoek berekent, zou type hebben `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="556df-228">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span> 

<span data-ttu-id="556df-229">*Bewerkingen* hebben bepaalde extra kenmerken die worden weer gegeven als onderdeel van het bewerkings type.</span><span class="sxs-lookup"><span data-stu-id="556df-229">*Operations* have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="556df-230">Dergelijke kenmerken bevatten informatie over welke *functors* de bewerking ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="556df-230">Such characteristics include information about which *functors* the operation supports.</span></span>
<span data-ttu-id="556df-231">Als de uitvoering van de bewerking bijvoorbeeld afhankelijk is van de status van andere qubits, moet de functor worden ondersteund `Controlled` . als de bewerking een omgekeerde waarde heeft, moet de functor worden ondersteund `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="556df-231">For example, if the execution of the operation relies on the state of other qubits, then it should support the `Controlled` functor; if the operation has an inverse, then it should support the `Adjoint` functor.</span></span>

> [!NOTE]
> <span data-ttu-id="556df-232">In dit artikel wordt alleen besproken hoe functors de hand tekening van de bewerking wijzigt.</span><span class="sxs-lookup"><span data-stu-id="556df-232">This article only discuss how functors alter the operation signature.</span></span> <span data-ttu-id="556df-233">Zie [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions)voor meer informatie over functors en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="556df-233">For more details about functors and operations, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span> 

<span data-ttu-id="556df-234">Om ondersteuning voor de `Controlled` and/of `Adjoint` functor in een bewerkings type te vereisen, moet u een aantekening toevoegen die de bijbehorende kenmerken aangeeft.</span><span class="sxs-lookup"><span data-stu-id="556df-234">To require support for the `Controlled` and/or `Adjoint` functor in an operation type, you need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="556df-235">De aantekening `is Ctl` (bijvoorbeeld `(Qubit => Unit is Ctl)` ) geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="556df-235">The annotation `is Ctl` (for example, `(Qubit => Unit is Ctl)`) indicates that the operation is controllable.</span></span> <span data-ttu-id="556df-236">Dat wil zeggen dat de uitvoering afhankelijk is van de status van een andere Qubit of qubits.</span><span class="sxs-lookup"><span data-stu-id="556df-236">That is, its execution relies on the state of another qubit or qubits.</span></span> <span data-ttu-id="556df-237">Op dezelfde manier wordt met de aantekening `is Adj` aangegeven dat de bewerking een adjoint heeft, dat wil zeggen, dat wil zeggen ' omgekeerd ', waardoor een bewerking herhaaldelijk wordt toegepast en de adjoint op een status de status ongewijzigd laat.</span><span class="sxs-lookup"><span data-stu-id="556df-237">Similarly, the annotation `is Adj` indicates that the operation has an adjoint, that is, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="556df-238">Als u wilt vereisen dat een bewerking van dat Type zowel de als de `Adjoint` `Controlled` functor ondersteunt, kunt u dit als volgt uitdrukken `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="556df-238">If you want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor you can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="556df-239">De ingebouwde bewerking Pauli is bijvoorbeeld van het <xref:microsoft.quantum.intrinsic.x> type `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="556df-239">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="556df-240">Een bewerkings type dat geen functors ondersteunt, wordt opgegeven door het invoer-en uitvoer type alleen, zonder extra aantekening.</span><span class="sxs-lookup"><span data-stu-id="556df-240">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="556df-241">Functies en bewerkingen van het type para meters</span><span class="sxs-lookup"><span data-stu-id="556df-241">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="556df-242">Aanroep bare typen kunnen *type parameters*bevatten.</span><span class="sxs-lookup"><span data-stu-id="556df-242">Callable types may contain *type parameters*.</span></span>
<span data-ttu-id="556df-243">Gebruik een symbool dat wordt voorafgegaan door één aanhalings teken om een type parameter te vermelden. `'A`is bijvoorbeeld een geldige type parameter.</span><span class="sxs-lookup"><span data-stu-id="556df-243">Use a symbol prefixed by a single quote to indicated a type parameter; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="556df-244">Zie [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)voor meer informatie en informatie over het definiëren van type parameters callables.</span><span class="sxs-lookup"><span data-stu-id="556df-244">For more information and details on how to define type-parameterized callables, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span></span>

<span data-ttu-id="556df-245">Een type parameter kan meermaals voor komen in één hand tekening.</span><span class="sxs-lookup"><span data-stu-id="556df-245">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="556df-246">Een functie waarmee een andere functie wordt toegepast op elk element van een matrix en die de verzamelde resultaten retourneert, heeft bijvoorbeeld de hand tekening `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="556df-246">For example, a function that applies another function to each element of an array and returns the collected results has the signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="556df-247">Op dezelfde manier heeft een functie die de samen stelling van twee bewerkingen retourneert, de hand tekening `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="556df-247">Similarly, a function that returns the composition of two operations has the signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="556df-248">Wanneer u een aanroepable van het type para meter aanroept, moeten alle argumenten met dezelfde type parameter van hetzelfde type zijn.</span><span class="sxs-lookup"><span data-stu-id="556df-248">When you invoke a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="556df-249">Q#biedt geen methode voor het beperken van de mogelijke typen die een gebruiker kan vervangen door een type parameter.</span><span class="sxs-lookup"><span data-stu-id="556df-249">Q# does not provide a mechanism for constraining the possible types that a user might substitute for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="556df-250">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="556df-250">Next steps</span></span>

<span data-ttu-id="556df-251">Nu u alle typen hebt gezien die de Q# taal vormen, Zie [ Q# expressies typen in](xref:microsoft.quantum.guide.expressions) voor meer informatie over het maken en bewerken van expressies van deze verschillende typen.</span><span class="sxs-lookup"><span data-stu-id="556df-251">Now that you've seen all the types which comprise the Q# language, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to learn how to create and manipulate expressions of these various types.</span></span>
