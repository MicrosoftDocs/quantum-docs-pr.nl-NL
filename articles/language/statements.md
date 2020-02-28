---
title: 'Q #-instructies'
description: 'Meer informatie over het juiste gebruik van instructies in Q #, inclusief functie-en bewerkings declaraties, variabele declaraties en toewijzingen en bewerkings aanroepen.'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: e801a5fdd24b973f47d23d2aca6f11bbebf333d4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904669"
---
# <a name="statements-and-other-constructs"></a><span data-ttu-id="84025-103">Instructies en andere constructs</span><span class="sxs-lookup"><span data-stu-id="84025-103">Statements and Other Constructs</span></span>

## <a name="comments"></a><span data-ttu-id="84025-104">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="84025-104">Comments</span></span>

<span data-ttu-id="84025-105">Opmerkingen beginnen met twee slashes, `//`en door gaan tot het einde van de regel.</span><span class="sxs-lookup"><span data-stu-id="84025-105">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="84025-106">Een opmerking kan ergens in een Q #-bron bestand worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="84025-106">A comment may appear anywhere in a Q# source file.</span></span>

### <a name="documentation-comments"></a><span data-ttu-id="84025-107">Documentatie opmerkingen</span><span class="sxs-lookup"><span data-stu-id="84025-107">Documentation Comments</span></span>

<span data-ttu-id="84025-108">Opmerkingen die beginnen met drie slashes, `///`, worden speciaal door de compiler behandeld wanneer ze direct vóór een naam ruimte, bewerking, specialisatie, functie of type definitie worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="84025-108">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="84025-109">In dat geval wordt de inhoud ervan als documentatie voor het gedefinieerde aanroepende of door de gebruiker gedefinieerde type beschouwd, net als bij andere .NET-talen.</span><span class="sxs-lookup"><span data-stu-id="84025-109">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="84025-110">Binnen `///` opmerkingen wordt tekst die als onderdeel van de API-documentatie wordt weer gegeven, opgemaakt als een [prijs](https://daringfireball.net/projects/markdown/syntax)opgave, waarbij verschillende delen van de documentatie worden aangegeven door middel van speciaal benoemde kopteksten.</span><span class="sxs-lookup"><span data-stu-id="84025-110">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="84025-111">Als uitbrei ding van de prijs informatie kunnen kruis verwijzingen naar bewerkingen, functies en door de gebruiker gedefinieerde typen in Q # worden opgenomen met behulp van de `@"<ref target>"`, waarbij `<ref target>` wordt vervangen door de volledig gekwalificeerde naam van het code-object waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="84025-111">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="84025-112">Een documentatie-engine kan eventueel ook extra kortings uitbreidingen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="84025-112">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="84025-113">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-113">For example:</span></span>

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

<span data-ttu-id="84025-114">De volgende namen worden herkend als documentatie opmerkings koppen.</span><span class="sxs-lookup"><span data-stu-id="84025-114">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="84025-115">**Samen vatting**: een korte samen vatting van het gedrag van een functie of bewerking, of van het doel van een type.</span><span class="sxs-lookup"><span data-stu-id="84025-115">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="84025-116">De eerste alinea van de samen vatting wordt gebruikt voor het aanwijzen van informatie.</span><span class="sxs-lookup"><span data-stu-id="84025-116">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="84025-117">Dit moet tekst zonder opmaak zijn.</span><span class="sxs-lookup"><span data-stu-id="84025-117">It should be plain text.</span></span>
- <span data-ttu-id="84025-118">**Beschrijving**: een beschrijving van het gedrag van een functie of bewerking, of van het doel van een type.</span><span class="sxs-lookup"><span data-stu-id="84025-118">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="84025-119">De samen vatting en beschrijving worden samengevoegd om het gegenereerde documentatie bestand te vormen voor de functie, bewerking of het type.</span><span class="sxs-lookup"><span data-stu-id="84025-119">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="84025-120">De beschrijving mag in-line-symbolen en-vergelijkingen in LaTeX-indeling bevatten.</span><span class="sxs-lookup"><span data-stu-id="84025-120">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="84025-121">**Invoer**: een beschrijving van de invoer-tuple voor een bewerking of functie.</span><span class="sxs-lookup"><span data-stu-id="84025-121">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="84025-122">Kan aanvullende subsecties van de korting bevatten die elk afzonderlijk element van de invoer-tuple aangeven.</span><span class="sxs-lookup"><span data-stu-id="84025-122">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="84025-123">**Output**: een beschrijving van de tuple die wordt geretourneerd door een bewerking of functie.</span><span class="sxs-lookup"><span data-stu-id="84025-123">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="84025-124">**Type parameters**: een lege sectie die één extra subsectie bevat voor elke algemene type parameter.</span><span class="sxs-lookup"><span data-stu-id="84025-124">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="84025-125">**Voor beeld**: een kort voor beeld van het gebruik van de bewerking, functie of het type.</span><span class="sxs-lookup"><span data-stu-id="84025-125">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="84025-126">**Opmerkingen**: diverse Prose die een aspect van de bewerking, functie of type beschrijven.</span><span class="sxs-lookup"><span data-stu-id="84025-126">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="84025-127">**Zie ook**: een lijst met volledig gekwalificeerde namen die betrekking hebben op gerelateerde functies, bewerkingen of door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="84025-127">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="84025-128">**Verwijzingen**: een lijst met verwijzingen en bron vermeldingen voor het item dat wordt gedocumenteerd.</span><span class="sxs-lookup"><span data-stu-id="84025-128">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="namespaces"></a><span data-ttu-id="84025-129">Naamruimten</span><span class="sxs-lookup"><span data-stu-id="84025-129">Namespaces</span></span>

<span data-ttu-id="84025-130">Elke Q #-bewerking,-functie en een door de gebruiker gedefinieerd type worden binnen een naam ruimte gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="84025-130">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>
<span data-ttu-id="84025-131">Q # volgt dezelfde regels als voor naam als andere .NET-talen.</span><span class="sxs-lookup"><span data-stu-id="84025-131">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="84025-132">Q # biedt echter geen ondersteuning voor relatieve verwijzingen naar naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="84025-132">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="84025-133">Dat wil zeggen, als de naam ruimte `a.b` is geopend, een verwijzing naar een bewerkings naam `c.d` niet wordt omgezet naar een bewerking met volledige naam `a.b.c.d`.</span><span class="sxs-lookup"><span data-stu-id="84025-133">That is, if the namespace `a.b` has been opened, a reference to an operation names `c.d` will not be resolved to an operation with full name `a.b.c.d`.</span></span>

<span data-ttu-id="84025-134">Binnen een naam ruimte blok kan de `open`-instructie worden gebruikt voor het importeren van alle typen en callables die zijn gedeclareerd in een bepaalde naam ruimte en deze te verwijzen naar de niet-gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="84025-134">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span> <span data-ttu-id="84025-135">Een korte naam voor de naam ruimte kan eventueel worden gedefinieerd, zodat alle elementen van die naam ruimte kunnen (en moeten) worden gekwalificeerd door de gedefinieerde korte naam.</span><span class="sxs-lookup"><span data-stu-id="84025-135">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="84025-136">De `open`-instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.</span><span class="sxs-lookup"><span data-stu-id="84025-136">The `open` directive applies to the entire namespace block within a file.</span></span>

<span data-ttu-id="84025-137">Er moet naar een type of aanroepbaar worden gedefinieerd in een andere naam ruimte die niet in de huidige naam ruimte wordt geopend, met de volledig gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="84025-137">A type or callable defined in another namespace that is not opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="84025-138">Een bewerking met de naam `Op` in de naam ruimte `X.Y` moet bijvoorbeeld verwijzen naar de volledig gekwalificeerde naam `X.Y.Op`, tenzij de `X.Y` naam ruimte eerder in het huidige blok is geopend.</span><span class="sxs-lookup"><span data-stu-id="84025-138">For example, an operation named `Op` in the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="84025-139">Zoals hierboven vermeld, is het niet mogelijk om te verwijzen naar de bewerking als `Y.Op`, zelfs als de naam ruimte `X` is geopend.</span><span class="sxs-lookup"><span data-stu-id="84025-139">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="84025-140">Als er een korte naam `Z` voor `X.Y` is gedefinieerd in die naam ruimte en het bestand, moet `Op` worden aangeduid als `Z.Op`.</span><span class="sxs-lookup"><span data-stu-id="84025-140">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

<span data-ttu-id="84025-141">Het is doorgaans beter om een naam ruimte op te maken met behulp van een `open`-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-141">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="84025-142">Het gebruik van een volledig gekwalificeerde naam is vereist als twee naam ruimten constructies met dezelfde naam definiëren. voor de huidige bron worden constructies van beide gebruikt.</span><span class="sxs-lookup"><span data-stu-id="84025-142">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

## <a name="formatting"></a><span data-ttu-id="84025-143">Opmaak</span><span class="sxs-lookup"><span data-stu-id="84025-143">Formatting</span></span>

<span data-ttu-id="84025-144">De meeste Q #-instructies en de instructies eindigen met een punt komma, `;`.</span><span class="sxs-lookup"><span data-stu-id="84025-144">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="84025-145">Instructies en aangiften, zoals `for` en `operation` die eindigen op een instructie blok, hebben geen afsluitende punt komma.</span><span class="sxs-lookup"><span data-stu-id="84025-145">Statements and declarations such as `for` and `operation` that end with a statement block do not require a terminating semicolon.</span></span>
<span data-ttu-id="84025-146">Elke instructie bevat een beschrijving van de vraag of de afsluit punt komma is vereist.</span><span class="sxs-lookup"><span data-stu-id="84025-146">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="84025-147">Instructies, zoals expressies, declaraties en instructies, kunnen worden verdeeld over meerdere regels.</span><span class="sxs-lookup"><span data-stu-id="84025-147">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="84025-148">Meerdere instructies op één regel moeten worden vermeden.</span><span class="sxs-lookup"><span data-stu-id="84025-148">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="84025-149">Instructie blokken</span><span class="sxs-lookup"><span data-stu-id="84025-149">Statement Blocks</span></span>

<span data-ttu-id="84025-150">Q #-instructies worden gegroepeerd in instructie blokken.</span><span class="sxs-lookup"><span data-stu-id="84025-150">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="84025-151">Een instructie blok begint met een openings `{` en eindigt met een sluit `}`.</span><span class="sxs-lookup"><span data-stu-id="84025-151">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="84025-152">Een overzichts blok dat is inge sloten in een ander blok, wordt beschouwd als een subblok van het container blok; contains-en sub-blokken worden ook outer-en Inner-blokken genoemd.</span><span class="sxs-lookup"><span data-stu-id="84025-152">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="symbol-binding-and-assignment"></a><span data-ttu-id="84025-153">Symbool binding en toewijzing</span><span class="sxs-lookup"><span data-stu-id="84025-153">Symbol Binding and Assignment</span></span>

<span data-ttu-id="84025-154">Q # onderscheidt tussen onveranderlijke en onveranderlijke symbolen.</span><span class="sxs-lookup"><span data-stu-id="84025-154">Q# distinguishes between mutable and immutable symbols.</span></span>
<span data-ttu-id="84025-155">In het algemeen wordt het gebruik van onveranderbare symbolen aanbevolen omdat de compiler meer optimalisaties kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="84025-155">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="84025-156">De linkerkant van de binding bestaat uit een symbool-tuple en de rechter kant van een expressie.</span><span class="sxs-lookup"><span data-stu-id="84025-156">The left-hand-side of the binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

<span data-ttu-id="84025-157">Aangezien alle typen Q # waardetypen zijn, is het qubits van een enigszins speciale rol, formeel een ' kopie ' gemaakt wanneer een waarde is gebonden aan een symbool of wanneer een symbool wordt losgekoppeld.</span><span class="sxs-lookup"><span data-stu-id="84025-157">Since all Q# types are value types - with the qubits taking a somewhat special role - formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="84025-158">Dat wil zeggen dat het gedrag van Q # hetzelfde is als wanneer er een kopie is gemaakt voor de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="84025-158">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span> <span data-ttu-id="84025-159">Dit bevat met name ook matrices.</span><span class="sxs-lookup"><span data-stu-id="84025-159">This in particular also includes arrays.</span></span> <span data-ttu-id="84025-160">Natuurlijk worden alleen de relevante onderdelen, indien nodig, feitelijk opnieuw gemaakt.</span><span class="sxs-lookup"><span data-stu-id="84025-160">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

### <a name="tuple-deconstruction"></a><span data-ttu-id="84025-161">Ontbouw van tuple</span><span class="sxs-lookup"><span data-stu-id="84025-161">Tuple Deconstruction</span></span>

<span data-ttu-id="84025-162">Als de rechter kant van de binding een tuple is, kan die tuple worden ontbouwd bij toewijzing.</span><span class="sxs-lookup"><span data-stu-id="84025-162">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="84025-163">Deze ontbouwingen kunnen geneste Tuples omvatten en een volledige of gedeeltelijke ontbouwing is geldig zolang de vorm van de tuple aan de rechter kant compatibel is met de vorm van de symbool-tuple.</span><span class="sxs-lookup"><span data-stu-id="84025-163">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>
<span data-ttu-id="84025-164">Het ontbouwen van een tupel kan met name ook worden gebruikt wanneer de rechter kant van de `=` een tuple-expressie is.</span><span class="sxs-lookup"><span data-stu-id="84025-164">Tuple deconstruction can in particular also be used when the right-hand side of the `=` is a tuple-valued expression.</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a><span data-ttu-id="84025-165">Onveranderbare symbolen</span><span class="sxs-lookup"><span data-stu-id="84025-165">Immutable Symbols</span></span>

<span data-ttu-id="84025-166">Onveranderbare symbolen zijn gekoppeld met behulp van de `let`-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-166">Immutable symbols are bound using the `let` statement.</span></span>
<span data-ttu-id="84025-167">Dit is ongeveer gelijk aan de declaratie van variabelen en initialisatie in talen zoals C#, behalve dat Q #-symbolen, zodra deze is gebonden, mag niet worden gewijzigd. `let` bindingen zijn onveranderbaar.</span><span class="sxs-lookup"><span data-stu-id="84025-167">This is roughly equivalent to variable declaration and initialization in languages such as C#, except that Q# symbols, once bound, may not be changed; `let` bindings are immutable.</span></span>

<span data-ttu-id="84025-168">Een onveranderlijke binding bestaat uit het tref woord `let`, gevolgd door een symbool of symbool tuple, een gelijkteken `=`, een expressie om de symbolen te binden aan en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="84025-168">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="84025-169">Het type van de afhankelijke symbolen wordt afgeleid op basis van de expressie aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="84025-169">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span>

### <a name="mutable-symbols"></a><span data-ttu-id="84025-170">Onveranderbare symbolen</span><span class="sxs-lookup"><span data-stu-id="84025-170">Mutable Symbols</span></span>

<span data-ttu-id="84025-171">Onveranderbare symbolen worden gedefinieerd en geïnitialiseerd met behulp van de `mutable`-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-171">Mutable symbols are defined and initialized using the `mutable` statement.</span></span>
<span data-ttu-id="84025-172">Symbolen die zijn gedeclareerd en gebonden als onderdeel van een `mutable` instructie, kunnen later in de code aan een andere waarde worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="84025-172">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> 

<span data-ttu-id="84025-173">Een onveranderlijke bindings instructie bestaat uit het tref woord `mutable`, gevolgd door een symbool of symbool tuple, een gelijkteken `=`, een expressie om de symbolen te binden aan en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="84025-173">A mutable binding statement consists of the keyword `mutable`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="84025-174">Het type van de afhankelijke symbolen wordt afgeleid op basis van de expressie aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="84025-174">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span> <span data-ttu-id="84025-175">Als een symbool later in de code wordt gebonden, wordt het type ervan niet gewijzigd en moet de gebonden waarde compatibel zijn met dat type.</span><span class="sxs-lookup"><span data-stu-id="84025-175">If a symbol is rebound later in the code, its type does not change, and the bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="84025-176">Rebinding van onveranderlijke symbolen</span><span class="sxs-lookup"><span data-stu-id="84025-176">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="84025-177">Een onveranderlijke variabele kan worden gekoppeld met behulp van een `set`-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-177">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="84025-178">Een herbinding bestaat uit het tref woord `set`, gevolgd door een symbool of symbool tuple, een gelijkteken `=`, een expressie waarmee de symbolen opnieuw worden verbonden en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="84025-178">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="84025-179">De waarde moet compatibel zijn met het type (n) van de symbolen waaraan deze is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="84025-179">The value must be compatible with the type(s) of the symbol(s) it is bound to.</span></span>

#### <a name="apply-and-reassign-statement"></a><span data-ttu-id="84025-180">Instructie apply-and-assign</span><span class="sxs-lookup"><span data-stu-id="84025-180">Apply-and-Reassign Statement</span></span>

<span data-ttu-id="84025-181">Een bepaald soort set-instructie waarnaar wordt verwezen als een instructie apply-and-reassign, biedt een handige manier om samen te voegen als de rechter kant bestaat uit de toepassing van een binaire operator en het resultaat moet worden gekoppeld aan het argument links voor de operator.</span><span class="sxs-lookup"><span data-stu-id="84025-181">A particular kind of set-statement we refer to as an apply-and-reassign statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="84025-182">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-182">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="84025-183">verhoogt de waarde van de teller `counter` in elke iteratie van de `for`-lus.</span><span class="sxs-lookup"><span data-stu-id="84025-183">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="84025-184">De bovenstaande code is gelijk aan</span><span class="sxs-lookup"><span data-stu-id="84025-184">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
<span data-ttu-id="84025-185">Soort gelijke instructies zijn beschikbaar voor alle binaire Opera tors waarin het type van de linkerkant van het expressie type overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="84025-185">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="84025-186">Dit biedt bijvoorbeeld een handige manier om waarden op te tellen:</span><span class="sxs-lookup"><span data-stu-id="84025-186">This provides for example a convenient way to accumulate values:</span></span>
```qsharp
mutable results = new Result[0];
for (qubit in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a><span data-ttu-id="84025-187">Instructie update-and-assign</span><span class="sxs-lookup"><span data-stu-id="84025-187">Update-and-Reassign Statement</span></span>

<span data-ttu-id="84025-188">Er bestaat een soort gelijke samen voeging voor expressies voor kopiëren en bijwerken aan de rechter kant.</span><span class="sxs-lookup"><span data-stu-id="84025-188">A similar concatenation exists for copy-and-update expressions on the right hand side.</span></span> <span data-ttu-id="84025-189">Daarnaast bestaan er instructies voor bijwerken en opnieuw toewijzen voor benoemde items in door de gebruiker gedefinieerde typen en voor matrix items.</span><span class="sxs-lookup"><span data-stu-id="84025-189">Correspondingly, update-and-reassign statements exist for named items in user-defined types as well as for array items.</span></span>  

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

<span data-ttu-id="84025-190">In het geval van matrices bevatten onze standaard bibliotheken de benodigde hulpprogram ma's voor veel algemene matrix initialisatie en bewerkings behoeften. zo voor komt u dat u matrix items in de eerste plaats hoeft bij te werken.</span><span class="sxs-lookup"><span data-stu-id="84025-190">In the case of arrays, our standard libraries contain the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> <span data-ttu-id="84025-191">Instructies update-en-reassign bieden een alternatief als dat nodig is:</span><span class="sxs-lookup"><span data-stu-id="84025-191">Update-and-reassign statements provide an alternative if needed:</span></span>

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
> <span data-ttu-id="84025-192">Vermijd onnodig gebruik van instructies voor bijwerken en opnieuw toewijzen met behulp van de hulpprogram ma's in <xref:microsoft.quantum.arrays>.</span><span class="sxs-lookup"><span data-stu-id="84025-192">Avoid unnecessary use of update-and-reassign statements by leveraging the tools provided in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="84025-193">De functie</span><span class="sxs-lookup"><span data-stu-id="84025-193">The function</span></span>
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
<span data-ttu-id="84025-194">u kunt bijvoorbeeld eenvoudig eenvoudiger met de functie `ConstantArray` in `Microsoft.Quantum.Arrays`en een Kopieer-en-update-expressie retour neren:</span><span class="sxs-lookup"><span data-stu-id="84025-194">for example can simply be simplified using the function `ConstantArray` in `Microsoft.Quantum.Arrays`, and returning a copy-and-update expression:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

### <a name="binding-scopes"></a><span data-ttu-id="84025-195">Bindings bereiken</span><span class="sxs-lookup"><span data-stu-id="84025-195">Binding Scopes</span></span>

<span data-ttu-id="84025-196">Over het algemeen gaan symbool bindingen zich buiten het bereik en worden ze niet meer aan het einde van het instructie blok weer gegeven waarin ze zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="84025-196">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="84025-197">Er zijn twee uitzonde ringen op deze regel:</span><span class="sxs-lookup"><span data-stu-id="84025-197">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="84025-198">De binding van de lus-variabele van een `for`-lus bevindt zich in het bereik van de hoofd tekst van de lus for, maar niet na het einde van de lus.</span><span class="sxs-lookup"><span data-stu-id="84025-198">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="84025-199">Alle drie delen van een `repeat`/`until` lus (de hoofd tekst, de test en de reparatie) worden behandeld als één bereik, waardoor symbolen die in de hoofd tekst zijn gebonden, beschikbaar zijn in de test en in de reparatie.</span><span class="sxs-lookup"><span data-stu-id="84025-199">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="84025-200">Voor beide typen lussen wordt elke pass-through-lus uitgevoerd in een eigen bereik, waardoor bindingen van een eerdere Passes niet meer beschikbaar zijn in een latere fase.</span><span class="sxs-lookup"><span data-stu-id="84025-200">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>

<span data-ttu-id="84025-201">Symbool bindingen van de buitenste blokken worden overgenomen door binnenste blokken.</span><span class="sxs-lookup"><span data-stu-id="84025-201">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="84025-202">Een symbool mag slechts eenmaal per blok zijn gebonden; het is niet toegestaan om een symbool te definiëren met dezelfde naam als een ander symbool dat zich binnen het bereik bevindt (geen "schaduw").</span><span class="sxs-lookup"><span data-stu-id="84025-202">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="84025-203">De volgende reeksen zijn juridisch:</span><span class="sxs-lookup"><span data-stu-id="84025-203">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="84025-204">en</span><span class="sxs-lookup"><span data-stu-id="84025-204">and</span></span>

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

<span data-ttu-id="84025-205">Maar dit is niet toegestaan:</span><span class="sxs-lookup"><span data-stu-id="84025-205">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="84025-206">Zo zou:</span><span class="sxs-lookup"><span data-stu-id="84025-206">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="control-flow"></a><span data-ttu-id="84025-207">Controlestroom</span><span class="sxs-lookup"><span data-stu-id="84025-207">Control Flow</span></span>

### <a name="for-loop"></a><span data-ttu-id="84025-208">For-lus</span><span class="sxs-lookup"><span data-stu-id="84025-208">For Loop</span></span>

<span data-ttu-id="84025-209">De instructie `for` ondersteunt herhalingen over een geheel getal of een matrix.</span><span class="sxs-lookup"><span data-stu-id="84025-209">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="84025-210">De instructie bestaat uit het tref woord `for`, een open haakje `(`, gevolgd door een symbool of symbool tuple, het tref woord `in`, een expressie van het type `Range` of matrix, een haakje sluiten `)`en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="84025-210">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="84025-211">Het instructie blok (de hoofd tekst van de lus) wordt herhaaldelijk uitgevoerd, met de gedefinieerde symbolen (een of meer lussen) die zijn gekoppeld aan elke waarde in het bereik of de matrix.</span><span class="sxs-lookup"><span data-stu-id="84025-211">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="84025-212">Houd er rekening mee dat als de expressie Range resulteert in een leeg bereik of een lege matrix, de hoofd tekst helemaal niet wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="84025-212">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="84025-213">De expressie is volledig geëvalueerd voordat de lus wordt ingevoerd en wordt niet gewijzigd terwijl de lus wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="84025-213">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="84025-214">De binding van de gedeclareerde symbolen is onveranderbaar en volgt dezelfde regels als andere variabele bindingen.</span><span class="sxs-lookup"><span data-stu-id="84025-214">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> <span data-ttu-id="84025-215">Het is met name mogelijk om de struct te ontleden, bijvoorbeeld om matrix items te bepalen voor een herhaling over een matrix bij toewijzing aan de lus-variabele (n).</span><span class="sxs-lookup"><span data-stu-id="84025-215">In particular, it is possible to destruct e.g. array items for an iteration over an array upon assignment to the loop variable(s).</span></span>

<span data-ttu-id="84025-216">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-216">For example,</span></span>

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

<span data-ttu-id="84025-217">De lus-variabele is bij elke toegang aan de hoofd tekst van de lus gebonden en ontbond aan het einde van de hoofd tekst.</span><span class="sxs-lookup"><span data-stu-id="84025-217">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="84025-218">Met name de lus-variabele is niet gebonden nadat de for-lus is voltooid.</span><span class="sxs-lookup"><span data-stu-id="84025-218">In particular, the loop variable is not bound after the for loop is completed.</span></span>

### <a name="repeat-until-success-loop"></a><span data-ttu-id="84025-219">Herhalen-tot-succes-lus</span><span class="sxs-lookup"><span data-stu-id="84025-219">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="84025-220">De instructie `repeat` ondersteunt het patroon ' herhalen tot geslaagd '.</span><span class="sxs-lookup"><span data-stu-id="84025-220">The `repeat` statement supports the quantum “repeat until success” pattern.</span></span>
<span data-ttu-id="84025-221">Het bestaat uit het tref woord `repeat`, gevolgd door een instructie blok (de hoofd tekst van de _lus_ ), het tref woord `until`, een booleaanse expressie en een scheidings punt of het tref woord `fixup` gevolgd door een ander instructie blok (de _reparatie_).</span><span class="sxs-lookup"><span data-stu-id="84025-221">It consists of the keyword `repeat`, followed by a statement block (the _loop_ body), the keyword `until`, a Boolean expression, and either a terminating semicolon or the keyword `fixup` followed by another statement block (the _fixup_).</span></span>
<span data-ttu-id="84025-222">De hoofd tekst van de lus, de voor waarde en de reparatie worden beschouwd als één bereik, dus de symbolen die in de hoofd tekst zijn gebonden, zijn beschikbaar in de voor waarde en correctie.</span><span class="sxs-lookup"><span data-stu-id="84025-222">The loop body, condition, and fixup are all considered to be a single scope, so symbols bound in the body are available in the condition and fixup.</span></span>

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

<span data-ttu-id="84025-223">De hoofd tekst van de lus wordt uitgevoerd en vervolgens wordt de voor waarde geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="84025-223">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="84025-224">Als de voor waarde waar is, wordt de instructie voltooid. anders wordt de reparatie uitgevoerd en wordt de instructie opnieuw uitgevoerd, te beginnen met de hoofd tekst van de lus.</span><span class="sxs-lookup"><span data-stu-id="84025-224">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>
<span data-ttu-id="84025-225">Houd er rekening mee dat het volt ooien van de uitvoering van de reparatie het bereik voor de instructie beëindigt, zodat symbool bindingen die zijn gemaakt tijdens de hoofd tekst of reparatie, niet beschikbaar zijn in volgende herhalingen.</span><span class="sxs-lookup"><span data-stu-id="84025-225">Note that completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="84025-226">De volgende code is bijvoorbeeld een Probabilistic-circuit waarmee een belang rijke rotatie poort wordt geïmplementeerd $V _3 = (\boldone + 2 i Z)/\sqrt{5}$ met behulp van de Hadamard en T-poorten.</span><span class="sxs-lookup"><span data-stu-id="84025-226">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the Hadamard and T gates.</span></span>
<span data-ttu-id="84025-227">De lus eindigt in $ \frac{8}{5}$ herhalingen op gemiddeld.</span><span class="sxs-lookup"><span data-stu-id="84025-227">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="84025-228">Zie [*herhalen-tot-geslaagd: niet-deterministische ontleding van single-Qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick en Svore, 2014) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84025-228">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for details.</span></span>

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
> <span data-ttu-id="84025-229">Vermijd het gebruik van herhalingen tot geslaagde lussen binnen functions.</span><span class="sxs-lookup"><span data-stu-id="84025-229">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="84025-230">De bijbehorende functionaliteit wordt gegeven door-lussen in-functies.</span><span class="sxs-lookup"><span data-stu-id="84025-230">The corresponding functionality is provided by while loops in functions.</span></span> 

### <a name="while-loop"></a><span data-ttu-id="84025-231">Lus while</span><span class="sxs-lookup"><span data-stu-id="84025-231">While Loop</span></span>

<span data-ttu-id="84025-232">Herhalen-tot-succes-patronen hebben een zeer Quantum specifieke connotation.</span><span class="sxs-lookup"><span data-stu-id="84025-232">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="84025-233">Ze worden veel gebruikt in bepaalde klassen van Quantum algoritmen, dus de speciale taal construct in Q #.</span><span class="sxs-lookup"><span data-stu-id="84025-233">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="84025-234">Lussen die op basis van een voor waarde worden uitgevoerd en waarvan de uitvoerings lengte daarom onbekend is tijdens de compilatie, moeten worden behandeld met een speciale Care in een Quantum runtime.</span><span class="sxs-lookup"><span data-stu-id="84025-234">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="84025-235">Het gebruik ervan in functions is niet probleemend, omdat deze alleen code bevatten die op conventionele hardware (niet-Quantum) wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="84025-235">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="84025-236">Q # ondersteunt daarom alleen het gebruik van while-lussen in-functies.</span><span class="sxs-lookup"><span data-stu-id="84025-236">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="84025-237">Een `while`-instructie bestaat uit het sleutel woord `while`, een haakje openen `(`, een voor waarde (een booleaanse expressie), een haakje sluiten `)`en een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="84025-237">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="84025-238">Het instructie blok (de hoofd tekst van de lus) wordt uitgevoerd zolang de voor waarde wordt geëvalueerd als `true`.</span><span class="sxs-lookup"><span data-stu-id="84025-238">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a><span data-ttu-id="84025-239">Voorwaardelijke instructie</span><span class="sxs-lookup"><span data-stu-id="84025-239">Conditional Statement</span></span>

<span data-ttu-id="84025-240">De instructie `if` ondersteunt voorwaardelijke uitvoering.</span><span class="sxs-lookup"><span data-stu-id="84025-240">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="84025-241">Het bestaat uit het tref woord `if`, een open haakje `(`, een Boole-expressie, een haakje sluiten `)`en een instructie blok (de _vervolgens_ blok kering).</span><span class="sxs-lookup"><span data-stu-id="84025-241">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="84025-242">Dit kan worden gevolgd door een wille keurig aantal else-if-componenten, die elk bestaan uit het tref woord `elif`, een open haakje `(`, een booleaanse expressie, een haakje sluiten `)`en een instructie blok (het _else-if-_ blok).</span><span class="sxs-lookup"><span data-stu-id="84025-242">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="84025-243">Ten slotte kan de instructie eventueel eindigen met een else-component, die bestaat uit het tref woord `else` gevolgd door een ander instructie blok (het _else_ -blok).</span><span class="sxs-lookup"><span data-stu-id="84025-243">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>
<span data-ttu-id="84025-244">De voor waarde wordt geëvalueerd, en als deze waar is, wordt de blok kering uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="84025-244">The condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="84025-245">Als de voor waarde ONWAAR is, wordt de eerste else-if-voor waarde geëvalueerd; Als de waarde True is, wordt het blok Else-If uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="84025-245">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="84025-246">Anders wordt het tweede else-if-blok getest en vervolgens de derde, enzovoort, totdat een component met de voor waarde True wordt aangetroffen of omdat er geen else-if-componenten zijn.</span><span class="sxs-lookup"><span data-stu-id="84025-246">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="84025-247">Als de component origineel als voor waarde en alle else-if resulteert in ONWAAR, wordt het else-blok uitgevoerd als er een is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="84025-247">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="84025-248">Houd er rekening mee dat welk blok wordt uitgevoerd in een eigen bereik.</span><span class="sxs-lookup"><span data-stu-id="84025-248">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="84025-249">Bindingen die zijn gemaakt binnen een then-, else-if-of else-blok zijn niet zichtbaar na het einde van de if-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-249">Bindings made inside of a then, else-if, or else block are not visible after the end of the if statement.</span></span>

<span data-ttu-id="84025-250">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-250">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
} 
```

<span data-ttu-id="84025-251">of</span><span class="sxs-lookup"><span data-stu-id="84025-251">or</span></span>

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a><span data-ttu-id="84025-252">Opvragen</span><span class="sxs-lookup"><span data-stu-id="84025-252">Return</span></span>

<span data-ttu-id="84025-253">De instructie return beëindigt de uitvoering van een bewerking of functie en retourneert een waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="84025-253">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="84025-254">Het bestaat uit het tref woord `return`, gevolgd door een expressie van het juiste type en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="84025-254">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="84025-255">Een aanroepable die een lege tuple retourneert, `()`, heeft geen instructie return nodig.</span><span class="sxs-lookup"><span data-stu-id="84025-255">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="84025-256">Als een vroege afsluiting gewenst is, kan `return ()` in dit geval worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="84025-256">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="84025-257">Callables die een wille keurig ander type retour neren, moeten een laatste Return-instructie hebben.</span><span class="sxs-lookup"><span data-stu-id="84025-257">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="84025-258">Er is geen maximum aantal retour instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="84025-258">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="84025-259">De compiler kan een waarschuwing verzenden als de instructies een instructie return in een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="84025-259">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="84025-260">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-260">For example,</span></span>

```qsharp
return 1;
```

<span data-ttu-id="84025-261">of</span><span class="sxs-lookup"><span data-stu-id="84025-261">or</span></span>

```qsharp
return ();
```

<span data-ttu-id="84025-262">of</span><span class="sxs-lookup"><span data-stu-id="84025-262">or</span></span>

```qsharp
return (results, qubits);
```

### <a name="fail"></a><span data-ttu-id="84025-263">Mislukt</span><span class="sxs-lookup"><span data-stu-id="84025-263">Fail</span></span>

<span data-ttu-id="84025-264">De instructie Fail beëindigt de uitvoering van een bewerking en retourneert een fout waarde naar de aanroeper.</span><span class="sxs-lookup"><span data-stu-id="84025-264">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="84025-265">Het bestaat uit het tref woord `fail`, gevolgd door een teken reeks en een punt komma.</span><span class="sxs-lookup"><span data-stu-id="84025-265">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="84025-266">De teken reeks wordt geretourneerd naar het klassieke stuur programma als het fout bericht.</span><span class="sxs-lookup"><span data-stu-id="84025-266">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="84025-267">Er is geen beperking voor het aantal mislukte instructies in een bewerking.</span><span class="sxs-lookup"><span data-stu-id="84025-267">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="84025-268">De compiler kan een waarschuwing verzenden als de instructies een mislukte instructie binnen een blok volgen.</span><span class="sxs-lookup"><span data-stu-id="84025-268">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="84025-269">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-269">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```

<span data-ttu-id="84025-270">of</span><span class="sxs-lookup"><span data-stu-id="84025-270">or</span></span>

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a><span data-ttu-id="84025-271">Qubit-beheer</span><span class="sxs-lookup"><span data-stu-id="84025-271">Qubit Management</span></span>

<span data-ttu-id="84025-272">Houd er rekening mee dat geen van deze instructies zijn toegestaan in de hoofd tekst van een functie.</span><span class="sxs-lookup"><span data-stu-id="84025-272">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="84025-273">Ze zijn alleen geldig in-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="84025-273">They are only valid within operations.</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="84025-274">Qubits opschonen</span><span class="sxs-lookup"><span data-stu-id="84025-274">Clean Qubits</span></span>

<span data-ttu-id="84025-275">De instructie `using` wordt gebruikt om nieuwe qubits te verkrijgen voor gebruik tijdens een instructie blok.</span><span class="sxs-lookup"><span data-stu-id="84025-275">The `using` statement is used to acquire new qubits for use during a statement block.</span></span>
<span data-ttu-id="84025-276">De qubits worden gegarandeerd geïnitialiseerd voor de reken `Zero`-status.</span><span class="sxs-lookup"><span data-stu-id="84025-276">The qubits are guaranteed to be initialized to the computational `Zero` state.</span></span>
<span data-ttu-id="84025-277">De qubits moet zich in de reken kundige `Zero` status bekomen aan het einde van het instructie blok; simulatoren worden aangemoedigd om dit af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="84025-277">The qubits should be in the computational `Zero` state at the end of the statement block; simulators are encouraged to enforce this.</span></span>

<span data-ttu-id="84025-278">De instructie bestaat uit het tref woord `using`, gevolgd door een haakje openen `(`, een binding, een haakje sluiten `)`en het instructie blok waarbinnen de qubits beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="84025-278">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="84025-279">De binding volgt hetzelfde patroon als `let`-instructies: een enkel symbool of een tuple van symbolen, gevolgd door een gelijkteken `=`en een enkele waarde of een overeenkomende tuple van initializers.</span><span class="sxs-lookup"><span data-stu-id="84025-279">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of initializers.</span></span>
<span data-ttu-id="84025-280">Initialisatie functies zijn beschikbaar voor één Qubit, aangeduid als `Qubit()`, of een matrix van qubits, aangegeven door `Qubit[`, een `Int`-expressie en `]`.</span><span class="sxs-lookup"><span data-stu-id="84025-280">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, indicated by `Qubit[`, an `Int` expression, and `]`.</span></span>

<span data-ttu-id="84025-281">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-281">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="borrowed-qubits"></a><span data-ttu-id="84025-282">Geleed qubits</span><span class="sxs-lookup"><span data-stu-id="84025-282">Borrowed Qubits</span></span>

<span data-ttu-id="84025-283">De instructie `borrowing` wordt gebruikt om qubits te verkrijgen voor tijdelijk gebruik.</span><span class="sxs-lookup"><span data-stu-id="84025-283">The `borrowing` statement is used to obtain qubits for temporary use.</span></span> <span data-ttu-id="84025-284">De instructie bestaat uit het tref woord `borrowing`, gevolgd door een haakje openen `(`, een binding, een haakje sluiten `)`en het instructie blok waarbinnen de qubits beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="84025-284">The statement consists of the keyword `borrowing`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="84025-285">De binding volgt hetzelfde patroon en dezelfde regels als in een `using`-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-285">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>

<span data-ttu-id="84025-286">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-286">For example,</span></span>

```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

<span data-ttu-id="84025-287">De geleende qubits bevinden zich in een onbekende status en het vervalt buiten het bereik aan het einde van het instructie blok.</span><span class="sxs-lookup"><span data-stu-id="84025-287">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="84025-288">De lenende door Voer om de qubits te verlaten in dezelfde staat waarin ze zich bevonden toen ze werden uitgeleend, d.w.z. hun status aan het begin en aan het einde van het blok van de verklaring, wordt naar verwachting hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="84025-288">The borrower commits to leaving the qubits in the same state they were in when they were borrowed, i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="84025-289">Deze status is in het bijzonder niet noodzakelijkerwijs een klassieke staat, zoals in de meeste gevallen, het lenen van scopes mag geen metingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="84025-289">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="84025-290">Bekijk [*factoring met behulp van 2n + 2 qubits met modulaire vermenigvuldiging op basis van Toffoli*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler en Svore 2017) voor een voor beeld van een geleend Qubit-gebruik.</span><span class="sxs-lookup"><span data-stu-id="84025-290">See [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an example of borrowed qubit use.</span></span>

<span data-ttu-id="84025-291">Wanneer qubits wordt uitgeleend, probeert het systeem eerst de aanvraag in te vullen vanuit qubits die in gebruik zijn, maar niet worden geopend tijdens de hoofd tekst van de `borrowing`-instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-291">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="84025-292">Als er onvoldoende qubits zijn, wordt er nieuwe qubits toegewezen om de aanvraag te volt ooien.</span><span class="sxs-lookup"><span data-stu-id="84025-292">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>

## <a name="conjugations"></a><span data-ttu-id="84025-293">Conjugations</span><span class="sxs-lookup"><span data-stu-id="84025-293">Conjugations</span></span>

<span data-ttu-id="84025-294">In tegens telling tot klassieke bits is het vrijgeven van Quantum geheugen iets resterend omdat het blind opnieuw instellen van qubits mogelijk ongewenste gevolgen heeft voor de resterende berekening als de qubits nog steeds Entangled zijn.</span><span class="sxs-lookup"><span data-stu-id="84025-294">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="84025-295">Dit kan worden vermeden door de uitgevoerde berekeningen op de juiste manier uit te voeren voordat het geheugen wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="84025-295">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="84025-296">Een gemeen schappelijk patroon in de Quantum Computing is daarom het volgende:</span><span class="sxs-lookup"><span data-stu-id="84025-296">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="84025-297">: Nieuw: vanaf onze 0,9-versie bieden we ondersteuning voor een conjugation-instructie die de bovenstaande trans formatie implementeert.</span><span class="sxs-lookup"><span data-stu-id="84025-297">:new: Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="84025-298">Met deze instructie kan de bewerkings `ApplyWith` op de volgende manier worden geïmplementeerd:</span><span class="sxs-lookup"><span data-stu-id="84025-298">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="84025-299">Een dergelijke conjugation-instructie is natuurlijk veel handiger als de buitenste en de binnenste trans formatie niet onmiddellijk beschikbaar zijn als bewerkingen, maar in plaats daarvan handiger zijn om te beschrijven door een blok bestaande uit verschillende instructies.</span><span class="sxs-lookup"><span data-stu-id="84025-299">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="84025-300">De inverse trans formatie voor de instructies die in het binnen-blok zijn gedefinieerd, wordt automatisch gegenereerd door de compiler en uitgevoerd nadat de Apply-Block is voltooid.</span><span class="sxs-lookup"><span data-stu-id="84025-300">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span> <span data-ttu-id="84025-301">Omdat alle onveranderlijke variabelen die als onderdeel van de binnen-blok kering worden gebruikt, niet in het apply-blok kunnen worden gebonden, is de gegenereerde trans formatie gegarandeerd de adjoint van de berekening in het binnen-blok.</span><span class="sxs-lookup"><span data-stu-id="84025-301">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="expression-evaluation-statements"></a><span data-ttu-id="84025-302">Expressie-evaluatie-instructies</span><span class="sxs-lookup"><span data-stu-id="84025-302">Expression Evaluation Statements</span></span>

<span data-ttu-id="84025-303">Een aanroep expressie van het type `Unit` kan worden gebruikt als een instructie.</span><span class="sxs-lookup"><span data-stu-id="84025-303">Any call expression of type `Unit` may be used as a statement.</span></span>
<span data-ttu-id="84025-304">Dit wordt voornamelijk gebruikt bij het aanroepen van bewerkingen op qubits die `Unit` retour neren, omdat het doel van de instructie is om de impliciete Quantum status te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="84025-304">This is primarily of use when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="84025-305">Voor expressie-evaluatie-instructies is een afsluit punt komma vereist.</span><span class="sxs-lookup"><span data-stu-id="84025-305">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="84025-306">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="84025-306">For example,</span></span>

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
