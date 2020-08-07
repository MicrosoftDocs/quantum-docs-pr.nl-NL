---
title: Q#Bestands structuur
description: Hierin worden de structuur en syntaxis van een Q# bestand beschreven.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
no-loc:
- Q#
- $$v
ms.openlocfilehash: ac73962b1a718cd04aa87ee3476c66781fe3ac2b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867927"
---
# <a name="no-locq-file-structure"></a><span data-ttu-id="a8246-103">Q#Bestands structuur</span><span class="sxs-lookup"><span data-stu-id="a8246-103">Q# File Structure</span></span>

<span data-ttu-id="a8246-104">Een Q# bestand bestaat uit een reeks *naam ruimte declaraties*.</span><span class="sxs-lookup"><span data-stu-id="a8246-104">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="a8246-105">Elke naam ruimte declaratie bevat declaraties voor door de gebruiker gedefinieerde typen, bewerkingen en functies en kan een wille keurig aantal van elk type declaratie en een wille keurige volg orde bevatten.</span><span class="sxs-lookup"><span data-stu-id="a8246-105">Each namespace declaration contains declarations for user-defined types, operations, and functions, and can contain any number of each type of declaration and in any order.</span></span>
<span data-ttu-id="a8246-106">Zie door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.guide.types#user-defined-types), [bewerkingen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)en [functies](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions)voor meer informatie over declaraties in een naam ruimte.</span><span class="sxs-lookup"><span data-stu-id="a8246-106">For more information on declarations within a namespace, see [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span></span>

<span data-ttu-id="a8246-107">De enige tekst die buiten een naam ruimte declaratie kan worden weer gegeven, is opmerkingen.</span><span class="sxs-lookup"><span data-stu-id="a8246-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="a8246-108">In het bijzonder worden documentatie opmerkingen voor een naam ruimte voorafgaat aan de declaratie.</span><span class="sxs-lookup"><span data-stu-id="a8246-108">In particular, documentation comments for a namespace precede the declaration.</span></span> <span data-ttu-id="a8246-109">Zie voor meer informatie [documentatie opmerkingen](#documentation-comments) in dit artikel.</span><span class="sxs-lookup"><span data-stu-id="a8246-109">For more information, see [Documentation comments](#documentation-comments) in this article.</span></span> 

## <a name="namespace-declarations"></a><span data-ttu-id="a8246-110">Naam ruimte declaraties</span><span class="sxs-lookup"><span data-stu-id="a8246-110">Namespace Declarations</span></span>

<span data-ttu-id="a8246-111">Een Q# bestand heeft doorgaans slechts één naam ruimte declaratie, maar kan geen (en leeg zijn of alleen opmerkingen bevatten) of meerdere naam ruimten bevatten.</span><span class="sxs-lookup"><span data-stu-id="a8246-111">A Q# file typically has just one namespace declaration, but could have none (and be empty or just contain comments) or could contain multiple namespaces.</span></span>
<span data-ttu-id="a8246-112">Naam ruimte declaraties kunnen niet worden genest.</span><span class="sxs-lookup"><span data-stu-id="a8246-112">Namespace declarations can not be nested.</span></span>

<span data-ttu-id="a8246-113">U kunt dezelfde naam ruimte declareren in meerdere Q# bestanden die samen worden gecompileerd, zolang er geen type, bewerking of functie declaraties met dezelfde naam zijn.</span><span class="sxs-lookup"><span data-stu-id="a8246-113">You can declare the same namespace in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="a8246-114">Het is met name ongeldig om hetzelfde type in dezelfde naam ruimte in meerdere bestanden te definiëren, zelfs als de declaraties identiek zijn.</span><span class="sxs-lookup"><span data-stu-id="a8246-114">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="a8246-115">Een naam ruimte declaratie bestaat uit het tref woord `namespace` , gevolgd door de naam van de naam ruimte en de declaraties in de naam ruimte tussen accolades `{ }` .</span><span class="sxs-lookup"><span data-stu-id="a8246-115">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, and the declarations contained in the namespace enclosed in braces `{ }`.</span></span>
<span data-ttu-id="a8246-116">Naam ruimte namen volgen het .NET-patroon van een reeks van een of meer juridische symbolen, gescheiden door punten `.` .</span><span class="sxs-lookup"><span data-stu-id="a8246-116">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="a8246-117">`MyQuantumStuff`En `Microsoft.Quantum.Intrinsic` zijn bijvoorbeeld geldige naam ruimte namen.</span><span class="sxs-lookup"><span data-stu-id="a8246-117">For example, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="a8246-118">In de conventies is het echter niet vereist om de symbolen in de naam van een naam ruimte te kapitaliseren.</span><span class="sxs-lookup"><span data-stu-id="a8246-118">By convention, capitalize the symbols in a namespace name, however, this is not required.</span></span>

<span data-ttu-id="a8246-119">Verwijzingen naar typen of callables die verder worden gedeclareerd in een bestand, worden correct omgezet. het is niet nodig om een verwijzing naar het type, de bewerking of de functie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a8246-119">References to types or callables declared further down in a file resolve properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="a8246-120">Open instructies</span><span class="sxs-lookup"><span data-stu-id="a8246-120">Open Directives</span></span>

<span data-ttu-id="a8246-121">In een naam ruimte blok gebruikt `open` u de instructie om alle typen en callables te importeren die zijn gedeclareerd in een bepaalde naam ruimte en deze te raadplegen op basis van de niet-gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="a8246-121">Within a namespace block, use the `open` directive to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="a8246-122">Een dergelijke `open` richt lijn bestaat uit het `open` tref woord, gevolgd door de naam ruimte die moet worden geopend en een punt komma als scheidings tekens.</span><span class="sxs-lookup"><span data-stu-id="a8246-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="a8246-123">Alle `open` instructies moeten voor alle `function` , `operation` of `newtype` declaraties in het naam ruimte blok worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="a8246-123">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="a8246-124">U kunt desgewenst een korte naam definiëren voor de naam ruimte die u hebt geopend.</span><span class="sxs-lookup"><span data-stu-id="a8246-124">Optionally, you can define a short name for the opened namespace.</span></span> <span data-ttu-id="a8246-125">Als er een korte naam is gedefinieerd, moet u alle elementen uit die naam ruimte kwalificeren met de gedefinieerde korte naam.</span><span class="sxs-lookup"><span data-stu-id="a8246-125">If a short name is defined, you must qualify all elements from that namespace by the defined short name.</span></span> <span data-ttu-id="a8246-126">Als u bijvoorbeeld de volgende naam ruimte declaratie en open instructies hebt opgegeven,</span><span class="sxs-lookup"><span data-stu-id="a8246-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="a8246-127">Als een gedeclareerde bewerking gebruikmaakt `Op` van een bewerking vanuit `Microsoft.Quantum.Intrinsic` , kunt u deze aanroepen door eenvoudigweg te gebruiken `Op` .</span><span class="sxs-lookup"><span data-stu-id="a8246-127">if a declared operation uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, you call it by simply using `Op`.</span></span>
<span data-ttu-id="a8246-128">Als u echter een bepaalde functie wilt aanroepen `Fn` vanuit `Microsoft.Quantum.Math` , moet u deze aanroepen met `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="a8246-128">However, to call a certain function `Fn` from `Microsoft.Quantum.Math`, you must call it using `Math.Fn`.</span></span>

<span data-ttu-id="a8246-129">De `open` instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.</span><span class="sxs-lookup"><span data-stu-id="a8246-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="a8246-130">Als u dus een extra naam ruimte in hetzelfde bestand definieert Q# als `NS` eerder, hebben alle bewerkingen/functies/typen die zijn gedefinieerd in de tweede naam ruimte, geen toegang tot niets van `Microsoft.Quantum.Intrinsic` of `Microsoft.Quantum.Math` tenzij u de open instructies daarin hebt herhaald.</span><span class="sxs-lookup"><span data-stu-id="a8246-130">Hence, if you define an additional namespace in the same Q# file as `NS` earlier, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless you repeated the open directives therein.</span></span> 

<span data-ttu-id="a8246-131">Als u wilt verwijzen naar een type of aanroepable dat is gedefinieerd in een andere naam ruimte die *niet* in de huidige naam ruimte wordt geopend, moet u ernaar verwijzen met de volledig gekwalificeerde naam.</span><span class="sxs-lookup"><span data-stu-id="a8246-131">To reference a type or callable defined in another namespace that is *not* opened in the current namespace, you must reference it by its fully-qualified name.</span></span>
<span data-ttu-id="a8246-132">Een voor beeld van een bewerking `Op` met de naam van de `X.Y` naam ruimte:</span><span class="sxs-lookup"><span data-stu-id="a8246-132">For example, given an operation named `Op` from the `X.Y` namespace:</span></span>

* <span data-ttu-id="a8246-133">U moet ernaar verwijzen met de volledig gekwalificeerde naam `X.Y.Op` , tenzij de `X.Y` naam ruimte eerder in het huidige blok is geopend.</span><span class="sxs-lookup"><span data-stu-id="a8246-133">You must reference it by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> 
* <span data-ttu-id="a8246-134">Zelfs als de `X` naam ruimte wordt geopend, is het niet mogelijk om te verwijzen naar de bewerking als `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="a8246-134">Even if the `X` namespace is opened, it is not possible to reference the operation as `Y.Op`.</span></span>
* <span data-ttu-id="a8246-135">Als u de korte naam `Z` voor `X.Y` in die naam ruimte en het bestand hebt gedefinieerd, moet u verwijzen naar `Op` `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="a8246-135">If you defined the short name `Z` for `X.Y` in that namespace and file, you must reference `Op` as `Z.Op`.</span></span> 

<span data-ttu-id="a8246-136">Het is doorgaans beter om een naam ruimte op te neemen met behulp van een `open` instructie.</span><span class="sxs-lookup"><span data-stu-id="a8246-136">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="a8246-137">Het gebruik van een volledig gekwalificeerde naam is vereist als twee naam ruimten constructies met dezelfde naam definiëren. voor de huidige bron worden constructies van beide gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a8246-137">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="a8246-138">Q#volgt dezelfde regels als voor naam als andere .NET-talen.</span><span class="sxs-lookup"><span data-stu-id="a8246-138">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="a8246-139">Biedt echter Q# geen ondersteuning voor relatieve verwijzingen naar naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="a8246-139">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="a8246-140">Als de naam ruimte bijvoorbeeld `a.b` is geopend, wordt een verwijzing naar een bewerking met de naam `c.d` *niet* omgezet naar een bewerking met een volledige naam `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="a8246-140">For example, if the namespace `a.b` is open, a reference to an operation named `c.d` does *not* resolve to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="a8246-141">Opmaak</span><span class="sxs-lookup"><span data-stu-id="a8246-141">Formatting</span></span>

<span data-ttu-id="a8246-142">Q#De meeste instructies en instructies eindigen met een punt komma, `;` .</span><span class="sxs-lookup"><span data-stu-id="a8246-142">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="a8246-143">Instructies en declaraties, zoals `for` en `operation` die eindigen op een instructie blok (Zie de volgende sectie), vereisen geen afsluitende punt komma.</span><span class="sxs-lookup"><span data-stu-id="a8246-143">Statements and declarations such as `for` and `operation` that end with a statement block (see the following section) do not require a terminating semicolon.</span></span>
<span data-ttu-id="a8246-144">Elke instructie bevat een beschrijving van de vraag of de afsluit punt komma is vereist.</span><span class="sxs-lookup"><span data-stu-id="a8246-144">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="a8246-145">Instructies, zoals expressies, declaraties en instructies, kunnen worden verdeeld over meerdere regels.</span><span class="sxs-lookup"><span data-stu-id="a8246-145">Statements, like expressions, declarations, and directives, can be broken out across multiple lines.</span></span>
<span data-ttu-id="a8246-146">Vermijd het plaatsen van meerdere instructies op één regel.</span><span class="sxs-lookup"><span data-stu-id="a8246-146">Avoid putting multiple statements on a single line.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="a8246-147">Instructie blokken</span><span class="sxs-lookup"><span data-stu-id="a8246-147">Statement Blocks</span></span>

<span data-ttu-id="a8246-148">Q#instructies worden gegroepeerd in instructie blokken, die zijn opgenomen in accolades `{ }` .</span><span class="sxs-lookup"><span data-stu-id="a8246-148">Q# statements are grouped into statement blocks, which are contained with braces `{ }`.</span></span> <span data-ttu-id="a8246-149">Een instructie blok begint met het openen `{` en eindigen met een afsluiting `}` .</span><span class="sxs-lookup"><span data-stu-id="a8246-149">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="a8246-150">Een overzichts blok dat is inge sloten in een ander blok, wordt beschouwd als een subblok van het container blok; contains-en sub-blokken worden ook outer-en Inner-blokken genoemd.</span><span class="sxs-lookup"><span data-stu-id="a8246-150">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="a8246-151">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a8246-151">Comments</span></span>

<span data-ttu-id="a8246-152">Opmerkingen beginnen met twee slashes `//` en door gaan tot het einde van de regel.</span><span class="sxs-lookup"><span data-stu-id="a8246-152">Comments begin with two forward slashes, `//`, and continue until the end of the line.</span></span>
<span data-ttu-id="a8246-153">Een opmerking kan ergens in een bron bestand worden weer gegeven Q# .</span><span class="sxs-lookup"><span data-stu-id="a8246-153">A comment can appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="a8246-154">Documentatie opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a8246-154">Documentation Comments</span></span>

<span data-ttu-id="a8246-155">Opmerkingen die beginnen met drie slashes, `///` worden speciaal door de compiler behandeld wanneer ze direct vóór een naam ruimte, bewerking, specialisatie, functie of type definitie worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="a8246-155">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="a8246-156">In dat geval behandelt de compiler ze als documentatie voor het gedefinieerde aanroep bare of door de gebruiker gedefinieerde type, hetzelfde als andere .NET-talen.</span><span class="sxs-lookup"><span data-stu-id="a8246-156">In that case, the compiler treats them as documentation for the defined callable or user-defined type, the same as other .NET languages.</span></span>

<span data-ttu-id="a8246-157">In `///` opmerkingen wordt tekst die als onderdeel van de API-documentatie moet worden weer gegeven, opgemaakt als een [prijs](https://daringfireball.net/projects/markdown/syntax)opgave, met verschillende delen van de documentatie die worden aangegeven door een speciaal benoemde koptekst.</span><span class="sxs-lookup"><span data-stu-id="a8246-157">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation indicated by specially-named headers.</span></span>
<span data-ttu-id="a8246-158">Gebruik in de prijs van de `@"<ref target>"` uitbrei ding voor kruis verwijzings bewerkingen, functies en door de gebruiker gedefinieerde typen in Q# .</span><span class="sxs-lookup"><span data-stu-id="a8246-158">In Markdown, use the `@"<ref target>"` extension to cross-reference operations, functions, and user-defined types in Q#.</span></span> <span data-ttu-id="a8246-159">Vervang door `<ref target>` de volledig gekwalificeerde naam van het code object waarnaar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="a8246-159">Replace `<ref target>` with the fully qualified name of the referenced code object.</span></span>
<span data-ttu-id="a8246-160">Andere documentatie-engines kunnen ook extra kortings uitbreidingen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="a8246-160">Different documentation engines may also support additional Markdown extensions.</span></span>

<span data-ttu-id="a8246-161">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="a8246-161">For example:</span></span>

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

<span data-ttu-id="a8246-162">De volgende namen zijn geldig als documentatie opmerkings koppen.</span><span class="sxs-lookup"><span data-stu-id="a8246-162">The following names are valid as documentation comment headers.</span></span>

- <span data-ttu-id="a8246-163">**Samen vatting**: een korte samen vatting van het gedrag van een functie of bewerking, of het doel van een type.</span><span class="sxs-lookup"><span data-stu-id="a8246-163">**Summary**: A short summary of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="a8246-164">De eerste alinea van de samen vatting wordt gebruikt voor het aanwijzen van informatie.</span><span class="sxs-lookup"><span data-stu-id="a8246-164">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="a8246-165">Dit moet tekst zonder opmaak zijn.</span><span class="sxs-lookup"><span data-stu-id="a8246-165">It should be plain text.</span></span>
- <span data-ttu-id="a8246-166">**Beschrijving**: een beschrijving van het gedrag van een functie of bewerking, of het doel van een type.</span><span class="sxs-lookup"><span data-stu-id="a8246-166">**Description**: A description of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="a8246-167">De samen vatting en beschrijving vormen samen het gegenereerde documentatie bestand voor de functie, bewerking of het type.</span><span class="sxs-lookup"><span data-stu-id="a8246-167">Together, the summary and description form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="a8246-168">De beschrijving ondersteunt de in-line in LaTeX ingedeelde symbolen en vergelijkingen.</span><span class="sxs-lookup"><span data-stu-id="a8246-168">The description supports in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="a8246-169">**Invoer**: een beschrijving van de invoer-tuple voor een bewerking of functie.</span><span class="sxs-lookup"><span data-stu-id="a8246-169">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="a8246-170">Kan aanvullende subsecties van de korting bevatten die elk element van de invoer-tuple aangeven.</span><span class="sxs-lookup"><span data-stu-id="a8246-170">Can contain additional Markdown subsections indicating each element of the input tuple.</span></span>
- <span data-ttu-id="a8246-171">**Output**: een beschrijving van de tuple die wordt geretourneerd door een bewerking of functie.</span><span class="sxs-lookup"><span data-stu-id="a8246-171">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="a8246-172">**Type para meters**: een lege sectie die één extra subsectie bevat voor elke algemene type parameter.</span><span class="sxs-lookup"><span data-stu-id="a8246-172">**Type Parameters**: An empty section that contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="a8246-173">**Voor beeld**: een kort voor beeld van het gebruik van de bewerking, functie of het type.</span><span class="sxs-lookup"><span data-stu-id="a8246-173">**Example**: A short example of the operation, function, or type in use.</span></span>
- <span data-ttu-id="a8246-174">**Opmerkingen**: diverse Prose die een aspect van de bewerking, functie of type beschrijven.</span><span class="sxs-lookup"><span data-stu-id="a8246-174">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="a8246-175">**Zie ook**: een lijst met volledig gekwalificeerde namen die betrekking hebben op gerelateerde functies, bewerkingen of door de gebruiker gedefinieerde typen.</span><span class="sxs-lookup"><span data-stu-id="a8246-175">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="a8246-176">**Verwijzingen**: een lijst met verwijzingen en citaten voor het gedocumenteerde item.</span><span class="sxs-lookup"><span data-stu-id="a8246-176">**References**: A list of references and citations for the documented item.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a8246-177">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="a8246-177">Next steps</span></span>

<span data-ttu-id="a8246-178">Meer informatie over [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions) in Q# .</span><span class="sxs-lookup"><span data-stu-id="a8246-178">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>