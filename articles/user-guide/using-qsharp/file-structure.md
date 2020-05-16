---
title: 'Q # bestands structuur'
description: 'Hierin worden de structuur en syntaxis van een Q #-bestand beschreven.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: cbee92c6d7e765237a7a42532dd7012b51421708
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430965"
---
# <a name="q-file-structure"></a><span data-ttu-id="30188-103">Q # bestands structuur</span><span class="sxs-lookup"><span data-stu-id="30188-103">Q# File Structure</span></span>

<span data-ttu-id="30188-104">Elke Q #-bewerking,-functie en een door de gebruiker gedefinieerd type worden binnen een naam ruimte gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="30188-104">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>

<span data-ttu-id="30188-105">Een Q #-bestand bestaat uit een reeks *naam ruimte declaraties*.</span><span class="sxs-lookup"><span data-stu-id="30188-105">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="30188-106">Elke naam ruimte declaratie bevat declaraties voor door de gebruiker gedefinieerde typen, bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="30188-106">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="30188-107">Een naam ruimte declaratie kan elk wille keurig aantal van elk type declaratie en in een wille keurige volg orde bevatten.</span><span class="sxs-lookup"><span data-stu-id="30188-107">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="30188-108">Volg deze koppelingen voor meer informatie over het declareren van door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.guide.types#user-defined-types), [bewerkingen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)en [functies](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) binnen een naam ruimte.</span><span class="sxs-lookup"><span data-stu-id="30188-108">Follow these links for more details on declaring [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) within a namespace.</span></span>

<span data-ttu-id="30188-109">De enige tekst die buiten een naam ruimte declaratie kan worden weer gegeven, is opmerkingen.</span><span class="sxs-lookup"><span data-stu-id="30188-109">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="30188-110">In het bijzonder worden documentatie opmerkingen (meer details hieronder) voor een naam ruimte voorafgaat aan de declaratie.</span><span class="sxs-lookup"><span data-stu-id="30188-110">In particular, documentation comments (more details below) for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="30188-111">Naam ruimte declaraties</span><span class="sxs-lookup"><span data-stu-id="30188-111">Namespace Declarations</span></span>

<span data-ttu-id="30188-112">Een Q #-bestand heeft normaal gesp roken precies één naam ruimte declaratie, maar kan geen hebben (en mag niet leeg zijn of alleen opmerkingen bevatten) of kan meerdere naam ruimten bevatten.</span><span class="sxs-lookup"><span data-stu-id="30188-112">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="30188-113">Naam ruimte declaraties mogen niet worden genest.</span><span class="sxs-lookup"><span data-stu-id="30188-113">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="30188-114">Dezelfde naam ruimte kan worden gedeclareerd in meerdere Q #-bestanden die samen worden gecompileerd, zolang er geen type, bewerking of functie declaraties met dezelfde naam zijn.</span><span class="sxs-lookup"><span data-stu-id="30188-114">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="30188-115">Het is met name ongeldig om hetzelfde type in dezelfde naam ruimte in meerdere bestanden te definiëren, zelfs als de declaraties identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="30188-115">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="30188-116">Een naam ruimte declaratie bestaat uit het tref woord `namespace` , gevolgd door de naam van de naam ruimte, een open accolade `{` , de declaraties in de naam ruimte en een sluitings accolade `}` .</span><span class="sxs-lookup"><span data-stu-id="30188-116">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="30188-117">Naam ruimte namen volgen het .NET-patroon van een reeks van een of meer juridische symbolen, gescheiden door punten `.` .</span><span class="sxs-lookup"><span data-stu-id="30188-117">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="30188-118">`MyQuantumStuff`En `Microsoft.Quantum.Intrinsic` zijn bijvoorbeeld geldige naam ruimte namen.</span><span class="sxs-lookup"><span data-stu-id="30188-118">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="30188-119">Per Conventie worden de symbolen in de naam van een naam ruimte gekapitaliseerd, maar dit is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="30188-119">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="30188-120">Verwijzingen naar typen of callables die verder in een bestand worden aangegeven, worden op de juiste wijze opgelost. het is niet nodig om een verwijzing naar het type, de bewerking of de functie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30188-120">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="30188-121">Open instructies</span><span class="sxs-lookup"><span data-stu-id="30188-121">Open Directives</span></span>

<span data-ttu-id="30188-122">Binnen een naam ruimte blok `open` kan de instructie worden gebruikt voor het importeren van alle typen en callables die zijn gedeclareerd in een bepaalde naam ruimte en deze te raadplegen op basis van de niet-gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="30188-122">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="30188-123">Een dergelijke `open` richt lijn bestaat uit het `open` tref woord, gevolgd door de naam ruimte die moet worden geopend en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="30188-123">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="30188-124">Alle `open` instructies moeten voor alle `function` , `operation` of `newtype` declaraties in het naam ruimte blok worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="30188-124">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="30188-125">Een korte naam voor de naam ruimte kan eventueel worden gedefinieerd, zodat alle elementen van die naam ruimte kunnen (en moeten) worden gekwalificeerd door de gedefinieerde korte naam.</span><span class="sxs-lookup"><span data-stu-id="30188-125">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="30188-126">Als u bijvoorbeeld de volgende naam ruimte declaratie en open instructies hebt opgegeven,</span><span class="sxs-lookup"><span data-stu-id="30188-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="30188-127">Als voor een bewerking die we declareren een bewerking wordt gebruikt `Op` `Microsoft.Quantum.Intrinsic` , wordt deze aangeroepen door eenvoudigweg te gebruiken `Op` .</span><span class="sxs-lookup"><span data-stu-id="30188-127">if an operation we declare uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, we would call it by simply using `Op`.</span></span>
<span data-ttu-id="30188-128">Als we echter een bepaalde functie willen aanroepen `Fn` vanuit `Microsoft.Quantum.Math` , moeten we deze aanroepen met `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="30188-128">However, if we wanted a call a certain function `Fn` from `Microsoft.Quantum.Math`, we would need to call it using `Math.Fn`.</span></span>

<span data-ttu-id="30188-129">De `open` instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.</span><span class="sxs-lookup"><span data-stu-id="30188-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="30188-130">Als we een extra naam ruimte in hetzelfde Q #-bestand als hierboven hadden gedefinieerd `NS` , hebben alle bewerkingen/functies/typen die zijn gedefinieerd in de tweede naam ruimte, geen toegang tot niets van `Microsoft.Quantum.Intrinsic` of `Microsoft.Quantum.Math` , tenzij we de open instructies daarin hebben herhaald.</span><span class="sxs-lookup"><span data-stu-id="30188-130">Hence, if we were to define an additional namespace in the same Q# file as `NS` above, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless we repeated the open directives therein.</span></span> 

<span data-ttu-id="30188-131">Er moet naar een type of aanroepbaar worden gedefinieerd in een andere naam ruimte die *niet* in de huidige naam ruimte wordt geopend, met de volledig gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="30188-131">A type or callable defined in another namespace that is *not* opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="30188-132">Bijvoorbeeld: er `Op` moet naar een bewerking met de naam van de `X.Y` naam ruimte worden verwezen met de volledig gekwalificeerde naam `X.Y.Op` , tenzij de `X.Y` naam ruimte eerder in het huidige blok is geopend.</span><span class="sxs-lookup"><span data-stu-id="30188-132">For example, an operation named `Op` from the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="30188-133">Zoals eerder vermeld, `X` is het niet mogelijk om te verwijzen naar de bewerking, zelfs als de naam ruimte is geopend `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="30188-133">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="30188-134">Als er een korte naam `Z` voor `X.Y` is gedefinieerd in die naam ruimte en het bestand, `Op` moet worden aangeduid als `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="30188-134">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

<span data-ttu-id="30188-135">Het is doorgaans beter om een naam ruimte op te neemen met behulp van een `open` instructie.</span><span class="sxs-lookup"><span data-stu-id="30188-135">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="30188-136">Het gebruik van een volledig gekwalificeerde naam is vereist als twee naam ruimten constructies met dezelfde naam definiëren. voor de huidige bron worden constructies van beide gebruikt.</span><span class="sxs-lookup"><span data-stu-id="30188-136">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="30188-137">Q # volgt dezelfde regels als voor naam als andere .NET-talen.</span><span class="sxs-lookup"><span data-stu-id="30188-137">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="30188-138">Q # biedt echter geen ondersteuning voor relatieve verwijzingen naar naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="30188-138">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="30188-139">Als de naam ruimte is `a.b` geopend, wordt een verwijzing naar een bewerking met de naam `c.d` *niet* omgezet naar een bewerking met een volledige naam `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="30188-139">That is, if the namespace `a.b` has been opened, a reference to an operation named `c.d` will *not* be resolved to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="30188-140">Opmaak</span><span class="sxs-lookup"><span data-stu-id="30188-140">Formatting</span></span>

<span data-ttu-id="30188-141">De meeste Q #-instructies en de instructies eindigen met een punt komma, `;` .</span><span class="sxs-lookup"><span data-stu-id="30188-141">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="30188-142">Instructies en declaraties, zoals `for` en `operation` die eindigen op een instructie blok (zie hieronder), vereisen geen afsluitende punt komma.</span><span class="sxs-lookup"><span data-stu-id="30188-142">Statements and declarations such as `for` and `operation` that end with a statement block (see below) do not require a terminating semicolon.</span></span>
<span data-ttu-id="30188-143">Elke instructie bevat een beschrijving van de vraag of de afsluit punt komma is vereist.</span><span class="sxs-lookup"><span data-stu-id="30188-143">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="30188-144">Instructies, zoals expressies, declaraties en instructies, kunnen worden verdeeld over meerdere regels.</span><span class="sxs-lookup"><span data-stu-id="30188-144">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="30188-145">Meerdere instructies op één regel moeten worden vermeden.</span><span class="sxs-lookup"><span data-stu-id="30188-145">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="30188-146">Instructie blokken</span><span class="sxs-lookup"><span data-stu-id="30188-146">Statement Blocks</span></span>

<span data-ttu-id="30188-147">Q #-instructies worden gegroepeerd in instructie blokken.</span><span class="sxs-lookup"><span data-stu-id="30188-147">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="30188-148">Een instructie blok begint met het openen `{` en eindigen met een afsluiting `}` .</span><span class="sxs-lookup"><span data-stu-id="30188-148">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="30188-149">Een overzichts blok dat is inge sloten in een ander blok, wordt beschouwd als een subblok van het container blok; contains-en sub-blokken worden ook outer-en Inner-blokken genoemd.</span><span class="sxs-lookup"><span data-stu-id="30188-149">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="30188-150">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="30188-150">Comments</span></span>

<span data-ttu-id="30188-151">Opmerkingen beginnen met twee slashes `//` en door gaan tot het einde van de regel.</span><span class="sxs-lookup"><span data-stu-id="30188-151">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="30188-152">Een opmerking kan ergens in een Q #-bron bestand worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="30188-152">A comment may appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="30188-153">Documentatie opmerkingen</span><span class="sxs-lookup"><span data-stu-id="30188-153">Documentation Comments</span></span>

<span data-ttu-id="30188-154">Opmerkingen die beginnen met drie slashes, `///` worden speciaal door de compiler behandeld wanneer ze direct vóór een naam ruimte, bewerking, specialisatie, functie of type definitie worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="30188-154">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="30188-155">In dat geval wordt de inhoud ervan als documentatie voor het gedefinieerde aanroepende of door de gebruiker gedefinieerde type beschouwd, net als bij andere .NET-talen.</span><span class="sxs-lookup"><span data-stu-id="30188-155">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="30188-156">Binnen `///` opmerkingen wordt tekst die als onderdeel van de API-documentatie moet worden weer gegeven, opgemaakt als een [prijs](https://daringfireball.net/projects/markdown/syntax)opgave, waarbij verschillende delen van de documentatie worden aangegeven door een speciaal benoemde koptekst.</span><span class="sxs-lookup"><span data-stu-id="30188-156">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="30188-157">Als uitbrei ding om te kunnen worden genoteerd, kunnen kruis verwijzingen naar bewerkingen, functies en door de gebruiker gedefinieerde typen in Q # worden opgenomen met behulp `@"<ref target>"` van de, waar `<ref target>` wordt vervangen door de volledig gekwalificeerde naam van het code object waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="30188-157">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="30188-158">Een documentatie-engine kan eventueel ook extra kortings uitbreidingen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="30188-158">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="30188-159">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="30188-159">For example:</span></span>

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

<span data-ttu-id="30188-160">De volgende namen worden herkend als documentatie opmerkings koppen.</span><span class="sxs-lookup"><span data-stu-id="30188-160">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="30188-161">**Samen vatting**: een korte samen vatting van het gedrag van een functie of bewerking, of van het doel van een type.</span><span class="sxs-lookup"><span data-stu-id="30188-161">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="30188-162">De eerste alinea van de samen vatting wordt gebruikt voor het aanwijzen van informatie.</span><span class="sxs-lookup"><span data-stu-id="30188-162">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="30188-163">Dit moet tekst zonder opmaak zijn.</span><span class="sxs-lookup"><span data-stu-id="30188-163">It should be plain text.</span></span>
- <span data-ttu-id="30188-164">**Beschrijving**: een beschrijving van het gedrag van een functie of bewerking, of van het doel van een type.</span><span class="sxs-lookup"><span data-stu-id="30188-164">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="30188-165">De samen vatting en beschrijving worden samengevoegd om het gegenereerde documentatie bestand te vormen voor de functie, bewerking of het type.</span><span class="sxs-lookup"><span data-stu-id="30188-165">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="30188-166">De beschrijving mag in-line-symbolen en-vergelijkingen in LaTeX-indeling bevatten.</span><span class="sxs-lookup"><span data-stu-id="30188-166">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="30188-167">**Invoer**: een beschrijving van de invoer-tuple voor een bewerking of functie.</span><span class="sxs-lookup"><span data-stu-id="30188-167">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="30188-168">Kan aanvullende subsecties van de korting bevatten die elk afzonderlijk element van de invoer-tuple aangeven.</span><span class="sxs-lookup"><span data-stu-id="30188-168">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="30188-169">**Output**: een beschrijving van de tuple die wordt geretourneerd door een bewerking of functie.</span><span class="sxs-lookup"><span data-stu-id="30188-169">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="30188-170">**Type parameters**: een lege sectie die één extra subsectie bevat voor elke algemene type parameter.</span><span class="sxs-lookup"><span data-stu-id="30188-170">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="30188-171">**Voor beeld**: een kort voor beeld van het gebruik van de bewerking, functie of het type.</span><span class="sxs-lookup"><span data-stu-id="30188-171">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="30188-172">**Opmerkingen**: diverse Prose die een aspect van de bewerking, functie of type beschrijven.</span><span class="sxs-lookup"><span data-stu-id="30188-172">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="30188-173">**Zie ook**: een lijst met volledig gekwalificeerde namen die betrekking hebben op gerelateerde functies, bewerkingen of door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="30188-173">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="30188-174">**Verwijzingen**: een lijst met verwijzingen en bron vermeldingen voor het item dat wordt gedocumenteerd.</span><span class="sxs-lookup"><span data-stu-id="30188-174">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="whats-next"></a><span data-ttu-id="30188-175">Hoe nu verder?</span><span class="sxs-lookup"><span data-stu-id="30188-175">What's Next?</span></span>
<span data-ttu-id="30188-176">Meer informatie over [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions) in Q #.</span><span class="sxs-lookup"><span data-stu-id="30188-176">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>