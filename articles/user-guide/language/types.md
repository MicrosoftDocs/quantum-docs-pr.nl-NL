---
title: Typen in Q#
description: 'Meer informatie over de verschillende typen die worden gebruikt in de Q #-programmeer taal.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: f7a3ac3813966c0ef695068297ce4d9949ead554
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327285"
---
# <a name="types-in-q"></a><span data-ttu-id="fe660-103">Typen in Q#</span><span class="sxs-lookup"><span data-stu-id="fe660-103">Types in Q#</span></span>

<span data-ttu-id="fe660-104">Op deze pagina wordt het type Q # vermeld en wordt de syntaxis voor het opgeven en werken met typen beschreven.</span><span class="sxs-lookup"><span data-stu-id="fe660-104">This page lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="fe660-105">Op de volgende pagina [typt u expressies](xref:microsoft.quantum.guide.expressions), informatie over het maken en bewerken van expressies van deze typen.</span><span class="sxs-lookup"><span data-stu-id="fe660-105">The next page, [Type Expressions](xref:microsoft.quantum.guide.expressions), details how to create and operate on expressions of these types.</span></span>

<span data-ttu-id="fe660-106">Houd er rekening mee dat Q # een *sterk getypeerde* taal is, zodat het gebruik van deze typen zorgvuldig kan bijdragen aan de compiler om sterke garanties te bieden voor Q #-Program ma's tijdens het compileren.</span><span class="sxs-lookup"><span data-stu-id="fe660-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="fe660-107">Om de krach tigste garanties te bieden, moeten conversies tussen typen in Q # expliciet worden gebruikt voor het gebruik van aanroepen van functies die de conversie door lopen.</span><span class="sxs-lookup"><span data-stu-id="fe660-107">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="fe660-108">Er zijn verschillende functies die deel uitmaken van de <xref:microsoft.quantum.convert> naam ruimte.</span><span class="sxs-lookup"><span data-stu-id="fe660-108">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="fe660-109">Er wordt impliciet een conversie naar compatibele typen uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fe660-109">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="fe660-110">Q # bevat beide primitieve typen, die rechtstreeks kunnen worden gebruikt en een aantal manieren om nieuwe typen van andere typen te maken.</span><span class="sxs-lookup"><span data-stu-id="fe660-110">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="fe660-111">We beschrijven elk in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="fe660-111">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="fe660-112">Primitieve typen</span><span class="sxs-lookup"><span data-stu-id="fe660-112">Primitive Types</span></span>

<span data-ttu-id="fe660-113">De Q #-taal biedt verschillende *primitieve typen*, waaruit andere typen kunnen worden samengesteld:</span><span class="sxs-lookup"><span data-stu-id="fe660-113">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="fe660-114">Het `Int` type vertegenwoordigt een 64-bits geheel getal met teken, bijvoorbeeld: `2` , `107` , `-5` .</span><span class="sxs-lookup"><span data-stu-id="fe660-114">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="fe660-115">Het `BigInt` type vertegenwoordigt een ondertekende integer met een wille keurige grootte, bijvoorbeeld `2L` ,, `107L` `-5L` .</span><span class="sxs-lookup"><span data-stu-id="fe660-115">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="fe660-116">Dit type is gebaseerd op .NET<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="fe660-116">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="fe660-117">voert.</span><span class="sxs-lookup"><span data-stu-id="fe660-117">type.</span></span>
- <span data-ttu-id="fe660-118">Het `Double` type vertegenwoordigt een drijvende-komma getal met dubbele precisie, bijvoorbeeld: `0.0` , `-1.3` , `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="fe660-118">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="fe660-119">Het `Bool` type vertegenwoordigt een Booleaanse waarde die kan of zijn `true` `false` .</span><span class="sxs-lookup"><span data-stu-id="fe660-119">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="fe660-120">Het `Range` type vertegenwoordigt een reeks gehele getallen, aangeduid door `start..step..stop` , waarbij de stap optioneel wordt aangeduid.</span><span class="sxs-lookup"><span data-stu-id="fe660-120">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="fe660-121">Dit `start .. stop` komt overeen met `start..1..stop` , en geeft bijvoorbeeld `1..2..7` de reeks $ \{ 1, 3, 5, 7 \} $ aan.</span><span class="sxs-lookup"><span data-stu-id="fe660-121">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="fe660-122">Het `String` type is een opeenvolging van Unicode-tekens die ondoorzichtig is voor de gebruiker nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fe660-122">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="fe660-123">Dit type wordt gebruikt om berichten te rapporteren aan een klassieke host in het geval van een fout of diagnostische gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="fe660-123">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="fe660-124">Het `Unit` type is het type waarmee slechts één waarde is toegestaan `()` .</span><span class="sxs-lookup"><span data-stu-id="fe660-124">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="fe660-125">Dit type wordt gebruikt om aan te geven dat de functie van Q # of de bewerking geen informatie retourneert.</span><span class="sxs-lookup"><span data-stu-id="fe660-125">This type is used to indicate that Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="fe660-126">Het `Qubit` type vertegenwoordigt een Quantum bit of Qubit.</span><span class="sxs-lookup"><span data-stu-id="fe660-126">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="fe660-127">`Qubit`s ondoorzichtig voor de gebruiker; de enige bewerking die kan worden uitgevoerd, met uitzonde ring van deze aan een andere bewerking door gegeven, is om te testen op identiteit (gelijkheid).</span><span class="sxs-lookup"><span data-stu-id="fe660-127">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="fe660-128">Uiteindelijk worden acties op `Qubit` s geïmplementeerd door het aanroepen van intrinsieke instructies op een Quantum processor (of een simulatie daarvan).</span><span class="sxs-lookup"><span data-stu-id="fe660-128">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="fe660-129">Het `Pauli` type vertegenwoordigt een van de vier Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="fe660-129">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="fe660-130">Dit type wordt gebruikt voor het aanduiden van de basis bewerking voor rotaties en het bepalen van het waarneem bare gemeten.</span><span class="sxs-lookup"><span data-stu-id="fe660-130">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="fe660-131">Dit is een opgesomd type met vier mogelijke waarden: `PauliI` , `PauliX` , `PauliY` , en `PauliZ` , constanten van het type `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="fe660-131">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="fe660-132">Het `Result` type vertegenwoordigt het resultaat van een meting.</span><span class="sxs-lookup"><span data-stu-id="fe660-132">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="fe660-133">Dit is een opgesomd type met twee mogelijke waarden: `One` en `Zero` , die constanten van het type zijn `Result` .</span><span class="sxs-lookup"><span data-stu-id="fe660-133">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="fe660-134">`Zero`geeft aan dat de + 1-eigenvalue is gemeten; `One`Hiermee wordt de-1-eigenvalue aangegeven.</span><span class="sxs-lookup"><span data-stu-id="fe660-134">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>

<span data-ttu-id="fe660-135">De constanten,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` en `Zero` zijn alle gereserveerde symbolen in Q #.</span><span class="sxs-lookup"><span data-stu-id="fe660-135">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="fe660-136">Matrix typen</span><span class="sxs-lookup"><span data-stu-id="fe660-136">Array Types</span></span>

<span data-ttu-id="fe660-137">Als er een geldig Q # `'T` -type is opgegeven, is er een type dat een matrix met waarden van het type vertegenwoordigt `'T` .</span><span class="sxs-lookup"><span data-stu-id="fe660-137">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="fe660-138">Dit matrix type wordt weer gegeven als `'T[]` , bijvoorbeeld `Qubit[]` of `Int[][]` .</span><span class="sxs-lookup"><span data-stu-id="fe660-138">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="fe660-139">Zo wordt bijvoorbeeld een verzameling met gehele getallen aangegeven `Int[]` , terwijl een matrix met `(Bool, Pauli)` waarden wordt aangeduid als matrix `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="fe660-139">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="fe660-140">In het tweede voor beeld ziet u dat dit een mogelijk gekartelde matrix van matrices is en niet een rechthoekige tweedimensionale matrix.</span><span class="sxs-lookup"><span data-stu-id="fe660-140">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="fe660-141">Q # biedt geen ondersteuning voor rechthoekige matrices met meerdere dimensies.</span><span class="sxs-lookup"><span data-stu-id="fe660-141">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="fe660-142">Een matrix waarde kan worden geschreven in Q #-bron code met behulp van rechte haken rond de elementen van een matrix, zoals in `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="fe660-142">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="fe660-143">Het type van een matrix letterlijke waarde wordt bepaald door het algemene basis type van alle items in de matrix.</span><span class="sxs-lookup"><span data-stu-id="fe660-143">The type of an array literal is determined by the common base type of all items in the array.</span></span> <span data-ttu-id="fe660-144">Wanneer u probeert een matrix te maken met elementen die geen gemeen schappelijk basis type hebben, wordt er een fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="fe660-144">Hence trying to construct an array with elements that have no common base type will raise an error.</span></span>  
<span data-ttu-id="fe660-145">Zie [matrices van callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables) voor een voor beeld hiervan.</span><span class="sxs-lookup"><span data-stu-id="fe660-145">See [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables) for an example of this.</span></span>

> [!WARNING]
> <span data-ttu-id="fe660-146">De elementen van een matrix kunnen niet worden gewijzigd nadat de matrix is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fe660-146">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="fe660-147">[Instructies update-en-reassign](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) en/of [Copy-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) kunnen worden gebruikt om een gewijzigde matrix te maken.</span><span class="sxs-lookup"><span data-stu-id="fe660-147">[Update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) and/or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) can be used to construct a modified array.</span></span>

<span data-ttu-id="fe660-148">U kunt een matrix ook maken op basis van de grootte met behulp van het `new` sleutel woord:</span><span class="sxs-lookup"><span data-stu-id="fe660-148">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="fe660-149">In beide gevallen kan de functie kern, wanneer een matrix is samengesteld, `Length` worden gebruikt om het aantal elementen als een te verkrijgen `Int` .</span><span class="sxs-lookup"><span data-stu-id="fe660-149">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="fe660-150">Matrices kunnen worden ondergeschreven met behulp van vier Kante haken, waarbij subscripts van `Int` het type of type `Range` zijn, om afzonderlijke elementen of nieuwe matrices te verkrijgen die een subset van de elementen van een matrix bevatten.</span><span class="sxs-lookup"><span data-stu-id="fe660-150">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="fe660-151">De subscripts van matrices zijn gebaseerd op nul:</span><span class="sxs-lookup"><span data-stu-id="fe660-151">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="fe660-152">Tuple-typen</span><span class="sxs-lookup"><span data-stu-id="fe660-152">Tuple Types</span></span>

<span data-ttu-id="fe660-153">Nul of meer verschillende typen `T0` , `T1` ,..., `Tn` kunnen we een nieuw tuple- *type* aanduiden als `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-153">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="fe660-154">De typen die worden gebruikt voor het maken van een nieuw tuple-type kunnen Tuples zijn, zoals in `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="fe660-154">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="fe660-155">Deze geneste is altijd eindig, maar aangezien tuple-typen niet in elke situatie zichzelf kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="fe660-155">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="fe660-156">Waarden van het nieuwe tuple-type zijn Tuples die worden gevormd door reeksen waarden van elk type in de tuple.</span><span class="sxs-lookup"><span data-stu-id="fe660-156">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="fe660-157">Bijvoorbeeld: `(3, false)` is een tuple waarvan het type het tuple-type is `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-157">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="fe660-158">Het is mogelijk om matrices met Tuples, Tuples van matrices, Tuples van sub-Tuples, enzovoort te maken.</span><span class="sxs-lookup"><span data-stu-id="fe660-158">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="fe660-159">Vanaf Q # 0,3 `Unit` is de naam van het *type* van de lege tuple; `()` wordt gebruikt voor de lege tuple- *waarde*.</span><span class="sxs-lookup"><span data-stu-id="fe660-159">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="fe660-160">Tuple-instanties zijn onveranderbaar.</span><span class="sxs-lookup"><span data-stu-id="fe660-160">Tuple instances are immutable.</span></span>
<span data-ttu-id="fe660-161">Q # biedt geen mechanisme om de inhoud van een tuple te wijzigen nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fe660-161">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="fe660-162">Tuples zijn een krachtig concept dat gedurende Q # wordt gebruikt voor het verzamelen van waarden in één waarde, waardoor het eenvoudiger wordt om ze te passeren.</span><span class="sxs-lookup"><span data-stu-id="fe660-162">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="fe660-163">Met name voor het gebruik van de tuple-notatie kunnen we uitdrukken dat elke bewerking en aanroepbaar precies één invoer hebben en er precies één uitvoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="fe660-163">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="fe660-164">Singleton-tuple-equivalentie</span><span class="sxs-lookup"><span data-stu-id="fe660-164">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="fe660-165">Het is mogelijk om een singleton-tuple (één element) te maken, `('T1)` zoals `(5)` of `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="fe660-165">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="fe660-166">Q # behandelt echter een singleton-tuple als volledig gelijk aan een waarde van het Inge sloten type.</span><span class="sxs-lookup"><span data-stu-id="fe660-166">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="fe660-167">Dat wil zeggen dat er geen verschil is tussen en `5` `(5)` , of tussen en of tussen en `5` `(((5)))` `(5, (6))` `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-167">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="fe660-168">Het is net zo geldig als write `(5)+3` als schrijven `5+3` en beide expressies evalueren naar `8` .</span><span class="sxs-lookup"><span data-stu-id="fe660-168">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>

<span data-ttu-id="fe660-169">Deze gelijkwaardigheid geldt voor alle doel einden, inclusief toewijzing en expressies.</span><span class="sxs-lookup"><span data-stu-id="fe660-169">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="fe660-170">Op basis van een expressie is dezelfde expressie die tussen haakjes staat, een expressie van hetzelfde type.</span><span class="sxs-lookup"><span data-stu-id="fe660-170">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="fe660-171">Bijvoorbeeld: `(7)` is een `Int` expressie, `([1,2,3])` is een expressie van het type matrix van `Int` s en `((1,2))` is een expressie van het type `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-171">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="fe660-172">Dit betekent met name dat een bewerking of functie waarvan het type tuple of uitvoer tuple één veld heeft, kan worden beschouwd als het nemen van één argument of het retour neren van een enkele waarde.</span><span class="sxs-lookup"><span data-stu-id="fe660-172">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="fe660-173">We verwijzen naar deze eigenschap als _Singleton-tuple-equivalentie_.</span><span class="sxs-lookup"><span data-stu-id="fe660-173">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="fe660-174">Door de gebruiker gedefinieerde typen</span><span class="sxs-lookup"><span data-stu-id="fe660-174">User-Defined Types</span></span>

<span data-ttu-id="fe660-175">Een door de gebruiker gedefinieerde type declaratie bestaat uit het tref woord `newtype` , gevolgd door de naam van het door de gebruiker gedefinieerde type, een `=` , een geldige type specificatie en een afsluitende punt komma.</span><span class="sxs-lookup"><span data-stu-id="fe660-175">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="fe660-176">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="fe660-176">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="fe660-177">Elk Q #-bron bestand kan elk gewenst aantal door de gebruiker gedefinieerde typen declareren.</span><span class="sxs-lookup"><span data-stu-id="fe660-177">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="fe660-178">Type namen moeten uniek zijn binnen een naam ruimte en kunnen geen conflict veroorzaken met de namen van bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="fe660-178">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="fe660-179">Door de gebruiker gedefinieerde typen zijn verschillend, zelfs als de basis typen identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="fe660-179">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="fe660-180">In het bijzonder is er geen automatische conversie tussen waarden van twee door de gebruiker gedefinieerde typen, zelfs als de onderliggende typen identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="fe660-180">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="fe660-181">Benoemde versus anonieme items</span><span class="sxs-lookup"><span data-stu-id="fe660-181">Named vs. anonymous items</span></span>

<span data-ttu-id="fe660-182">Een Q #-bestand kan een nieuw benoemd type definiëren dat één waarde van elk juridisch type bevat.</span><span class="sxs-lookup"><span data-stu-id="fe660-182">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="fe660-183">Voor elk type tuple `T` kunnen we een nieuw door de gebruiker gedefinieerd type declareren dat een subtype is van `T` met de `newtype` instructie.</span><span class="sxs-lookup"><span data-stu-id="fe660-183">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="fe660-184">In de @"microsoft.quantum.math" naam ruimte worden bijvoorbeeld complexe getallen gedefinieerd als een door de gebruiker gedefinieerd type:</span><span class="sxs-lookup"><span data-stu-id="fe660-184">In the @"microsoft.quantum.math" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="fe660-185">Met deze instructie maakt u een nieuw type met twee anonieme items van het type `Double` .</span><span class="sxs-lookup"><span data-stu-id="fe660-185">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="fe660-186">Door de gebruiker gedefinieerde typen ondersteunen ook *benoemde items* van anonieme items, vanaf Q # versie 0,7 of hoger.</span><span class="sxs-lookup"><span data-stu-id="fe660-186">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="fe660-187">We hebben bijvoorbeeld de naam ' to items ' `Re` voor de dubbele waarde van het reële deel van een complex getal en `Im` voor het imaginaire deel:</span><span class="sxs-lookup"><span data-stu-id="fe660-187">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="fe660-188">De naam van een item in een door de gebruiker gedefinieerd type betekent niet dat alle items moeten worden benoemd: elke combi natie van benoemde en niet-benoemde items wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="fe660-188">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="fe660-189">Daarnaast kunnen interne items ook een naam hebben.</span><span class="sxs-lookup"><span data-stu-id="fe660-189">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="fe660-190">Het type `Nested` zoals hieronder gedefinieerd is bijvoorbeeld een onderliggend type `(Double, (Int, String))` , waarvan alleen het item van het type de `Int` naam heeft en alle andere items anoniem zijn.</span><span class="sxs-lookup"><span data-stu-id="fe660-190">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="fe660-191">Benoemde items hebben het voor deel dat ze rechtstreeks kunnen worden geopend via de *toegangs operator* `::` .</span><span class="sxs-lookup"><span data-stu-id="fe660-191">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="fe660-192">Naast het bieden van korte aliassen voor mogelijk gecompliceerde tuple-typen, is een belang rijk voor deel van het definiëren van dergelijke typen dat ze de bedoeling van een bepaalde waarde kunnen documenteren.</span><span class="sxs-lookup"><span data-stu-id="fe660-192">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="fe660-193">Als u terugkeert naar het voor beeld van `Complex` , kunt u een 2D polaire coördinaten ook als een door de gebruiker gedefinieerd type hebben gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="fe660-193">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="fe660-194">Hoewel beide `Complex` en `Polar` beide een onderliggend type hebben `(Double, Double)` , zijn de twee typen volledig incompatibel in Q #, zodat het risico wordt geminimaliseerd dat er per ongeluk een complexe wiskundige functie wordt aangeroepen met polaire coördinaten en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="fe660-194">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="fe660-195">Op deze manier hebben door de gebruiker gedefinieerde typen een vergelijk bare rol als records in F #, bijvoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="fe660-195">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="fe660-196">Toegang tot anonieme items met de operator voor uitpakken</span><span class="sxs-lookup"><span data-stu-id="fe660-196">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="fe660-197">Om toegang te krijgen tot anonieme items, moet de ingepakte waarde eerst worden geëxtraheerd met de operator achtervoegsel `!` .</span><span class="sxs-lookup"><span data-stu-id="fe660-197">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="fe660-198">De operator ' wrap ' `!` kan de waarde in een door de gebruiker gedefinieerd type ophalen.</span><span class="sxs-lookup"><span data-stu-id="fe660-198">The "unwrap" operator, `!`, allows to extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="fe660-199">Het type van een dergelijke expressie voor ' uitpakken ' is het onderliggende type van het door de gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="fe660-199">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="fe660-200">De operator voor het uitpakken van het uitpakken wordt één laag terugloop.</span><span class="sxs-lookup"><span data-stu-id="fe660-200">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="fe660-201">Meerdere opera tors voor uitpakken kunnen worden gebruikt om toegang te krijgen tot een waarde die is verpakt met vermenigvuldiging.</span><span class="sxs-lookup"><span data-stu-id="fe660-201">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="fe660-202">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="fe660-202">For instance:</span></span>

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

<span data-ttu-id="fe660-203">Meer informatie over de operator voor uitpakken kunt u vinden [in type-expressies in Q #](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="fe660-203">More details on the unwrap operator can be found at [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="fe660-204">Waarden maken van door de gebruiker gedefinieerde typen</span><span class="sxs-lookup"><span data-stu-id="fe660-204">Creating values of user-defined types</span></span>

<span data-ttu-id="fe660-205">Waarden van een door de gebruiker gedefinieerd type kunnen worden gemaakt door de overeenkomende type-constructor aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="fe660-205">Values of a user-defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="fe660-206">U kunt ook nieuwe waarden maken op basis van bestaande, met behulp van [kopiëren-en-update-expressies](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="fe660-206">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="fe660-207">Net als bij matrices kopieert deze expressies alle item waarden van de oorspronkelijke expressie, met uitzonde ring van de opgegeven benoemde items.</span><span class="sxs-lookup"><span data-stu-id="fe660-207">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="fe660-208">Voor deze waarden worden ingesteld op die zijn gedefinieerd aan de rechter kant van de expressie.</span><span class="sxs-lookup"><span data-stu-id="fe660-208">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="fe660-209">Alle andere taal constructies, zoals [instructies update-and-reassign](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), die beschikbaar zijn voor matrix items bestaan ook uit benoemde items in door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="fe660-209">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), that are available for array items exist for named-items in user-defined types as well.</span></span>

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

<span data-ttu-id="fe660-210">Door de gebruiker gedefinieerde typen kunnen worden gebruikt wanneer elk ander type kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fe660-210">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="fe660-211">Het is met name mogelijk een matrix van een door de gebruiker gedefinieerd type te definiëren en een door de gebruiker gedefinieerd type op te geven als element van een tuple-type.</span><span class="sxs-lookup"><span data-stu-id="fe660-211">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="fe660-212">Opmerking is niet mogelijk om recursieve type structuren te maken.</span><span class="sxs-lookup"><span data-stu-id="fe660-212">Note is not possible to create recursive type structures.</span></span>
<span data-ttu-id="fe660-213">Dat wil zeggen, het type dat een door de gebruiker gedefinieerd type definieert, mag geen tuple-type zijn dat een element van het door de gebruiker gedefinieerde type bevat.</span><span class="sxs-lookup"><span data-stu-id="fe660-213">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="fe660-214">Meer in het algemeen is het mogelijk dat door de gebruiker gedefinieerde typen geen cyclische afhankelijkheden hebben, waardoor de volgende reeks type definities ongeldig is:</span><span class="sxs-lookup"><span data-stu-id="fe660-214">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a><span data-ttu-id="fe660-215">Bewerkings-en functie typen</span><span class="sxs-lookup"><span data-stu-id="fe660-215">Operation and Function Types</span></span>

<span data-ttu-id="fe660-216">Het basis type voor een aanroepable is geschreven als `('Tinput => 'Tresult)` of `('Tinput -> 'Tresult)` , waarbij beide `'Tinput` en `'Tresult` typen zijn.</span><span class="sxs-lookup"><span data-stu-id="fe660-216">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="fe660-217">Deze worden de *hand tekening* van de aanroepable genoemd.</span><span class="sxs-lookup"><span data-stu-id="fe660-217">These are called the *signature* of the callable.</span></span>

<span data-ttu-id="fe660-218">Alle Q # callables worden beschouwd als een enkele waarde als invoer en retour neren één waarde als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="fe660-218">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="fe660-219">Zowel de invoer-als uitvoer waarden kunnen Tuples zijn.</span><span class="sxs-lookup"><span data-stu-id="fe660-219">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="fe660-220">Callables die geen resultaat retour hebben `Unit` .</span><span class="sxs-lookup"><span data-stu-id="fe660-220">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="fe660-221">Callables die geen invoer hebben, hebben de lege tuple als invoer.</span><span class="sxs-lookup"><span data-stu-id="fe660-221">Callables that have no input take the empty tuple as input.</span></span>

> [!NOTE]
> <span data-ttu-id="fe660-222">Het eerste formulier, met `=>` , wordt gebruikt voor bewerkingen; het tweede formulier, met `->` , voor functions.</span><span class="sxs-lookup"><span data-stu-id="fe660-222">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
> <span data-ttu-id="fe660-223">Bijvoorbeeld, `((Qubit, Pauli) => Result)` vertegenwoordigt de hand tekening voor een mogelijke meting bewerking met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="fe660-223">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>
<span data-ttu-id="fe660-224">*Functie* typen zijn volledig opgegeven met hun hand tekening.</span><span class="sxs-lookup"><span data-stu-id="fe660-224">*Function* types are completely specified by their signature.</span></span>
<span data-ttu-id="fe660-225">Een functie die bijvoorbeeld de sinus van een hoek berekent, zou type hebben `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-225">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="fe660-226">*Bewerkingen*---maar geen functies---bepaalde extra kenmerken hebben die worden weer gegeven als onderdeel van het bewerkings type.</span><span class="sxs-lookup"><span data-stu-id="fe660-226">*Operations*---but not functions---have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="fe660-227">Dergelijke kenmerken bevatten informatie over de *functors* die door de bewerking wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="fe660-227">Such characteristics include information about what *functors* the operation supports.</span></span>
<span data-ttu-id="fe660-228">Als de uitvoering van de bewerking bijvoorbeeld kan worden voor bereid op de status van andere qubits, moet deze de functor ondersteunen `Controlled` ; als de bewerking een omgekeerde waarde heeft, moet de functor worden ondersteund `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="fe660-228">For example, if execution of the operation can be conditioned on the state of other qubits, it should support the `Controlled` functor; if the operation has an inverse, it should support the `Adjoint` functor.</span></span> <span data-ttu-id="fe660-229">Functors en-bewerkingen worden gedetailleerd besproken bij [bewerkingen en functies in Q #](xref:microsoft.quantum.guide.operationsfunctions), maar hier bespreken we gewoon hoe de hand tekening van de bewerking verandert.</span><span class="sxs-lookup"><span data-stu-id="fe660-229">Functors and operations are discussed in detail at [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions), but here we simply discuss how this alters the operation signature.</span></span>

<span data-ttu-id="fe660-230">Om ondersteuning voor de `Controlled` and/of `Adjoint` functor in een bewerkings type te vereisen, moeten we een aantekening toevoegen die de bijbehorende kenmerken aangeeft.</span><span class="sxs-lookup"><span data-stu-id="fe660-230">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="fe660-231">Een aantekening `is Ctl` (bijvoorbeeld `(Qubit => Unit is Ctl)` ) geeft aan dat de bewerking kan worden bestuurd---dat wil zeggen dat de uitvoering wordt uitgevoerd voor de status van een andere Qubit of qubits.</span><span class="sxs-lookup"><span data-stu-id="fe660-231">An annotation `is Ctl` (e.g. `(Qubit => Unit is Ctl)`) indicates that the operation is controllable---that is, it's execution conditioned on the state of another qubit or qubits.</span></span> <span data-ttu-id="fe660-232">Op dezelfde manier `is Adj` wordt hiermee aangegeven dat de bewerking een adjoint heeft, of gewoon kan worden omgekeerd, waardoor een bewerking herhaaldelijk wordt toegepast en de adjoint naar een status de status ongewijzigd laat.</span><span class="sxs-lookup"><span data-stu-id="fe660-232">Similarly, `is Adj` indicates that the operation has an adjoint; or simply, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="fe660-233">Als we willen vereisen dat een bewerking van dat Type zowel de als de `Adjoint` `Controlled` functor ondersteunt, kunnen we dit als volgt uitdrukken `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-233">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="fe660-234">De ingebouwde bewerking Pauli is bijvoorbeeld van het <xref:microsoft.quantum.intrinsic.x> type `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="fe660-234">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="fe660-235">Een bewerkings type dat geen functors ondersteunt, wordt opgegeven door het invoer-en uitvoer type alleen, zonder extra aantekening.</span><span class="sxs-lookup"><span data-stu-id="fe660-235">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="fe660-236">Functies en bewerkingen van het type para meters</span><span class="sxs-lookup"><span data-stu-id="fe660-236">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="fe660-237">Aanroep bare typen kunnen type parameters bevatten.</span><span class="sxs-lookup"><span data-stu-id="fe660-237">Callable types may contain type parameters.</span></span>
<span data-ttu-id="fe660-238">Type parameters worden aangeduid met een symbool dat wordt voorafgegaan door één aanhalings teken. `'A`is bijvoorbeeld een geldige type parameter.</span><span class="sxs-lookup"><span data-stu-id="fe660-238">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="fe660-239">Details over het definiëren van type para meters callables worden gegeven op de pagina [bewerkingen en functies in Q #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .</span><span class="sxs-lookup"><span data-stu-id="fe660-239">Details on defining type-parameterized callables are provided on the [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) page.</span></span>

<span data-ttu-id="fe660-240">Een type parameter kan meermaals voor komen in één hand tekening.</span><span class="sxs-lookup"><span data-stu-id="fe660-240">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="fe660-241">Een functie waarmee een andere functie wordt toegepast op elk element van een matrix en die de verzamelde resultaten retourneert, zou hand tekening zijn `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="fe660-241">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="fe660-242">Op dezelfde manier kan een functie die de samen stelling van twee bewerkingen retourneert, hand tekeningen hebben `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="fe660-242">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="fe660-243">Bij het aanroepen van een type geparametriseerde aanroepable moeten alle argumenten van hetzelfde type para meter van hetzelfde type zijn.</span><span class="sxs-lookup"><span data-stu-id="fe660-243">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="fe660-244">Q # biedt geen mechanisme voor het beperken van de mogelijke typen die voor een type parameter kunnen worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="fe660-244">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fe660-245">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="fe660-245">Next steps</span></span>

<span data-ttu-id="fe660-246">Nu u alle typen hebt gezien die de Q #-taal vormen, kunt u in het hoofd om [expressies in q # te typen](xref:microsoft.quantum.guide.expressions) om te zien hoe u expressies van deze verschillende typen maakt en bewerkt.</span><span class="sxs-lookup"><span data-stu-id="fe660-246">Now that you've seen all the types which comprise the Q# language, you can head to [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to see how to create and manipulate expressions of these various types.</span></span>


