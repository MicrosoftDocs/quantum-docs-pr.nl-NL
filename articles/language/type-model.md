---
title: 'Q #-gegevens typen'
description: 'Meer informatie over de verschillende typen die worden gebruikt in de Q #-programmeer taal, waaronder ingebouwde typen, matrices, Tuples, bewerkingen, functies en door de gebruiker gedefinieerde typen.'
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 1fc4c0b3fed9277c7f9f3ac421330df03c1b30e4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904652"
---
# <a name="the-type-model"></a><span data-ttu-id="7a59f-103">Het type model</span><span class="sxs-lookup"><span data-stu-id="7a59f-103">The Type Model</span></span>

<span data-ttu-id="7a59f-104">In deze sectie wordt het type Q # vermeld en wordt de syntaxis voor het opgeven en gebruiken van typen beschreven.</span><span class="sxs-lookup"><span data-stu-id="7a59f-104">This section lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="7a59f-105">Houd er rekening mee dat Q # een *sterk getypeerde* taal is, zodat het gebruik van deze typen zorgvuldig kan bijdragen aan de compiler om sterke garanties te bieden voor Q #-Program ma's tijdens het compileren.</span><span class="sxs-lookup"><span data-stu-id="7a59f-105">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>

<span data-ttu-id="7a59f-106">Om de krach tigste garanties te bieden, moeten conversies tussen typen in Q # expliciet worden gebruikt voor het gebruik van aanroepen van functies die de conversie door lopen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-106">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="7a59f-107">Er zijn verschillende functies die deel uitmaken van de naam ruimte <xref:microsoft.quantum.convert>.</span><span class="sxs-lookup"><span data-stu-id="7a59f-107">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="7a59f-108">Er wordt impliciet een conversie naar compatibele typen uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-108">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="7a59f-109">Q # bevat beide primitieve typen, die rechtstreeks kunnen worden gebruikt en een aantal manieren om nieuwe typen van andere typen te maken.</span><span class="sxs-lookup"><span data-stu-id="7a59f-109">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="7a59f-110">We beschrijven elk in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="7a59f-110">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="7a59f-111">Primitieve typen</span><span class="sxs-lookup"><span data-stu-id="7a59f-111">Primitive Types</span></span>

<span data-ttu-id="7a59f-112">De Q #-taal biedt verschillende *primitieve typen*, waaruit andere typen kunnen worden samengesteld:</span><span class="sxs-lookup"><span data-stu-id="7a59f-112">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="7a59f-113">Het `Int` type vertegenwoordigt een 64-bits geheel getal met teken, bijvoorbeeld: `2`, `107``-5`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-113">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="7a59f-114">Het `BigInt` type vertegenwoordigt een ondertekende integer met een wille keurige grootte, zoals `2L`, `107L``-5L`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-114">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="7a59f-115">Dit type is gebaseerd op de .NET-<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="7a59f-115">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="7a59f-116">voert.</span><span class="sxs-lookup"><span data-stu-id="7a59f-116">type.</span></span>
- <span data-ttu-id="7a59f-117">Het `Double` type vertegenwoordigt een drijvende-komma getal met dubbele precisie, bijvoorbeeld: `0.0`, `-1.3``4e-7`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-117">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="7a59f-118">Het `Bool` type vertegenwoordigt een Booleaanse waarde die kan `true` of `false`zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-118">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="7a59f-119">Het `Qubit` type vertegenwoordigt een Quantum bit of Qubit.</span><span class="sxs-lookup"><span data-stu-id="7a59f-119">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="7a59f-120">`Qubit`s ondoorzichtig zijn voor de gebruiker; de enige bewerking die kan worden uitgevoerd, met uitzonde ring van deze aan een andere bewerking door gegeven, is om te testen op identiteit (gelijkheid).</span><span class="sxs-lookup"><span data-stu-id="7a59f-120">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="7a59f-121">Uiteindelijk worden acties op `Qubit`s geïmplementeerd door het aanroepen van intrinsieke instructies op een Quantum processor (of een simulatie daarvan).</span><span class="sxs-lookup"><span data-stu-id="7a59f-121">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="7a59f-122">Het `Pauli` type vertegenwoordigt een van de vier Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="7a59f-122">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="7a59f-123">Dit type wordt gebruikt voor het aanduiden van de basis bewerking voor rotaties en het bepalen van het waarneem bare gemeten.</span><span class="sxs-lookup"><span data-stu-id="7a59f-123">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="7a59f-124">Dit is een genummerd type dat vier mogelijke waarden heeft: `PauliI`, `PauliX`, `PauliY`en `PauliZ`, die constanten van het type `Pauli`zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-124">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="7a59f-125">Het `Result` type vertegenwoordigt het resultaat van een meting.</span><span class="sxs-lookup"><span data-stu-id="7a59f-125">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="7a59f-126">Dit is een opgesomd type met twee mogelijke waarden: `One` en `Zero`, die constanten zijn van het type `Result`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-126">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="7a59f-127">`Zero` geeft aan dat de + 1 eigenvalue is gemeten; `One` geeft de eigenvalue-1 aan.</span><span class="sxs-lookup"><span data-stu-id="7a59f-127">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>
- <span data-ttu-id="7a59f-128">Het `Range` type vertegenwoordigt een reeks gehele getallen, aangeduid door `start..step..stop`, waarbij de stap de opties zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-128">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is options.</span></span> 
   <span data-ttu-id="7a59f-129">Dat `start .. stop` overeenkomt met `start..1..stop`, en bijvoorbeeld `1..2..7` vertegenwoordigt de reeks $\{1, 3, 5, 7\}$.</span><span class="sxs-lookup"><span data-stu-id="7a59f-129">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="7a59f-130">Het `String` type is een opeenvolging van Unicode-tekens die ondoorzichtig is voor de gebruiker nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7a59f-130">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="7a59f-131">Dit type wordt gebruikt om berichten te rapporteren aan een klassieke host in het geval van een fout of diagnostische gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="7a59f-131">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="7a59f-132">Het `Unit` type is het type dat slechts één waarde `()`toestaat.</span><span class="sxs-lookup"><span data-stu-id="7a59f-132">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="7a59f-133">Dit type wordt gebruikt om aan te geven dat de functie van Q # of de bewerking geen informatie retourneert.</span><span class="sxs-lookup"><span data-stu-id="7a59f-133">This type is used to indicate that Q# function or operation returns no information.</span></span> 

<span data-ttu-id="7a59f-134">De constanten `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`en `Zero` zijn alle gereserveerde symbolen in Q #.</span><span class="sxs-lookup"><span data-stu-id="7a59f-134">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="7a59f-135">Matrix typen</span><span class="sxs-lookup"><span data-stu-id="7a59f-135">Array Types</span></span>

<span data-ttu-id="7a59f-136">Als er een geldig Q #-type `'T`is, is er een type dat een matrix met waarden van het type `'T`vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="7a59f-136">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="7a59f-137">Dit matrix type wordt weer gegeven als `'T[]`; bijvoorbeeld `Qubit[]` of `Int[][]`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-137">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="7a59f-138">Een verzameling integers wordt bijvoorbeeld aangeduid als `Int[]`, terwijl een matrix met matrices van `(Bool, Pauli)` waarden wordt aangegeven `(Bool, Pauli)[][]`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-138">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="7a59f-139">In het tweede voor beeld ziet u dat dit een mogelijk gekartelde matrix van matrices is en niet een rechthoekige tweedimensionale matrix.</span><span class="sxs-lookup"><span data-stu-id="7a59f-139">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="7a59f-140">Q # biedt geen ondersteuning voor rechthoekige matrices met meerdere dimensies.</span><span class="sxs-lookup"><span data-stu-id="7a59f-140">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="7a59f-141">Een matrix waarde kan worden geschreven in Q #-bron code met behulp van rechte haken rond de elementen van een matrix, zoals in `[PauliI, PauliX, PauliY, PauliZ]`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-141">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="7a59f-142">Het type van een matrix letterlijke waarde wordt bepaald door het algemene basis type van alle items in de matrix.</span><span class="sxs-lookup"><span data-stu-id="7a59f-142">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="7a59f-143">De elementen van een matrix kunnen niet worden gewijzigd nadat de matrix is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7a59f-143">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="7a59f-144">Instructies update-en-reassign en/of Copy-en-update-expressies kunnen worden gebruikt om een gewijzigde matrix te maken.</span><span class="sxs-lookup"><span data-stu-id="7a59f-144">Update-and-reassign statements and/or copy-and-update expressions can be used to construct a modified array.</span></span>

<span data-ttu-id="7a59f-145">U kunt een matrix ook maken op basis van de grootte met behulp van het sleutel woord `new`:</span><span class="sxs-lookup"><span data-stu-id="7a59f-145">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="7a59f-146">In beide gevallen kan de functie kern `Length` worden gebruikt voor het verkrijgen van het aantal elementen als een `Int`wanneer een matrix is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="7a59f-146">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="7a59f-147">Matrices kunnen worden ondergeschreven met behulp van vier Kante haken, met subscripts van het type `Int` of type `Range`om afzonderlijke elementen of nieuwe matrices te verkrijgen die een subset van de elementen van een matrix bevatten.</span><span class="sxs-lookup"><span data-stu-id="7a59f-147">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="7a59f-148">De subscripts van matrices zijn gebaseerd op nul:</span><span class="sxs-lookup"><span data-stu-id="7a59f-148">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="7a59f-149">Tuple-typen</span><span class="sxs-lookup"><span data-stu-id="7a59f-149">Tuple Types</span></span>

<span data-ttu-id="7a59f-150">Als er een of meer verschillende typen `T0`, `T1`,..., `Tn`, kunnen we een nieuw *tuple-type* aanduiden als `(T0, T1, ..., Tn)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-150">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="7a59f-151">De typen die worden gebruikt voor het maken van een nieuw tuple-type kunnen Tuples zijn, zoals in `(Int, (Qubit, Qubit))`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-151">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="7a59f-152">Deze geneste is altijd eindig, maar aangezien tuple-typen niet in elke situatie zichzelf kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="7a59f-152">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="7a59f-153">Waarden van het nieuwe tuple-type zijn Tuples die worden gevormd door reeksen waarden van elk type in de tuple.</span><span class="sxs-lookup"><span data-stu-id="7a59f-153">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="7a59f-154">`(3, false)` is bijvoorbeeld een tuple waarvan type het type tuple is `(Int, Bool)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-154">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="7a59f-155">Het is mogelijk om matrices met Tuples, Tuples van matrices, Tuples van sub-Tuples, enzovoort te maken.</span><span class="sxs-lookup"><span data-stu-id="7a59f-155">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="7a59f-156">Vanaf Q # 0,3 is `Unit` de naam van het *type* van de lege tuple. `()` wordt gebruikt voor de lege tuple- *waarde*.</span><span class="sxs-lookup"><span data-stu-id="7a59f-156">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="7a59f-157">Tuple-instanties zijn onveranderbaar.</span><span class="sxs-lookup"><span data-stu-id="7a59f-157">Tuple instances are immutable.</span></span>
<span data-ttu-id="7a59f-158">Q # biedt geen mechanisme om de inhoud van een tuple te wijzigen nadat deze is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7a59f-158">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="7a59f-159">Tuples zijn een krachtig concept dat gedurende Q # wordt gebruikt voor het verzamelen van waarden in één waarde, waardoor het eenvoudiger wordt om ze te passeren.</span><span class="sxs-lookup"><span data-stu-id="7a59f-159">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="7a59f-160">Met name voor het gebruik van de tuple-notatie kunnen we uitdrukken dat elke bewerking en aanroepbaar precies één invoer hebben en er precies één uitvoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-160">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="7a59f-161">Singleton-tuple-equivalentie</span><span class="sxs-lookup"><span data-stu-id="7a59f-161">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="7a59f-162">Het is mogelijk om een singleton-tuple (single-element) te maken `('T1)`, zoals `(5)` of `([1,2,3])`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-162">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="7a59f-163">Q # behandelt echter een singleton-tuple als volledig gelijk aan een waarde van het Inge sloten type.</span><span class="sxs-lookup"><span data-stu-id="7a59f-163">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="7a59f-164">Dat wil zeggen dat er geen verschil is tussen `5` en `(5)`, of tussen `5` en `(((5)))`, of tussen `(5, (6))` en `(5, 6)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-164">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>

<span data-ttu-id="7a59f-165">Deze gelijkwaardigheid geldt voor alle doel einden, inclusief toewijzing en expressies.</span><span class="sxs-lookup"><span data-stu-id="7a59f-165">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="7a59f-166">Het is net zo geldig als het schrijven van `(5)+3` om `5+3`te schrijven en beide expressies evalueren om `8`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>
<span data-ttu-id="7a59f-167">Dit betekent met name dat een bewerking of functie waarvan het type tuple of uitvoer tuple één veld heeft, kan worden beschouwd als het nemen van één argument of het retour neren van een enkele waarde.</span><span class="sxs-lookup"><span data-stu-id="7a59f-167">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="7a59f-168">We verwijzen naar deze eigenschap als _Singleton-tuple-equivalentie_.</span><span class="sxs-lookup"><span data-stu-id="7a59f-168">We refer to this property as _singleton tuple equivalence_.</span></span>

## <a name="user-defined-types"></a><span data-ttu-id="7a59f-169">Door de gebruiker gedefinieerde typen</span><span class="sxs-lookup"><span data-stu-id="7a59f-169">User-Defined Types</span></span>

<span data-ttu-id="7a59f-170">Een Q #-bestand kan een nieuw benoemd type definiëren dat één waarde van elk juridisch type bevat.</span><span class="sxs-lookup"><span data-stu-id="7a59f-170">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="7a59f-171">Voor elk type tuple `T`kunnen we een nieuw door de gebruiker gedefinieerd type declareren dat een subtype is van `T` met de `newtype`-instructie.</span><span class="sxs-lookup"><span data-stu-id="7a59f-171">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="7a59f-172">In de naam ruimte @"microsoft.quantum.math" worden bijvoorbeeld complexe getallen gedefinieerd als een door de gebruiker gedefinieerd type:</span><span class="sxs-lookup"><span data-stu-id="7a59f-172">In the @"microsoft.quantum.math" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```

<span data-ttu-id="7a59f-173">Met deze instructie maakt u een nieuw type met twee anonieme items van het type `Double`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-173">This statement creates a new type with two anonymous items of type `Double`.</span></span>   
<span data-ttu-id="7a59f-174">Door de gebruiker gedefinieerde typen bieden geen ondersteuning voor anonieme items, ook wel vanaf Q # versie 0,7 of hoger.</span><span class="sxs-lookup"><span data-stu-id="7a59f-174">Aside from anonymous items, user defined types also support named items as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="7a59f-175">We hebben bijvoorbeeld de naam ' to items `Re` voor de dubbele waarde van het reële deel van een complex getal en `Im` voor het imaginaire deel:</span><span class="sxs-lookup"><span data-stu-id="7a59f-175">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="7a59f-176">De naam van een item in een door de gebruiker gedefinieerd type betekent niet dat alle items moeten worden benoemd: elke combi natie van benoemde en niet-benoemde items wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="7a59f-176">Naming one item in a user defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="7a59f-177">Bovendien kunnen interne items ook een naam hebben.</span><span class="sxs-lookup"><span data-stu-id="7a59f-177">Furthermore, also inner items may be named.</span></span>
<span data-ttu-id="7a59f-178">Het type `Nested` zoals hieronder gedefinieerd, heeft bijvoorbeeld een onderliggend type `(Double, (Int, String))`, waarvan alleen het item van het type `Int` de naam heeft en alle andere items anoniem zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-178">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
<span data-ttu-id="7a59f-179">Benoemde items hebben het voor deel dat ze rechtstreeks kunnen worden geopend via de toegangs operator `::`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-179">Named items have the advantage that they can be accessed directly via the access operator `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="7a59f-180">Om toegang te krijgen tot anonieme items, moet de ingepakte waarde eerst worden geëxtraheerd met behulp van de achtervoegsel-operator `!`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-180">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="7a59f-181">Met de operator ' uitpakken ', `!`, kunt u de waarde die is opgenomen in een door de gebruiker gedefinieerd type ophalen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-181">The "unwrap" operator, `!`, allows to extract the value contained in a user defined type.</span></span>
<span data-ttu-id="7a59f-182">Het type van een dergelijke expressie voor ' uitpakken ' is het onderliggende type van het door de gebruiker gedefinieerde type.</span><span class="sxs-lookup"><span data-stu-id="7a59f-182">The type of such an "unwrap" expression is the underlying type of the user defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="7a59f-183">De operator voor het uitpakken van het uitpakken wordt één laag terugloop.</span><span class="sxs-lookup"><span data-stu-id="7a59f-183">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="7a59f-184">Meerdere opera tors voor uitpakken kunnen worden gebruikt om toegang te krijgen tot een waarde die is verpakt met vermenigvuldiging.</span><span class="sxs-lookup"><span data-stu-id="7a59f-184">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="7a59f-185">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="7a59f-185">For instance:</span></span>

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

<span data-ttu-id="7a59f-186">Bekijk de sectie over het [uitpakken van expressies](xref:microsoft.quantum.language.expressions#unwrap-expressions) en de [prioriteit van Opera tors](xref:microsoft.quantum.language.expressions#operator-precedence) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7a59f-186">Take a look at the section on [unwrap expressions](xref:microsoft.quantum.language.expressions#unwrap-expressions) and [operators precedence](xref:microsoft.quantum.language.expressions#operator-precedence) for more details.</span></span>

<span data-ttu-id="7a59f-187">Waarden van een door de gebruiker gedefinieerd type kunnen worden gemaakt door de overeenkomende type-constructor aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="7a59f-187">Values of a user defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="7a59f-188">U kunt ook nieuwe waarden maken op basis van bestaande, met behulp van [kopiëren-en-update-expressies](xref:microsoft.quantum.language.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="7a59f-188">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.language.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="7a59f-189">Net als bij matrices kopieert deze expressies alle item waarden van de oorspronkelijke expressie, met uitzonde ring van de opgegeven benoemde items.</span><span class="sxs-lookup"><span data-stu-id="7a59f-189">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="7a59f-190">Voor deze waarden worden ingesteld op die zijn gedefinieerd aan de rechter kant van de expressie.</span><span class="sxs-lookup"><span data-stu-id="7a59f-190">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="7a59f-191">Alle andere taal constructies, zoals instructies voor [bijwerken en opnieuw toewijzen](xref:microsoft.quantum.language.statements#update-and-reassign-statement), die beschikbaar zijn voor matrix items bestaan ook uit benoemde items in door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-191">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.language.statements#update-and-reassign-statement), that are available for array items exist for named-items in user defined types as well.</span></span>

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

<span data-ttu-id="7a59f-192">Door de gebruiker gedefinieerde typen kunnen worden gebruikt wanneer elk ander type kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7a59f-192">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="7a59f-193">Het is met name mogelijk een matrix van een door de gebruiker gedefinieerd type te definiëren en een door de gebruiker gedefinieerd type op te geven als element van een tuple-type.</span><span class="sxs-lookup"><span data-stu-id="7a59f-193">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="7a59f-194">Het is niet mogelijk om recursieve type structuren te maken.</span><span class="sxs-lookup"><span data-stu-id="7a59f-194">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="7a59f-195">Dat wil zeggen, het type dat een door de gebruiker gedefinieerd type definieert, mag geen tuple-type zijn dat een element van het door de gebruiker gedefinieerde type bevat.</span><span class="sxs-lookup"><span data-stu-id="7a59f-195">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="7a59f-196">Meer in het algemeen is het mogelijk dat door de gebruiker gedefinieerde typen geen cyclische afhankelijkheden hebben, waardoor de volgende reeks type definities ongeldig is:</span><span class="sxs-lookup"><span data-stu-id="7a59f-196">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

<span data-ttu-id="7a59f-197">Naast het bieden van korte aliassen voor mogelijk gecompliceerde tuple-typen, is een belang rijk voor deel van het definiëren van dergelijke typen dat ze de bedoeling van een bepaalde waarde kunnen documenteren.</span><span class="sxs-lookup"><span data-stu-id="7a59f-197">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="7a59f-198">Als u terugkeert naar het voor beeld van `Complex`, kan één 2D polaire coördinaten ook als een door de gebruiker gedefinieerd type hebben gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="7a59f-198">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="7a59f-199">Hoewel zowel `Complex` als `Polar` een onderliggend type hebben `(Double, Double)`, zijn de twee typen volledig incompatibel in Q #, waarmee het risico wordt geminimaliseerd dat per ongeluk een complexe wiskundige functie aanroept met polaire coördinaten en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-199">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="7a59f-200">Op deze manier hebben door de gebruiker gedefinieerde typen een vergelijk bare rol als records F# in bijvoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7a59f-200">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


## <a name="operation-and-function-types"></a><span data-ttu-id="7a59f-201">Bewerkings-en functie typen</span><span class="sxs-lookup"><span data-stu-id="7a59f-201">Operation and Function Types</span></span>

<span data-ttu-id="7a59f-202">Een Q #- _bewerking_ is een Quantum subroutine.</span><span class="sxs-lookup"><span data-stu-id="7a59f-202">A Q# _operation_ is a quantum subroutine.</span></span>
<span data-ttu-id="7a59f-203">ofwel een aanroepbare routine die kwantumbewerkingen bevat.</span><span class="sxs-lookup"><span data-stu-id="7a59f-203">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="7a59f-204">Een Q #- _functie_ is een klassieke subroutine die wordt gebruikt binnen een Quantum algoritme.</span><span class="sxs-lookup"><span data-stu-id="7a59f-204">A Q# _function_ is a classical subroutine used within a quantum algorithm.</span></span>
<span data-ttu-id="7a59f-205">Dit kan klassieke code bevatten, maar geen Quantum bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-205">It may contain classical code but no quantum operations.</span></span>
<span data-ttu-id="7a59f-206">Met name kunnen functies geen qubits toewijzen of lenen en kunnen ze geen bewerkingen aanroepen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-206">Specifically, functions may not allocate or borrow qubits, nor may they call operations.</span></span>
<span data-ttu-id="7a59f-207">Het is echter wel mogelijk om deze bewerkingen of qubits door te geven voor verwerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-207">It is possible, however, to pass them operations or qubits for processing.</span></span>
<span data-ttu-id="7a59f-208">Functions zijn daarom volledig deterministisch in de zin dat het aanroepen van de argumenten altijd hetzelfde resultaat oplevert.</span><span class="sxs-lookup"><span data-stu-id="7a59f-208">Functions are thus entirely deterministic in the sense that calling them with the same arguments will always produce the same result.</span></span> 

<span data-ttu-id="7a59f-209">Bewerkingen en functies worden samen _callables_genoemd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-209">Together, operations and functions are called _callables_.</span></span>  <span data-ttu-id="7a59f-210">Hieronder ziet u enkele [voor beelden](#examples) .</span><span class="sxs-lookup"><span data-stu-id="7a59f-210">You can see some [examples](#examples) of these below.</span></span>

<span data-ttu-id="7a59f-211">Alle Q # callables worden beschouwd als een enkele waarde als invoer en retour neren één waarde als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="7a59f-211">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="7a59f-212">Zowel de invoer-als uitvoer waarden kunnen Tuples zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-212">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="7a59f-213">Callables die geen resultaat retour `Unit`hebben.</span><span class="sxs-lookup"><span data-stu-id="7a59f-213">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="7a59f-214">Callables die geen invoer hebben, hebben de lege tuple als invoer.</span><span class="sxs-lookup"><span data-stu-id="7a59f-214">Callables that have no input take the empty tuple as input.</span></span>

<span data-ttu-id="7a59f-215">Het basis type voor een aanroepable wordt geschreven als `('Tinput => 'Tresult)` of `('Tinput -> 'Tresult)`, waarbij zowel `'Tinput` als `'Tresult` typen zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-215">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="7a59f-216">Het eerste formulier, met `=>`, wordt gebruikt voor bewerkingen. het tweede formulier, met `->`, voor functions.</span><span class="sxs-lookup"><span data-stu-id="7a59f-216">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
<span data-ttu-id="7a59f-217">`((Qubit, Pauli) => Result)` bijvoorbeeld vertegenwoordigt de hand tekening voor een mogelijke meting bewerking met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="7a59f-217">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>

<span data-ttu-id="7a59f-218">Functie typen zijn volledig opgegeven met hun hand tekening.</span><span class="sxs-lookup"><span data-stu-id="7a59f-218">Function types are completely specified by their signature.</span></span>
<span data-ttu-id="7a59f-219">Een functie die de sinus van een hoek berekent, zou bijvoorbeeld het type `(Double -> Double)`hebben.</span><span class="sxs-lookup"><span data-stu-id="7a59f-219">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="7a59f-220">Bewerkingen, maar geen functies, hebben bepaalde extra _kenmerken_ die worden weer gegeven als onderdeel van het bewerkings type.</span><span class="sxs-lookup"><span data-stu-id="7a59f-220">Operations—but not functions—have certain additional _characteristics_ that are expressed as part of the operation type.</span></span> <span data-ttu-id="7a59f-221">Dergelijke kenmerken bevatten informatie over de functors die door de bewerking wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="7a59f-221">Such characteristics include information about what functors the operation supports.</span></span>
<span data-ttu-id="7a59f-222">Functors zijn meta bewerkingen die een specialisatie van een basis bewerking genereren. Zie [functors](#functors)hieronder.</span><span class="sxs-lookup"><span data-stu-id="7a59f-222">Functors are meta-operations that generate a specialization of a base operation; see [Functors](#functors), below.</span></span>

<span data-ttu-id="7a59f-223">Bewerkings typen worden opgegeven door het invoer type, het uitvoer type en hun eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-223">Operation types are specified by the their input type, output type, and their characteristics.</span></span>    
<span data-ttu-id="7a59f-224">Om ondersteuning te vereisen voor de `Controlled` en/of `Adjoint` functor in een bewerkings type, moeten we een aantekening toevoegen die de bijbehorende kenmerken aangeeft.</span><span class="sxs-lookup"><span data-stu-id="7a59f-224">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="7a59f-225">Een aantekening `is Ctl` bijvoorbeeld geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-225">An annotation `is Ctl` for example indicates that the operation is controllable.</span></span> <span data-ttu-id="7a59f-226">Als we willen vereisen dat een bewerking van dat Type zowel de `Adjoint` als `Controlled` functor ondersteunt, kunnen we dit als `(Qubit => Unit is Adj + Ctl)`uitdrukken.</span><span class="sxs-lookup"><span data-stu-id="7a59f-226">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="7a59f-227">De gebruikte bewerkings kenmerken `Adj` en `Ctl` strikt uitspreken zijn twee vooraf gedefinieerde sets labels, waarbij elk label een bepaalde bewerkings kenmerken aangeeft, zoals bijvoorbeeld ondersteuning voor een bepaald functor.</span><span class="sxs-lookup"><span data-stu-id="7a59f-227">The used operation characteristics `Adj` and `Ctl` strictly speaking are two pre-defined sets of labels, where each label indicates a particular operation characteristics like e.g. support for a particular functor.</span></span>
<span data-ttu-id="7a59f-228">`+` wordt dus gebruikt om de samen voeging van deze twee sets aan te geven en `*` wordt gebruikt om het snij punt aan te geven, bijvoorbeeld de labels die voor beide sets gelden.</span><span class="sxs-lookup"><span data-stu-id="7a59f-228">Hence, `+` is used to indicate the union of those two sets, and `*` is used to indicate the intersection - i.e. the labels that are common to both sets.</span></span>  

<span data-ttu-id="7a59f-229">De Pauli-bewerking `X` heeft bijvoorbeeld type `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-229">For example, the Pauli `X` operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="7a59f-230">Een bewerkings type dat geen functors ondersteunt, wordt opgegeven door het invoer-en uitvoer type alleen, zonder extra aantekening.</span><span class="sxs-lookup"><span data-stu-id="7a59f-230">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>


### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="7a59f-231">Functies en bewerkingen van het type para meters</span><span class="sxs-lookup"><span data-stu-id="7a59f-231">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="7a59f-232">Aanroep bare typen kunnen type parameters bevatten.</span><span class="sxs-lookup"><span data-stu-id="7a59f-232">Callable types may contain type parameters.</span></span>
<span data-ttu-id="7a59f-233">Type parameters worden aangeduid met een symbool dat wordt voorafgegaan door één aanhalings teken. `'A` is bijvoorbeeld een geldige type parameter.</span><span class="sxs-lookup"><span data-stu-id="7a59f-233">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>

<span data-ttu-id="7a59f-234">Een type parameter kan meermaals voor komen in één hand tekening.</span><span class="sxs-lookup"><span data-stu-id="7a59f-234">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="7a59f-235">Een functie waarmee een andere functie wordt toegepast op elk element van een matrix en die de verzamelde resultaten retourneert, zou hand tekening `(('A[], 'A->'A) -> 'A[])`hebben.</span><span class="sxs-lookup"><span data-stu-id="7a59f-235">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="7a59f-236">Op dezelfde manier kan een functie die de samen stelling van twee bewerkingen retourneert, een hand tekening hebben `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-236">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="7a59f-237">Bij het aanroepen van een type geparametriseerde aanroepable moeten alle argumenten van hetzelfde type para meter van hetzelfde type zijn.</span><span class="sxs-lookup"><span data-stu-id="7a59f-237">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="7a59f-238">Q # biedt geen mechanisme voor het beperken van de mogelijke typen die voor een type parameter kunnen worden vervangen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-238">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

### <a name="type-compatibility"></a><span data-ttu-id="7a59f-239">Type compatibiliteit</span><span class="sxs-lookup"><span data-stu-id="7a59f-239">Type Compatibility</span></span>

<span data-ttu-id="7a59f-240">Een bewerking met aanvullende functors-ondersteuning kan worden gebruikt op een wille keurige locatie met minder functors, maar dezelfde hand tekening wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="7a59f-240">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="7a59f-241">Een bewerking van het type `(Qubit => Unit is Adj)` kan bijvoorbeeld worden gebruikt overal een bewerking van het type `(Qubit => Unit)` wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="7a59f-241">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="7a59f-242">Q # is covariantie ten opzichte van aanroep bare retour typen: een aanroepable die een type `'A` retourneert, is compatibel met een aanroepbaar met hetzelfde invoer type en een resultaat type dat `'A` compatibel is met.</span><span class="sxs-lookup"><span data-stu-id="7a59f-242">Q# is covariant with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="7a59f-243">Q # is contra variant met betrekking tot invoer typen: een aanroepable die een type `'A` als invoer compatibel is met een aanroepbaar met hetzelfde resultaat type en een invoer type dat compatibel is met `'A`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-243">Q# is contravariant with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="7a59f-244">Dat wil zeggen, op basis van de volgende definities:</span><span class="sxs-lookup"><span data-stu-id="7a59f-244">That is, given the following definitions:</span></span>

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="7a59f-245">de volgende voor waarden zijn waar:</span><span class="sxs-lookup"><span data-stu-id="7a59f-245">the following are true:</span></span>

- <span data-ttu-id="7a59f-246">De functie `ConjugateInvertWith` kan worden aangeroepen met een `inner` argument van `Invert` of `ApplyUnitary`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-246">The function `ConjugateInvertWith` may be invoked with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="7a59f-247">De functie `ConjugateUnitaryWith` kan worden aangeroepen met een `inner` argument van `ApplyUnitary`, maar niet `Invert`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-247">The function `ConjugateUnitaryWith` may be invoked with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="7a59f-248">Een waarde van het type `(Qubit[] => Unit is Adj + Ctl)` kan worden geretourneerd vanuit `ConjugateInvertWith`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-248">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a59f-249">Q # 0,3 introduceert een aanzienlijk verschil in het gedrag van door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="7a59f-249">Q# 0.3 introduces a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="7a59f-250">Door de gebruiker gedefinieerde typen worden behandeld als een ingepakte versie van het onderliggende type, in plaats van als subtype.</span><span class="sxs-lookup"><span data-stu-id="7a59f-250">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="7a59f-251">Dit betekent dat een waarde van een door de gebruiker gedefinieerd type niet kan worden gebruikt als een waarde van het onderliggende type wordt verwacht.</span><span class="sxs-lookup"><span data-stu-id="7a59f-251">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>

### <a name="functors"></a><span data-ttu-id="7a59f-252">Functors</span><span class="sxs-lookup"><span data-stu-id="7a59f-252">Functors</span></span>

<span data-ttu-id="7a59f-253">Een functor in Q # is een Factory die een nieuwe bewerking vanuit een andere bewerking definieert.</span><span class="sxs-lookup"><span data-stu-id="7a59f-253">A functor in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="7a59f-254">Functors hebben toegang tot de implementatie van de basis bewerking bij het definiëren van de implementatie van de nieuwe bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-254">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="7a59f-255">Daarom kunnen functors complexere functies uitvoeren dan traditionele functies op een hoger niveau.</span><span class="sxs-lookup"><span data-stu-id="7a59f-255">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span>

<span data-ttu-id="7a59f-256">Functors hebben geen weer gave in het Q #-type systeem.</span><span class="sxs-lookup"><span data-stu-id="7a59f-256">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="7a59f-257">Het is dus niet mogelijk om deze aan een variabele te binden of als argumenten door te geven.</span><span class="sxs-lookup"><span data-stu-id="7a59f-257">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="7a59f-258">Een functor wordt gebruikt door deze toe te passen op een bewerking en een nieuwe bewerking te retour neren.</span><span class="sxs-lookup"><span data-stu-id="7a59f-258">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="7a59f-259">De bewerking die het resultaat is van het Toep assen van de `Adjoint` functor aan de `Y` bewerking wordt bijvoorbeeld geschreven als `Adjoint Y`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-259">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="7a59f-260">De nieuwe bewerking kan vervolgens worden aangeroepen, zoals elke andere bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-260">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="7a59f-261">`Adjoint Y(q1)` past de adjoint functor toe aan de `Y` bewerking om een nieuwe bewerking te genereren en past die nieuwe bewerking toe op `q1`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-261">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>

<span data-ttu-id="7a59f-262">Op dezelfde manier `Controlled X(controls, target)` de beheerde functor toegepast op de `X` bewerking om een nieuwe bewerking te genereren en wordt die nieuwe bewerking toegepast op `controls` en `target`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-262">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

<span data-ttu-id="7a59f-263">De twee standaard functors in Q # zijn `Adjoint` en `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-263">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

#### <a name="adjoint"></a><span data-ttu-id="7a59f-264">Adjoint</span><span class="sxs-lookup"><span data-stu-id="7a59f-264">Adjoint</span></span>

<span data-ttu-id="7a59f-265">In de Quantum Computing is de adjoint van een bewerking de complexe geconjugeerde omzetting van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-265">In quantum computing, the adjoint of an operation is the complex conjugate transpose of the operation.</span></span>
<span data-ttu-id="7a59f-266">Voor bewerkingen waarbij een unitary-operator wordt geïmplementeerd, is de adjoint de inverse van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-266">For operations that implement a unitary operator, the adjoint is the inverse of the operation.</span></span>
<span data-ttu-id="7a59f-267">Voor een eenvoudige bewerking die zojuist een reeks andere unitary-bewerkingen op een set qubits aanroept, kan de adjoint worden berekend door de adjoints van de subbewerkingen op dezelfde qubits toe te passen in de omgekeerde volg orde.</span><span class="sxs-lookup"><span data-stu-id="7a59f-267">For a simple operation that just invokes a sequence of other unitary operations on a set of qubits, the adjoint may be computed by applying the adjoints of the sub-operations on the same qubits, in the reverse sequence.</span></span>

<span data-ttu-id="7a59f-268">Op basis van een bewerkings expressie kan een nieuwe bewerkings expressie worden gevormd met behulp van de `Adjoint` functor.</span><span class="sxs-lookup"><span data-stu-id="7a59f-268">Given an operation expression, a new operation expression may be formed using the `Adjoint` functor.</span></span>
<span data-ttu-id="7a59f-269">`Adjoint QFT` wijst bijvoorbeeld de adjoint van de `QFT` bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-269">For instance, `Adjoint QFT` designates the adjoint of the `QFT` operation.</span></span>
<span data-ttu-id="7a59f-270">De nieuwe bewerking heeft dezelfde hand tekening en type als de basis bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-270">The new operation has the same signature and type as the base operation.</span></span>
<span data-ttu-id="7a59f-271">Met name maakt de nieuwe bewerking ook gebruik van `Adjoint`en staat `Controlled` alleen toe als de basis bewerking is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-271">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>

<span data-ttu-id="7a59f-272">De adjoint-functor is zijn eigen inverse; dat wil zeggen dat `Adjoint Adjoint Op` altijd hetzelfde is als `Op`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-272">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled"></a><span data-ttu-id="7a59f-273">Gelijkrichter</span><span class="sxs-lookup"><span data-stu-id="7a59f-273">Controlled</span></span>

<span data-ttu-id="7a59f-274">De gecontroleerde versie van een bewerking is een nieuwe bewerking waarbij de basis bewerking alleen effectief wordt toegepast als alle besturings elementen qubits een opgegeven status hebben.</span><span class="sxs-lookup"><span data-stu-id="7a59f-274">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="7a59f-275">Als het besturings element qubits zich in de superpositie bevindt, wordt de basis bewerking samenhangend toegepast op het juiste deel van de superpositie.</span><span class="sxs-lookup"><span data-stu-id="7a59f-275">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="7a59f-276">Daarom worden beheerde bewerkingen vaak gebruikt voor het genereren van Entanglement.</span><span class="sxs-lookup"><span data-stu-id="7a59f-276">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="7a59f-277">In Q # maken bewaakte versies altijd een matrix van besturings element qubits, en de opgegeven status is altijd voor alle besturings elementen qubits in de status berekening (`PauliZ`) `One`, $ \ket{1}$.</span><span class="sxs-lookup"><span data-stu-id="7a59f-277">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
<span data-ttu-id="7a59f-278">Het beheer op basis van andere Staten kan worden bereikt door de juiste unitary-bewerking toe te passen op de controle qubits vóór de gecontroleerde bewerking en vervolgens de inverse van de unitary-bewerking toe te passen na de gecontroleerde bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-278">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
<span data-ttu-id="7a59f-279">Als u bijvoorbeeld een `X` bewerking toepast op een besturings element Qubit vóór en na een beheerde bewerking, zal de bewerking de `Zero` status ($ \ket{0}$) voor die Qubit beheren. het Toep assen van een `H` bewerking vóór en na gaat de `PauliX` `One` status, dat wil zeggen-1 eigenvalue van Pauli X, $ \ket{-} \mathrel{: =} (\ket{0}-\ket{1})/\sqrt{2}$ in plaats van de `PauliZ` `One` status.</span><span class="sxs-lookup"><span data-stu-id="7a59f-279">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="7a59f-280">Op basis van een bewerkings expressie kan een nieuwe bewerkings expressie worden gevormd met behulp van de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="7a59f-280">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="7a59f-281">De hand tekening van de nieuwe bewerking is gebaseerd op de hand tekening van de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-281">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="7a59f-282">Het resultaat type is hetzelfde, maar het invoer type is een twee-tuple met een Qubit-matrix met de Qubit (s) die het eerste element bevat en de argumenten van de oorspronkelijke bewerking als het tweede element.</span><span class="sxs-lookup"><span data-stu-id="7a59f-282">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="7a59f-283">De nieuwe bewerking ondersteunt `Controlled`en ondersteunt `Adjoint` alleen als de oorspronkelijke bewerking wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-283">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="7a59f-284">Als de oorspronkelijke bewerking slechts één argument heeft gevolgd, komt de singleton-tuple-equivalentie hier te staan.</span><span class="sxs-lookup"><span data-stu-id="7a59f-284">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="7a59f-285">`Controlled X` is bijvoorbeeld de bewaakte versie van de `X` bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-285">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span>
<span data-ttu-id="7a59f-286">`X` is van het type `(Qubit => Unit is Adj + Ctl)`, dus `Controlled X` heeft type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; vanwege Singleton-tuple-equivalentie is dit hetzelfde als `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-286">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="7a59f-287">Als de basis bewerking meerdere argumenten heeft, moet u de overeenkomstige argumenten van de gecontroleerde versie van de bewerking tussen haakjes plaatsen om ze te converteren naar een tuple.</span><span class="sxs-lookup"><span data-stu-id="7a59f-287">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="7a59f-288">`Controlled Rz` is bijvoorbeeld de bewaakte versie van de `Rz` bewerking.</span><span class="sxs-lookup"><span data-stu-id="7a59f-288">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span>
<span data-ttu-id="7a59f-289">`Rz` is van het type `((Double, Qubit) => Unit is Adj + Ctl)`, dus `Controlled Rz` heeft type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-289">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="7a59f-290">`Controlled Rz(controls, (0.1, target))` zou dus een geldige aanroep zijn van `Controlled Rz` (Let op de haakjes rond `0.1, target`).</span><span class="sxs-lookup"><span data-stu-id="7a59f-290">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="7a59f-291">Een ander voor beeld: `CNOT(control, target)` kan worden geïmplementeerd als `Controlled X([control], target)`.</span><span class="sxs-lookup"><span data-stu-id="7a59f-291">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="7a59f-292">Als een doel moet worden beheerd door 2 Control qubits (CCNOT), kunnen we `Controlled X([control1, control2], target)`-instructie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7a59f-292">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

### <a name="examples"></a><span data-ttu-id="7a59f-293">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7a59f-293">Examples</span></span>

<span data-ttu-id="7a59f-294">Dit voor beeld van een Q #-bewerking is afkomstig uit het voor beeld van de [meting](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) .</span><span class="sxs-lookup"><span data-stu-id="7a59f-294">This example of a Q# operation comes from the [Measurement](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) sample.</span></span> <span data-ttu-id="7a59f-295">Binnen bewerkingen kunnen we qubits toewijzen en Quantum bewerkingen gebruiken op deze qubits, zoals `H` en `X`:</span><span class="sxs-lookup"><span data-stu-id="7a59f-295">Within operations, we can allocate qubits and use quantum operations on those qubits such as `H` and `X`:</span></span>

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit() : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit
            set result = M(qubit);      // Measure the qubit
            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

<span data-ttu-id="7a59f-296">Dit voor beeld van een functie is afkomstig uit het [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) -voor beeld.</span><span class="sxs-lookup"><span data-stu-id="7a59f-296">This example of a function comes from the [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) sample.</span></span> <span data-ttu-id="7a59f-297">Het bevat louter klassieke code.</span><span class="sxs-lookup"><span data-stu-id="7a59f-297">It contains purely classical code.</span></span> <span data-ttu-id="7a59f-298">U kunt zien dat, in tegens telling tot het bovenstaande voor beeld, geen qubits worden toegewezen en er geen Quantum bewerkingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7a59f-298">You can see that, unlike the example above, no qubits are allocated, and no quantum operations are used.</span></span>

```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function PointwiseProduct(left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

<span data-ttu-id="7a59f-299">Het is ook mogelijk dat een functie qubits kan worden door gegeven voor verwerking, zoals in dit voor beeld van het [ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) -voor beeld.</span><span class="sxs-lookup"><span data-stu-id="7a59f-299">It is also possible for a function to be passed qubits for processing, as in this example from the [ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) sample.</span></span> <span data-ttu-id="7a59f-300">Qubits worden door gegeven aan de functie en worden gebruikt voor de verwerking, maar op geen enkel moment zijn de Qubit-statussen zelf gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="7a59f-300">Qubits are passed to the function and used for processing, although at no point are the qubit states themselves modified.</span></span>

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates(
    qubits : Qubit[], 
    masks : MCMTMask[]) 
: MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
