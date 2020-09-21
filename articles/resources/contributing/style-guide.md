---
title: Micro soft Q# stijl gids
description: Meer informatie over de naamgeving, invoer, documentatie en opmaak conventies voor Q# Program ma's en bibliotheken.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
no-loc:
- Q#
- $$v
ms.openlocfilehash: fef3cea1c11e4fef49ddbf63adb34e07675049d2
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834190"
---
# <a name="no-locq-style-guide"></a><span data-ttu-id="02565-103">Q# Stijl gids</span><span class="sxs-lookup"><span data-stu-id="02565-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="02565-104">Algemene conventies</span><span class="sxs-lookup"><span data-stu-id="02565-104">General Conventions</span></span> ##

<span data-ttu-id="02565-105">De conventies die in deze hand leiding worden beschreven, zijn bedoeld om Program ma's en bibliotheken te helpen maken die Q# gemakkelijker te lezen en te begrijpen zijn.</span><span class="sxs-lookup"><span data-stu-id="02565-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="02565-106">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-106">Guidance</span></span>

<span data-ttu-id="02565-107">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-107">We suggest:</span></span>

- <span data-ttu-id="02565-108">Negeer nooit een Conventie, tenzij u dit opzettelijk doet om meer Lees bare en begrijpelijke code voor uw gebruikers te bieden.</span><span class="sxs-lookup"><span data-stu-id="02565-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="02565-109">Naamgevings regels</span><span class="sxs-lookup"><span data-stu-id="02565-109">Naming Conventions</span></span> ##

<span data-ttu-id="02565-110">Om de Quantum Development Kit te bieden, streven we naar functie-en bewerkings namen die verquantumt ontwikkel aars om Program ma's te schrijven die gemakkelijk te lezen zijn en die verrassingen minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="02565-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="02565-111">Een belang rijk deel hiervan is dat wanneer we namen kiezen voor functies, bewerkingen en typen, de *woorden lijst* die programmeurs gebruiken om de Quantum concepten te Express, te bepalen. met onze keuzes kunnen we deze in hun inspanningen helpen om duidelijk te communiceren.</span><span class="sxs-lookup"><span data-stu-id="02565-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="02565-112">Dit is een verantwoordelijkheid voor ons om ervoor te zorgen dat de namen die we bieden, duidelijkheid geven in plaats van onduidelijkheid.</span><span class="sxs-lookup"><span data-stu-id="02565-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="02565-113">In deze sectie wordt beschreven hoe we voldoen aan deze verplichting in termen van expliciete richt lijnen die ons helpen bij het beste door de Q# ontwikkelings community.</span><span class="sxs-lookup"><span data-stu-id="02565-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="02565-114">Bewerkingen en functies</span><span class="sxs-lookup"><span data-stu-id="02565-114">Operations and Functions</span></span> ###

<span data-ttu-id="02565-115">Een van de eerste dingen die een naam moet bepalen, is of een bepaald symbool een functie of een bewerking vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="02565-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="02565-116">Het verschil tussen functies en bewerkingen is van cruciaal belang om te weten hoe een code blok zich gedraagt.</span><span class="sxs-lookup"><span data-stu-id="02565-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="02565-117">Om het onderscheid tussen functies en bewerkingen voor gebruikers te communiceren, vertrouwen we op die Q# modellen de Quantum bewerkingen via het gebruik van neven effecten.</span><span class="sxs-lookup"><span data-stu-id="02565-117">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="02565-118">Dat wil zeggen dat een bewerking iets *doet* .</span><span class="sxs-lookup"><span data-stu-id="02565-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="02565-119">Daarentegen beschrijven functies de wiskundige relaties tussen gegevens.</span><span class="sxs-lookup"><span data-stu-id="02565-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="02565-120">De expressie `Sin(PI() / 2.0)` *is* `1.0` en impliceert niets over de status van een programma of de qubits.</span><span class="sxs-lookup"><span data-stu-id="02565-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="02565-121">Samen vatting, bewerkingen doen zich voor in functies.</span><span class="sxs-lookup"><span data-stu-id="02565-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="02565-122">In dit onderscheid wordt gesuggereerd dat we bewerkingen als termen en functies als zelfstandig naam woord noemen.</span><span class="sxs-lookup"><span data-stu-id="02565-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="02565-123">Wanneer een door de gebruiker gedefinieerd type wordt gedeclareerd, wordt tegelijkertijd een nieuwe functie voor het maken van exemplaren van dat type gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="02565-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="02565-124">Vanuit dat perspectief moeten door de gebruiker gedefinieerde typen worden benoemd als zelfstandig naam woord, zodat zowel het type zelf als de functie-constructor consistente namen hebben.</span><span class="sxs-lookup"><span data-stu-id="02565-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="02565-125">Als dat het geval is, moet u ervoor zorgen dat de naam van de bewerking begint met de termen die duidelijk aangeven wat het effect van de bewerking is.</span><span class="sxs-lookup"><span data-stu-id="02565-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="02565-126">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="02565-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="02565-127">Een voor beeld van een specifieke bewerking in de duur van het verdient wanneer een bewerking een andere handeling als invoer gebruikt en aanroept.</span><span class="sxs-lookup"><span data-stu-id="02565-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="02565-128">In dergelijke gevallen is de actie die door de invoer bewerking wordt uitgevoerd niet duidelijk wanneer de buitenste bewerking is gedefinieerd, zodat de juiste term niet onmiddellijk wordt gewist.</span><span class="sxs-lookup"><span data-stu-id="02565-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="02565-129">We raden u aan de term in te voeren, `Apply` zoals in `ApplyIf` , `ApplyToEach` en `ApplyToFirst` .</span><span class="sxs-lookup"><span data-stu-id="02565-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="02565-130">Andere woorden kunnen ook nuttig zijn in dit geval, zoals in `IterateThroughCartesianPower` .</span><span class="sxs-lookup"><span data-stu-id="02565-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="02565-131">Verb</span><span class="sxs-lookup"><span data-stu-id="02565-131">Verb</span></span> | <span data-ttu-id="02565-132">Verwacht effect</span><span class="sxs-lookup"><span data-stu-id="02565-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="02565-133">Toepassen</span><span class="sxs-lookup"><span data-stu-id="02565-133">Apply</span></span> | <span data-ttu-id="02565-134">Een bewerking die is opgegeven als invoer, wordt aangeroepen</span><span class="sxs-lookup"><span data-stu-id="02565-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="02565-135">Assert</span><span class="sxs-lookup"><span data-stu-id="02565-135">Assert</span></span> | <span data-ttu-id="02565-136">Een hypo these over het resultaat van een mogelijke quantum meting wordt gecontroleerd door een simulator</span><span class="sxs-lookup"><span data-stu-id="02565-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="02565-137">Schatting</span><span class="sxs-lookup"><span data-stu-id="02565-137">Estimate</span></span> | <span data-ttu-id="02565-138">Er wordt een klassieke waarde geretourneerd die een schatting vertegenwoordigt die uit een of meer metingen is getrokken</span><span class="sxs-lookup"><span data-stu-id="02565-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="02565-139">Measure</span><span class="sxs-lookup"><span data-stu-id="02565-139">Measure</span></span> | <span data-ttu-id="02565-140">Er wordt een quantum meting uitgevoerd en het resultaat wordt geretourneerd aan de gebruiker</span><span class="sxs-lookup"><span data-stu-id="02565-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="02565-141">Voorbereiden</span><span class="sxs-lookup"><span data-stu-id="02565-141">Prepare</span></span> | <span data-ttu-id="02565-142">Een bepaald REGI ster van qubits wordt geïnitialiseerd in een bepaalde status</span><span class="sxs-lookup"><span data-stu-id="02565-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="02565-143">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="02565-143">Sample</span></span> | <span data-ttu-id="02565-144">Er wordt een klassieke waarde geretourneerd op wille keurige wijze van distributie</span><span class="sxs-lookup"><span data-stu-id="02565-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="02565-145">Voor-functies voor komt u dat het gebruik van woorden wordt voor komen voor veelvoorkomende naam woorden (Zie de richt lijnen voor de onderstaande juiste naam woorden) of bijvoeglijke naam woorden:</span><span class="sxs-lookup"><span data-stu-id="02565-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="02565-146">In nagenoeg alle gevallen raden we u aan om eerdere participles te gebruiken, waar dat nodig is om aan te geven dat een functie naam sterk is verbonden met een actie of een neven effect ergens anders in een Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="02565-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="02565-147">`ControlledOnInt`Maakt bijvoorbeeld gebruik van de formulier participle van de term ' besturings element ' om aan te geven dat de functie fungeert als een bijvoeger om het argument te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="02565-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="02565-148">Deze naam heeft een extra voor deel van het afstemmen van de semantiek van de ingebouwde `Controlled` functor, zoals hieronder wordt besproken.</span><span class="sxs-lookup"><span data-stu-id="02565-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="02565-149">Op dezelfde manier kunnen zelfstandige naam van _agents_ worden gebruikt om functie-en UDT-namen te maken op basis van bewerkings namen, zoals in het geval van de namen van `Encoder` een UDT die sterk is gekoppeld aan `Encode` .</span><span class="sxs-lookup"><span data-stu-id="02565-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-150">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-151">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-151">We suggest:</span></span>

- <span data-ttu-id="02565-152">Termen gebruiken voor bewerkings namen.</span><span class="sxs-lookup"><span data-stu-id="02565-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="02565-153">Gebruik naam woorden of bijvoegingen voor functie namen.</span><span class="sxs-lookup"><span data-stu-id="02565-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="02565-154">Gebruik zelfstandige naam woorden voor door de gebruiker gedefinieerde typen en kenmerken.</span><span class="sxs-lookup"><span data-stu-id="02565-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="02565-155">Gebruik voor alle aanroep bare namen een `CamelCase` sterke voor keur voor `pascalCase` , `snake_case` of `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="02565-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="02565-156">Zorg er met name voor dat oproep bare namen beginnen met hoofd letters.</span><span class="sxs-lookup"><span data-stu-id="02565-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="02565-157">Gebruik voor alle lokale variabelen een `pascalCase` sterke voor keur voor `CamelCase` , `snake_case` of `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="02565-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="02565-158">Zorg er met name voor dat lokale variabelen beginnen met kleine letters.</span><span class="sxs-lookup"><span data-stu-id="02565-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="02565-159">Vermijd het gebruik van onderstrepings tekens `_` in functie-en bewerkings namen; wanneer extra hiërarchie niveaus nodig zijn, gebruikt u naam ruimten en aliassen van naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="02565-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-160">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-160">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="02565-161">Naam</span><span class="sxs-lookup"><span data-stu-id="02565-161">Name</span></span> | <span data-ttu-id="02565-162">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="02565-163">☑</span><span class="sxs-lookup"><span data-stu-id="02565-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="02565-164">Het gebruik van een term (' reflectie ') wissen om het effect van de bewerking aan te geven.</span><span class="sxs-lookup"><span data-stu-id="02565-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="02565-165">☒</span><span class="sxs-lookup"><span data-stu-id="02565-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="02565-166">Het gebruik van de woord groep frase suggesties voor de functie, in plaats van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="02565-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="02565-167">☒</span><span class="sxs-lookup"><span data-stu-id="02565-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="02565-168">Gebruik van `snake_case` de Q# notatie contravenes.</span><span class="sxs-lookup"><span data-stu-id="02565-168">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="02565-169">☒</span><span class="sxs-lookup"><span data-stu-id="02565-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="02565-170">Gebruik van onderstrepings tekens intern naar bewerkings naam contravenes Q# notatie.</span><span class="sxs-lookup"><span data-stu-id="02565-170">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="02565-171">☑</span><span class="sxs-lookup"><span data-stu-id="02565-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="02565-172">Als u een woord groep gebruikt, wordt gesuggereerd dat de functie een bewerking retourneert.</span><span class="sxs-lookup"><span data-stu-id="02565-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="02565-173">☑</span><span class="sxs-lookup"><span data-stu-id="02565-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="02565-174">Het gebruik van zelfstandig naam woord ("feit") wissen om aan te geven dat dit een functie is, terwijl de bijvoeger.</span><span class="sxs-lookup"><span data-stu-id="02565-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="02565-175">☒</span><span class="sxs-lookup"><span data-stu-id="02565-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="02565-176">Bij gebruik van term (' Get ') wordt voorgesteld dat dit een bewerking is.</span><span class="sxs-lookup"><span data-stu-id="02565-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="02565-177">☑</span><span class="sxs-lookup"><span data-stu-id="02565-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="02565-178">Het gebruik van de woord groep van een zelfstandig nummer verwijst duidelijk naar het resultaat van het aanroepen van de UDT-constructor.</span><span class="sxs-lookup"><span data-stu-id="02565-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="02565-179">☒</span><span class="sxs-lookup"><span data-stu-id="02565-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="02565-180">Het gebruik van een verbale woord groep adviseert dat de UDT-constructor een bewerking is.</span><span class="sxs-lookup"><span data-stu-id="02565-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="02565-181">☑</span><span class="sxs-lookup"><span data-stu-id="02565-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="02565-182">Gebruik van de woord groep met zelfstandig naam communicatie communiceert het gebruik van het kenmerk.</span><span class="sxs-lookup"><span data-stu-id="02565-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="entry-points"></a><span data-ttu-id="02565-183">Invoerpunten</span><span class="sxs-lookup"><span data-stu-id="02565-183">Entry Points</span></span>

<span data-ttu-id="02565-184">Wanneer u een ingangs punt in een Q# programma definieert, Q# herkent de compiler het [ `@EntryPoint()` kenmerk](xref:microsoft.quantum.core.entrypoint) , in plaats van dat toegangs punten een bepaalde naam hebben (bijvoorbeeld: `main` , `Main` , of `__main__` ).</span><span class="sxs-lookup"><span data-stu-id="02565-184">When defining an entry point into a Q# program, the Q# compiler recognizes the [`@EntryPoint()` attribute](xref:microsoft.quantum.core.entrypoint) rather requiring that entry points have a particular name (e.g.: `main`, `Main`, or `__main__`).</span></span>
<span data-ttu-id="02565-185">Vanuit het perspectief van een Q# ontwikkelaar zijn ingangs punten normale bewerkingen die aantekeningen maken bij `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="02565-185">That is, from the perspective of a Q# developer, entry points are ordinary operations annotated with `@EntryPoint()`.</span></span>
<span data-ttu-id="02565-186">Daarnaast Q# kunnen ingangs punten toegangs punten zijn voor een hele toepassing (bijvoorbeeld in Q# zelfstandige uitvoer bare Program ma's), of kan een interface tussen een Q# programma en het hostprogramma voor een toepassing zijn (dat wil zeggen: bij gebruik Q# van python of .net), zodat de naam ' Main ' mogelijk misleidend is wanneer deze wordt toegepast op een Q# toegangs punt.</span><span class="sxs-lookup"><span data-stu-id="02565-186">Moreover, Q# entry points may be entry points for an entire application (for example, in Q# standalone executable programs), or may be an interface between a Q# program and the host program for an application (i.e.: when using Q# with Python or .NET), such that the name "main" could be misleading when applied to a Q# entry point.</span></span>

<span data-ttu-id="02565-187">We raden aan gebruik te maken van naamgevings punten om het gebruik van het kenmerk weer te geven met `@EntryPoint()` behulp van het algemene advies voor naamgevings bewerkingen die hierboven worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="02565-187">We suggest using naming entry points to reflect the use of the `@EntryPoint()` attribute by using the general advice for naming operations listed above.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="02565-188">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-188">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-189">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-189">We suggest:</span></span>

- <span data-ttu-id="02565-190">Geef geen toegangs punt bewerkingen als Main.</span><span class="sxs-lookup"><span data-stu-id="02565-190">Do not name entry point operations as "main."</span></span>
- <span data-ttu-id="02565-191">Geef toegangs punt bewerkingen op als normale bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="02565-191">Name entry point operations as ordinary operations.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-192">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-192">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="02565-193">Naam</span><span class="sxs-lookup"><span data-stu-id="02565-193">Name</span></span> | <span data-ttu-id="02565-194">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-194">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="02565-195">☑</span><span class="sxs-lookup"><span data-stu-id="02565-195">☑</span></span> | `@EntryPoint() operation RunSimulation` | <span data-ttu-id="02565-196">Het doel van het ingangs punt wordt duidelijk gecommuniceerd via de bewerkings naam.</span><span class="sxs-lookup"><span data-stu-id="02565-196">Clearly communicates purpose of entry point through operation name.</span></span> |
| <span data-ttu-id="02565-197">☒</span><span class="sxs-lookup"><span data-stu-id="02565-197">☒</span></span> | <s>`@EntryPoint() operation Main`</s> | <span data-ttu-id="02565-198">Het gebruik van `Main` heeft geen duidelijk communicatie doel van het begin punt en is redundant met het `@EntryPoint()` kenmerk.</span><span class="sxs-lookup"><span data-stu-id="02565-198">Use of `Main` doesn't clearly communicate purpose of entry point, and is redundant with `@EntryPoint()` attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="02565-199">Steno en afkortingen</span><span class="sxs-lookup"><span data-stu-id="02565-199">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="02565-200">Het bovenstaande advies ondanks dat er sprake is van een groot aantal vormen van steno met een gemeen schappelijke en pervasive gebruik in de Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="02565-200">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="02565-201">We raden u aan bestaande en algemene steno te gebruiken waar deze zich bevinden, met name voor bewerkingen die intrinsiek zijn voor de werking van een doel machine.</span><span class="sxs-lookup"><span data-stu-id="02565-201">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="02565-202">We kiezen bijvoorbeeld de naam `X` in plaats van `ApplyX` en `Rz` in plaats van `RotateAboutZ` .</span><span class="sxs-lookup"><span data-stu-id="02565-202">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="02565-203">Bij het gebruik van deze steno moeten de namen van de bewerkingen allemaal hoofd letters zijn (bijvoorbeeld: `MAJ` ).</span><span class="sxs-lookup"><span data-stu-id="02565-203">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="02565-204">Bij het Toep assen van deze Conventie is een zorgvuldige toepassing vereist voor een vaak gebruikte acroniemen en initialisms zoals ' QFT ' voor ' Quantum Fourier Transform '.</span><span class="sxs-lookup"><span data-stu-id="02565-204">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="02565-205">We suggereren de volgende algemene .NET-conventies voor het gebruik van acroniemen en initialisms in volledige namen, waarbij u moet bepalen dat:</span><span class="sxs-lookup"><span data-stu-id="02565-205">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="02565-206">afkortingen van twee letters en initialisms worden in hoofd letters genoemd (bijvoorbeeld: `BE` voor "big-endian"),</span><span class="sxs-lookup"><span data-stu-id="02565-206">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="02565-207">alle langere acroniemen en initialisms worden genoemd in `CamelCase` (bijvoorbeeld: `Qft` voor "Quantum Fourier Transform")</span><span class="sxs-lookup"><span data-stu-id="02565-207">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="02565-208">Een bewerking die de QFT implementeert, kan dus worden aangeroepen `QFT` als steno of als uitgeschreven als `ApplyQft` .</span><span class="sxs-lookup"><span data-stu-id="02565-208">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="02565-209">Voor bijzonder gebruikte bewerkingen en functies kan het wenselijk zijn om een steno naam op te geven als _alias_ voor een langer formulier:</span><span class="sxs-lookup"><span data-stu-id="02565-209">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[<span data-ttu-id="02565-210">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-210">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-211">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-211">We suggest:</span></span>

- <span data-ttu-id="02565-212">Overweeg vaak geaccepteerde en veelgebruikte steno namen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="02565-212">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="02565-213">Gebruik hoofd letters voor Steno.</span><span class="sxs-lookup"><span data-stu-id="02565-213">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="02565-214">Gebruik hoofd letters voor korte (twee letters) acroniemen en initialisms.</span><span class="sxs-lookup"><span data-stu-id="02565-214">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="02565-215">Gebruik `CamelCase` voor meer (drie of meer letter) acroniemen en initialisms.</span><span class="sxs-lookup"><span data-stu-id="02565-215">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-216">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-216">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="02565-217">Naam</span><span class="sxs-lookup"><span data-stu-id="02565-217">Name</span></span> | <span data-ttu-id="02565-218">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-218">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="02565-219">☑</span><span class="sxs-lookup"><span data-stu-id="02565-219">☑</span></span> | `X` | <span data-ttu-id="02565-220">Goed te begrijpen steno voor ' een $X $ Transformation ' toep assen '</span><span class="sxs-lookup"><span data-stu-id="02565-220">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="02565-221">☑</span><span class="sxs-lookup"><span data-stu-id="02565-221">☑</span></span> | `CNOT` | <span data-ttu-id="02565-222">Goed te begrijpen steno voor "Controlled-NOT"</span><span class="sxs-lookup"><span data-stu-id="02565-222">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="02565-223">☒</span><span class="sxs-lookup"><span data-stu-id="02565-223">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="02565-224">Steno mag niet in zijn `CamelCase` .</span><span class="sxs-lookup"><span data-stu-id="02565-224">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="02565-225">☑</span><span class="sxs-lookup"><span data-stu-id="02565-225">☑</span></span> | `ApplyQft` | <span data-ttu-id="02565-226">Common Initiation "QFT" wordt weer gegeven als onderdeel van een lange formulier naam.</span><span class="sxs-lookup"><span data-stu-id="02565-226">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="02565-227">☑</span><span class="sxs-lookup"><span data-stu-id="02565-227">☑</span></span> | `QFT` | <span data-ttu-id="02565-228">Common Initiation "QFT" wordt weer gegeven als onderdeel van een steno naam.</span><span class="sxs-lookup"><span data-stu-id="02565-228">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="02565-229">Juiste naam woorden in namen</span><span class="sxs-lookup"><span data-stu-id="02565-229">Proper Nouns in Names</span></span> ###

<span data-ttu-id="02565-230">In het geval van een fysieke waarde is het gebruikelijk om dingen te benoemen na de eerste persoon die over hen publiceert. de meeste niet-physicists zijn niet bekend met de namen van iedereen en alle geschiedenis.</span><span class="sxs-lookup"><span data-stu-id="02565-230">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="02565-231">Het is te sterk om te voldoen aan de naamgevings conventies van de fysica, waardoor er een aanzienlijke barrière kan worden ingevoerd, omdat gebruikers van andere achtergronden een groot aantal schijnbaar ondoorzichtige namen moeten leren om veelvoorkomende bewerkingen en concepten te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="02565-231">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="02565-232">Daarom is het raadzaam om, waar mogelijk, veelvoorkomende algemene naam woorden die een concept beschrijven, in hoge voor keur te worden aangenomen voor de juiste naam woorden die de publicatie geschiedenis van een concept beschrijven.</span><span class="sxs-lookup"><span data-stu-id="02565-232">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="02565-233">Een voor beeld hiervan is dat de afzonderlijk beheerde SWAP-en dubbele controle niet worden uitgevoerd, ook wel de "Fredkin"-en "Toffoli"-bewerkingen worden genoemd in academische literatuur, maar worden in de Q# eerste plaats aangeduid als `CSWAP` en `CCNOT` .</span><span class="sxs-lookup"><span data-stu-id="02565-233">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="02565-234">In beide gevallen bieden de API-documentatie opmerkingen synoniemen op basis van de juiste naam woorden, samen met alle relevante bron vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="02565-234">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="02565-235">Deze voor keur is met name belang rijk, omdat het gebruik van de juiste zelfstandige naam woorden altijd nood zakelijk is. Q# Dit is de traditie die is ingesteld door veel klassieke talen, bijvoorbeeld, en verwijst naar `Bool` typen in verwijzingen naar Booleaanse logica, die op zijn beurt wordt genoemd in respect van George Boole.</span><span class="sxs-lookup"><span data-stu-id="02565-235">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="02565-236">Enkele Quantum concepten worden op een vergelijk bare manier genoemd, met inbegrip van het `Pauli` type ingebouwd in de Q# taal.</span><span class="sxs-lookup"><span data-stu-id="02565-236">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="02565-237">Door het gebruik van de juiste zelfstandige naam woorden, waarbij dit gebruik niet essentieel is, te minimaliseren, kunnen we de impact verminderen waarbij de juiste zelfstandige naam woorden niet redelijkerwijs worden vermeden.</span><span class="sxs-lookup"><span data-stu-id="02565-237">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-238">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-238">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="02565-239">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-239">We suggest:</span></span>

- <span data-ttu-id="02565-240">Vermijd het gebruik van de juiste zelfstandige naam woorden in namen.</span><span class="sxs-lookup"><span data-stu-id="02565-240">Avoid the use of proper nouns in names.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-241">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-241">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="02565-242">Type conversies</span><span class="sxs-lookup"><span data-stu-id="02565-242">Type Conversions</span></span> ###

<span data-ttu-id="02565-243">Omdat een Q# sterk en statisch getypte taal is, kan een waarde van één type alleen worden gebruikt als een waarde van een ander type met behulp van een expliciete aanroep van een type conversie functie.</span><span class="sxs-lookup"><span data-stu-id="02565-243">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="02565-244">Dit is in tegens telling tot talen waarmee waarden typen impliciet kunnen worden gewijzigd (bijvoorbeeld: type promotie) of via casting.</span><span class="sxs-lookup"><span data-stu-id="02565-244">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="02565-245">Als gevolg hiervan spelen functies van het type conversie een belang rijke rol bij het Q# ontwikkelen van tape wisselaars en vormen ze een van de vaak voorkomende beslissingen over naamgeving.</span><span class="sxs-lookup"><span data-stu-id="02565-245">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="02565-246">Maar omdat type conversies altijd _deterministisch_zijn, kunnen ze worden geschreven als functies en dus onder de bovenstaande aanbeveling vallen.</span><span class="sxs-lookup"><span data-stu-id="02565-246">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="02565-247">In het bijzonder raden we aan dat type conversie functies nooit moeten worden benoemd als woorden (bijvoorbeeld:) of voor voor keuren voor bewerkings `ConvertToX` parameters ( `ToX` ), maar moeten worden benoemd als voor zetsels van bijvoeglijke woord groepen die de bron-en doel typen ( `XAsY` ) aangeven.</span><span class="sxs-lookup"><span data-stu-id="02565-247">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="02565-248">Bij het weer geven van matrix typen in functie namen van type conversie, wordt de steno aangeraden `Arr` .</span><span class="sxs-lookup"><span data-stu-id="02565-248">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="02565-249">Als buitengewone omstandigheden worden geblokkeerd, raden we aan dat alle type conversie functies worden benoemd met `As` zodat ze snel kunnen worden geïdentificeerd.</span><span class="sxs-lookup"><span data-stu-id="02565-249">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-250">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-250">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-251">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-251">We suggest:</span></span>

- <span data-ttu-id="02565-252">Als een functie een waarde van het type converteert `X` naar een waarde van `Y` het type, gebruikt u de naam `AsY` of `XAsY` .</span><span class="sxs-lookup"><span data-stu-id="02565-252">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-253">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-253">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="02565-254">Naam</span><span class="sxs-lookup"><span data-stu-id="02565-254">Name</span></span> | <span data-ttu-id="02565-255">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-255">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="02565-256">☒</span><span class="sxs-lookup"><span data-stu-id="02565-256">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="02565-257">De voor positie ' to ' resulteert in een verbale woord groep, wat een bewerking aangeeft en niet een functie.</span><span class="sxs-lookup"><span data-stu-id="02565-257">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="02565-258">☒</span><span class="sxs-lookup"><span data-stu-id="02565-258">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="02565-259">Het invoer type is niet duidelijk uit de functie naam.</span><span class="sxs-lookup"><span data-stu-id="02565-259">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="02565-260">☒</span><span class="sxs-lookup"><span data-stu-id="02565-260">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="02565-261">De invoer-en uitvoer typen worden in de verkeerde volg orde weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="02565-261">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="02565-262">☑</span><span class="sxs-lookup"><span data-stu-id="02565-262">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="02565-263">Zowel de invoer typen als de uitvoer typen zijn duidelijk.</span><span class="sxs-lookup"><span data-stu-id="02565-263">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="02565-264">Privé-of interne namen</span><span class="sxs-lookup"><span data-stu-id="02565-264">Private or Internal Names</span></span> ###

<span data-ttu-id="02565-265">In veel gevallen is een naam uitsluitend bedoeld voor intern gebruik in een bibliotheek of project en is dit geen gegarandeerd deel van de API die wordt aangeboden door een bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="02565-265">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="02565-266">Het is handig om duidelijk aan te geven dat dit het geval is bij het benoemen van functies en bewerkingen, zodat onbedoelde afhankelijkheden op interne code duidelijk worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02565-266">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="02565-267">Als een bewerking of functie niet bedoeld is voor direct gebruik, maar moet worden gebruikt door een overeenkomende aanroepable die door een gedeeltelijke toepassing wordt uitgevoerd, kunt u overwegen een naam te gebruiken die begint met het `internal` sleutel woord voor de aanroepable die gedeeltelijk is toegepast.</span><span class="sxs-lookup"><span data-stu-id="02565-267">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with the `internal` keyword for the callable that is partially applied.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-268">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-268">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-269">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-269">We suggest:</span></span>

- <span data-ttu-id="02565-270">Wanneer een functie, bewerking of door de gebruiker gedefinieerd type geen deel uitmaakt van de open bare API voor een Q# bibliotheek of programma, moet u ervoor zorgen dat deze is gemarkeerd als intern door het `internal` tref woord vóór de `function` , `operation` of declaratie te plaatsen `newtype` .</span><span class="sxs-lookup"><span data-stu-id="02565-270">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that it is marked as internal by placing the `internal` keyword before the `function`, `operation`, or `newtype` declaration.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-271">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-271">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="02565-272">Naam</span><span class="sxs-lookup"><span data-stu-id="02565-272">Name</span></span> | <span data-ttu-id="02565-273">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-273">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="02565-274">☒</span><span class="sxs-lookup"><span data-stu-id="02565-274">☒</span></span> | <s>`operation _ApplyDecomposedOperation`</s> | <span data-ttu-id="02565-275">Gebruik geen onderstrepings teken `_` om aan te geven dat deze bewerking alleen voor intern gebruik is.</span><span class="sxs-lookup"><span data-stu-id="02565-275">Do not use an underscore `_` to indicate that this operation is for internal use only.</span></span> |
| <span data-ttu-id="02565-276">☑</span><span class="sxs-lookup"><span data-stu-id="02565-276">☑</span></span> | `internal operation ApplyDecomposedOperation` | <span data-ttu-id="02565-277">Het `internal` sleutel woord aan het begin geeft duidelijk aan dat deze bewerking alleen voor intern gebruik is.</span><span class="sxs-lookup"><span data-stu-id="02565-277">The `internal` keyword at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***
### <a name="variants"></a><span data-ttu-id="02565-278">Qua</span><span class="sxs-lookup"><span data-stu-id="02565-278">Variants</span></span> ###

<span data-ttu-id="02565-279">Hoewel deze beperking mogelijk niet in toekomstige versies van van Q# toepassing is, is het al het geval dat er vaak groepen van gerelateerde bewerkingen of functies zijn die worden onderscheiden door welke functors hun invoer ondersteunen, of door het concrete type van de argumenten.</span><span class="sxs-lookup"><span data-stu-id="02565-279">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="02565-280">Deze groepen kunnen worden onderscheiden met dezelfde hoofd naam, gevolgd door een of twee letters die de variant aangeven.</span><span class="sxs-lookup"><span data-stu-id="02565-280">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="02565-281">Achtervoegsel</span><span class="sxs-lookup"><span data-stu-id="02565-281">Suffix</span></span> | <span data-ttu-id="02565-282">Betekenis</span><span class="sxs-lookup"><span data-stu-id="02565-282">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="02565-283">Verwachte invoer wordt ondersteund `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="02565-283">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="02565-284">Verwachte invoer wordt ondersteund `Controlled`</span><span class="sxs-lookup"><span data-stu-id="02565-284">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="02565-285">Verwachte invoer voor ondersteuning `Controlled` en `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="02565-285">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="02565-286">Invoer-of invoer waarden zijn van het type `Int`</span><span class="sxs-lookup"><span data-stu-id="02565-286">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="02565-287">Invoer-of invoer waarden zijn van het type `Double`</span><span class="sxs-lookup"><span data-stu-id="02565-287">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="02565-288">Invoer-of invoer waarden zijn van het type `BigInt`</span><span class="sxs-lookup"><span data-stu-id="02565-288">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidance"></a>[<span data-ttu-id="02565-289">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-289">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-290">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-290">We suggest:</span></span>

- <span data-ttu-id="02565-291">Als een functie of bewerking niet is gerelateerd aan vergelijk bare functies of bewerkingen door de typen en functor-ondersteuning van de invoer, mag u geen achtervoegsel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="02565-291">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="02565-292">Als een functie of bewerking is gerelateerd aan vergelijk bare functies of bewerkingen door de typen en functor-ondersteuning van de invoer, gebruikt u achtervoegsels zoals in de bovenstaande tabel om varianten te onderscheiden.</span><span class="sxs-lookup"><span data-stu-id="02565-292">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-293">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-293">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="02565-294">Argumenten en variabelen</span><span class="sxs-lookup"><span data-stu-id="02565-294">Arguments and Variables</span></span> ###

<span data-ttu-id="02565-295">Een belang rijk doel van de Q# code voor een functie of bewerking is dat deze eenvoudig kan worden gelezen en begrepen.</span><span class="sxs-lookup"><span data-stu-id="02565-295">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="02565-296">Op dezelfde manier moeten de namen van invoer-en type argumenten communiceren hoe een functie of argument wordt gebruikt wanneer dit wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="02565-296">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="02565-297">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-297">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-298">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-298">We suggest:</span></span>

- <span data-ttu-id="02565-299">Gebruik voor alle variabele-en invoer namen een `pascalCase` sterke voor keur voor `CamelCase` , `snake_case` of `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="02565-299">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="02565-300">De invoer namen moeten een beschrijvende naam hebben. Vermijd waar mogelijk een of twee letter namen.</span><span class="sxs-lookup"><span data-stu-id="02565-300">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="02565-301">Bewerkingen en functies die precies één type argument accepteren, moeten dit type argument aangeven door `T` als de bijbehorende rol duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="02565-301">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="02565-302">Als een functie of bewerking meerdere type argumenten nodig heeft, of als de rol van een enkel type argument niet duidelijk is, overweeg dan het gebruik van een kort gepaard woord met als `T` voor beeld (bijvoorbeeld: `TOutput` ) voor elk type.</span><span class="sxs-lookup"><span data-stu-id="02565-302">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="02565-303">Typ geen type namen in argument-en variabelenamen; deze informatie kan worden verstrekt door uw ontwikkel omgeving.</span><span class="sxs-lookup"><span data-stu-id="02565-303">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="02565-304">Denoteer scalaire typen met hun letterlijke namen ( `flagQubit` ) en matrix typen met een meervoud ( `measResults` ).</span><span class="sxs-lookup"><span data-stu-id="02565-304">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="02565-305">Voor matrices van qubits met name, overweeg om dergelijke typen te identificeren, `Register` waarbij de naam verwijst naar een reeks qubits die op een of andere manier nauw verwant zijn.</span><span class="sxs-lookup"><span data-stu-id="02565-305">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="02565-306">Variabelen die als indexen worden gebruikt in matrices moeten beginnen met `idx` en moeten een enkelvoud zijn (bijvoorbeeld: `things[idxThing]` ).</span><span class="sxs-lookup"><span data-stu-id="02565-306">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="02565-307">In het bijzonder Vermijd het gebruik van variabelen namen met één letter als indices. Overweeg `idx` ten minste te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="02565-307">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="02565-308">Variabelen die worden gebruikt om de lengte van matrices te bewaren, moeten beginnen met `n` en moeten worden gemeervoudt (bijvoorbeeld: `nThings` ).</span><span class="sxs-lookup"><span data-stu-id="02565-308">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-309">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-309">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="02565-310">Door de gebruiker gedefinieerd type met de naam items</span><span class="sxs-lookup"><span data-stu-id="02565-310">User-Defined Type Named Items</span></span> ###

<span data-ttu-id="02565-311">Benoemde items in door de gebruiker gedefinieerde typen moeten worden aangeduid als `CamelCase` , zelfs bij invoer naar UDT-constructors.</span><span class="sxs-lookup"><span data-stu-id="02565-311">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="02565-312">Dit helpt om de benoemde items duidelijk te scheiden van verwijzingen naar variabelen met een lokaal bereik wanneer u een accessor-notatie (bijvoorbeeld: `callable::Apply` ) of Copy-and-update notatie ( `set arr w/= Data <- newData` ) gebruikt.</span><span class="sxs-lookup"><span data-stu-id="02565-312">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-313">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-313">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-314">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-314">We suggest:</span></span>

- <span data-ttu-id="02565-315">Benoemde items in UDT-constructors moeten worden benoemd als `CamelCase` ; dat wil zeggen dat ze beginnen met een eerste hoofd letter.</span><span class="sxs-lookup"><span data-stu-id="02565-315">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="02565-316">Benoemde items die aan bewerkingen worden omgezet, moeten de naam werk woord fasen hebben.</span><span class="sxs-lookup"><span data-stu-id="02565-316">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="02565-317">Benoemde items die niet naar bewerkingen worden omgezet, moeten een naam hebben als woord groepen.</span><span class="sxs-lookup"><span data-stu-id="02565-317">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="02565-318">Voor UDTs die verloopt, moet een enkel benoemd item `Apply` worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="02565-318">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-319">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-319">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="02565-320">Codefragment</span><span class="sxs-lookup"><span data-stu-id="02565-320">Snippet</span></span> | <span data-ttu-id="02565-321">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-321">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="02565-322">☑</span><span class="sxs-lookup"><span data-stu-id="02565-322">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="02565-323">De naam `Apply` is een `CamelCase` verbale woord groep waarmee wordt voorgesteld dat het benoemd item een bewerking is.</span><span class="sxs-lookup"><span data-stu-id="02565-323">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="02565-324">☒</span><span class="sxs-lookup"><span data-stu-id="02565-324">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="02565-325">Benoemde items moeten beginnen met een eerste hoofd letter.</span><span class="sxs-lookup"><span data-stu-id="02565-325">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="02565-326">☒</span><span class="sxs-lookup"><span data-stu-id="02565-326">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="02565-327">Benoemde items die worden omgezet in-functies, moeten worden benoemd als woord groepen, niet als verbale woord groepen.</span><span class="sxs-lookup"><span data-stu-id="02565-327">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="02565-328">Invoer conventies</span><span class="sxs-lookup"><span data-stu-id="02565-328">Input Conventions</span></span> ##

<span data-ttu-id="02565-329">Wanneer een ontwikkelaar een bewerking of functie aanroept, moeten de verschillende invoer waarden voor die bewerking of functie worden opgegeven in een bepaalde volg orde, waardoor de cognitieve belasting die een ontwikkelaar gemerkt, wordt gebruikt om een bibliotheek te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="02565-329">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="02565-330">Met name de taak van het onthouden van invoer orders is vaak een afleiding van de taak bij de hand: het Program meren van een implementatie van een Quantum algoritme.</span><span class="sxs-lookup"><span data-stu-id="02565-330">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="02565-331">Hoewel uitgebreide ondersteuning voor IDE dit in grote mate kan beperken, kan een goed ontwerp en de gang bare conventies ook helpen om de cognitieve belasting van een API te minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="02565-331">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="02565-332">Waar mogelijk kan het nuttig zijn om het aantal ingevoerde invoer waarden te verminderen dat wordt verwacht door een bewerking of functie, zodat de rol van elke invoer onmiddellijk duidelijker is voor ontwikkel aars die de bewerking of functie aanroepen, en naar ontwikkel aars die code later lezen.</span><span class="sxs-lookup"><span data-stu-id="02565-332">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="02565-333">Met name wanneer het niet mogelijk is om het aantal argumenten voor een bewerking of functie te verminderen, is het belang rijk om een consistente volg orde te hebben die het voors pellen van de gebruiker bij de voor spelling van de invoer verkleint.</span><span class="sxs-lookup"><span data-stu-id="02565-333">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="02565-334">We raden u aan om de conventies voor invoer volgorde in te stellen die grotendeels afleiden van een deel van de toepassing als generalisatie van currying f (x, y) ≡ f (x) (y).</span><span class="sxs-lookup"><span data-stu-id="02565-334">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="02565-335">Het Toep assen van de eerste argumenten zou dus gedeeltelijk van toepassing moeten zijn en die nuttig is voor eigen rechts, wanneer dat redelijk is.</span><span class="sxs-lookup"><span data-stu-id="02565-335">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="02565-336">U kunt de volgende volg orde van argumenten gebruiken om dit principe te volgen:</span><span class="sxs-lookup"><span data-stu-id="02565-336">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="02565-337">Klassieke niet-aanroep bare argumenten, zoals hoeken, vectoren van bevoegdheden, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="02565-337">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="02565-338">Aanroep bare argumenten (functies en argumenten).</span><span class="sxs-lookup"><span data-stu-id="02565-338">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="02565-339">Als beide functies en bewerkingen worden uitgevoerd als argumenten, kunt u de bewerkingen na functies plaatsen.</span><span class="sxs-lookup"><span data-stu-id="02565-339">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="02565-340">Verzamelingen die worden uitgevoerd door aanroep bare argumenten op soort gelijke wijze als,, en `Map` `Iter` `Enumerate` `Fold` .</span><span class="sxs-lookup"><span data-stu-id="02565-340">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="02565-341">Qubit argumenten gebruikt als besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="02565-341">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="02565-342">Qubit argumenten die als doelen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="02565-342">Qubit arguments used as targets.</span></span>

<span data-ttu-id="02565-343">Houd rekening met een bewerking `ApplyPhaseEstimationIteration` voor het gebruik in de fase-schatting die een hoek en een Oracle afneemt, de hoek door gegeven aan `Rz` een matrix met verschillende schaal factoren en vervolgens de toepassingen van de Oracle beheert.</span><span class="sxs-lookup"><span data-stu-id="02565-343">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="02565-344">De invoer wordt op `ApplyPhaseEstimationIteration` de volgende manier gerangschikt:</span><span class="sxs-lookup"><span data-stu-id="02565-344">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
<span data-ttu-id="02565-345">Als een speciaal geval van het minimaliseren van de verrassingen, simuleren sommige functies en bewerkingen het gedrag van de ingebouwde functors `Adjoint` en `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="02565-345">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="02565-346">Bijvoorbeeld, `ControlledOnInt<'T>` is van `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` het type, bijvoorbeeld `ControlledOnInt<Qubit[]>(5, _)` de `Controlled` functor, maar op voor waarde dat het controle register de status $ \ket {5} = \ket {101} $ vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="02565-346">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="02565-347">Daarom verwacht een ontwikkelaar dat de invoer de `ControlledOnInt` aanroep zou plaatsen die het laatst is getransformeerd en dat de resulterende bewerking de invoer `(Qubit[], 'T)` ---dezelfde volg orde uitvoert, gevolgd door de uitvoer van de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="02565-347">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-348">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-348">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-349">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-349">We suggest:</span></span>

- <span data-ttu-id="02565-350">Gebruik invoer volgorden die consistent zijn met het gebruik van een gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="02565-350">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="02565-351">Gebruik invoer volgorden die consistent zijn met ingebouwde functors.</span><span class="sxs-lookup"><span data-stu-id="02565-351">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="02565-352">Plaats alle klassieke invoer vóór een Quantum invoer.</span><span class="sxs-lookup"><span data-stu-id="02565-352">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-353">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-353">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="02565-354">Documentatie conventies</span><span class="sxs-lookup"><span data-stu-id="02565-354">Documentation Conventions</span></span> ##

<span data-ttu-id="02565-355">De Q# taal biedt de mogelijkheid om documentatie te koppelen aan bewerkingen, functies en door de gebruiker gedefinieerde typen door het gebruik van documentatie opmerkingen over speciaal opgemaakte documenten.</span><span class="sxs-lookup"><span data-stu-id="02565-355">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="02565-356">Deze documentatie opmerkingen worden aangeduid met drievoudige slashes ( `///` ) en zijn kleine [DocFX-geprijsde](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documenten die kunnen worden gebruikt voor het beschrijven van het doel van elke bewerking, functie en door de gebruiker gedefinieerd type, welke invoer elk verwacht, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="02565-356">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="02565-357">De compiler die wordt geleverd met de Quantum Development Kit, haalt deze opmerkingen op en gebruikt deze om de typen documentatie op te geven die vergelijkbaar is met die in https://docs.microsoft.com/quantum .</span><span class="sxs-lookup"><span data-stu-id="02565-357">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="02565-358">Op dezelfde manier gebruikt de taal server van de Quantum Development Kit deze opmerkingen om gebruikers te helpen bij het aanwijzen van de muis aanwijzer over symbolen in hun Q# code.</span><span class="sxs-lookup"><span data-stu-id="02565-358">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="02565-359">Het gebruik van documentatie opmerkingen kan gebruikers helpen om code te maken met behulp van een nuttige referentie voor informatie die niet eenvoudig kan worden weer gegeven met de andere conventies in dit document.</span><span class="sxs-lookup"><span data-stu-id="02565-359">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="02565-360">[Naslag informatie over de syntaxis van documentatie](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span><span class="sxs-lookup"><span data-stu-id="02565-360">[Documentation comment syntax reference](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span></span>

<span data-ttu-id="02565-361">Als u deze functionaliteit effectief wilt gebruiken om gebruikers te helpen, raden we u aan om een aantal zaken te houden wanneer u documentatie opmerkingen schrijft.</span><span class="sxs-lookup"><span data-stu-id="02565-361">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-362">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-362">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="02565-363">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-363">We suggest:</span></span>

- <span data-ttu-id="02565-364">Elke open bare functie, bewerking en door de gebruiker gedefinieerd type moeten onmiddellijk worden voorafgegaan door een documentatie opmerking.</span><span class="sxs-lookup"><span data-stu-id="02565-364">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="02565-365">Elke documentatie opmerking moet mini maal de volgende secties bevatten:</span><span class="sxs-lookup"><span data-stu-id="02565-365">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="02565-366">Samenvatting</span><span class="sxs-lookup"><span data-stu-id="02565-366">Summary</span></span>
    - <span data-ttu-id="02565-367">Invoer</span><span class="sxs-lookup"><span data-stu-id="02565-367">Input</span></span>
    - <span data-ttu-id="02565-368">Uitvoer (indien van toepassing)</span><span class="sxs-lookup"><span data-stu-id="02565-368">Output (if applicable)</span></span>
- <span data-ttu-id="02565-369">Zorg ervoor dat alle samen vattingen twee zinnen of minder zijn.</span><span class="sxs-lookup"><span data-stu-id="02565-369">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="02565-370">Als er meer ruimte nodig is, geeft u een `# Description` sectie op die direct volgt `# Summary` met de volledige informatie.</span><span class="sxs-lookup"><span data-stu-id="02565-370">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="02565-371">Als dat niet het geval is, kunt u geen wiskundige formules in samen vattingen gebruiken, omdat niet alle clients TeX-notatie in samen vattingen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="02565-371">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="02565-372">Houd er rekening mee dat bij het schrijven van Prose-documenten (bijvoorbeeld TeX of prijs verlaging) het voor keur is dat er langere lijn lengten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="02565-372">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="02565-373">Geef alle relevante wiskundige expressies op in de `# Description` sectie.</span><span class="sxs-lookup"><span data-stu-id="02565-373">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="02565-374">Herhaal bij het beschrijven van invoer de typen van elke invoer niet, aangezien deze kunnen worden afgeleid door de compiler en het risico dat inconsistentie wordt geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="02565-374">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="02565-375">Geef voor beelden op die van toepassing zijn, elk in hun eigen `# Example` sectie.</span><span class="sxs-lookup"><span data-stu-id="02565-375">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="02565-376">Geef een korte beschrijving van elk voor beeld voordat u code vermeldt.</span><span class="sxs-lookup"><span data-stu-id="02565-376">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="02565-377">Vermeld alle relevante academische publicaties (bijvoorbeeld: papers, procedures, blog berichten en alternatieve implementaties) in een `# References` sectie als een lijst met opsommings tekens van koppelingen.</span><span class="sxs-lookup"><span data-stu-id="02565-377">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="02565-378">Zorg ervoor dat alle bron vermelding-koppelingen, waar mogelijk, permanent en onveranderbare id's (DOIs of genummerde arXiv) zijn.</span><span class="sxs-lookup"><span data-stu-id="02565-378">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="02565-379">Wanneer een bewerking of functie is gerelateerd aan andere bewerkingen of functies van functor varianten, vermeldt u andere varianten als opsommings tekens in de `# See Also` sectie.</span><span class="sxs-lookup"><span data-stu-id="02565-379">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="02565-380">Laat een lege opmerkings regel tussen de secties Level-1 ( `/// #` ), maar laat geen lege regel tussen de secties Level-2 ( `/// ##` ) staan.</span><span class="sxs-lookup"><span data-stu-id="02565-380">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-381">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-381">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="02565-382">☑</span><span class="sxs-lookup"><span data-stu-id="02565-382">☑</span></span> ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

***

## <a name="formatting-conventions"></a><span data-ttu-id="02565-383">Opmaak conventies</span><span class="sxs-lookup"><span data-stu-id="02565-383">Formatting Conventions</span></span> ##

<span data-ttu-id="02565-384">Naast de voor gaande suggesties is het handig om code zo leesbaar mogelijk te maken voor het gebruik van consistente opmaak regels.</span><span class="sxs-lookup"><span data-stu-id="02565-384">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="02565-385">Dergelijke opmaak regels worden op een wille keurige manier en in het algemeen op persoonlijke wijze in het gepaareerd.</span><span class="sxs-lookup"><span data-stu-id="02565-385">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="02565-386">Het is echter raadzaam een consistente set opmaak conventies binnen een groep mede werkers te onderhouden, met name voor grote Q# projecten, zoals de Quantum Development Kit zelf.</span><span class="sxs-lookup"><span data-stu-id="02565-386">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="02565-387">Deze regels kunnen automatisch worden toegepast met behulp van het opmaak programma dat is geïntegreerd met de Q# compiler.</span><span class="sxs-lookup"><span data-stu-id="02565-387">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="02565-388">Hulp</span><span class="sxs-lookup"><span data-stu-id="02565-388">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="02565-389">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="02565-389">We suggest:</span></span>

- <span data-ttu-id="02565-390">Gebruik vier spaties in plaats van tabs voor portabiliteit.</span><span class="sxs-lookup"><span data-stu-id="02565-390">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="02565-391">Bijvoorbeeld in VS code:</span><span class="sxs-lookup"><span data-stu-id="02565-391">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="02565-392">Regel terugloop om 79 tekens waar redelijk.</span><span class="sxs-lookup"><span data-stu-id="02565-392">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="02565-393">Gebruik spaties om binaire Opera tors.</span><span class="sxs-lookup"><span data-stu-id="02565-393">Use spaces around binary operators.</span></span>
- <span data-ttu-id="02565-394">Gebruik spaties aan beide zijden van de dubbele punten die worden gebruikt voor type annotaties.</span><span class="sxs-lookup"><span data-stu-id="02565-394">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="02565-395">Gebruik één spatie na komma's die worden gebruikt in matrix-en tuple-letterlijke waarden (bijvoorbeeld: in ingangen naar functies en bewerkingen).</span><span class="sxs-lookup"><span data-stu-id="02565-395">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="02565-396">Gebruik geen spaties na functie, bewerking of UDT-namen, of na de `@` in-kenmerk declaraties.</span><span class="sxs-lookup"><span data-stu-id="02565-396">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="02565-397">Elke kenmerk declaratie moet op een eigen regel staan.</span><span class="sxs-lookup"><span data-stu-id="02565-397">Each attribute declaration should be on its own line.</span></span>

# <a name="examples"></a>[<span data-ttu-id="02565-398">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="02565-398">Examples</span></span>](#tab/examples)

| &nbsp; | <span data-ttu-id="02565-399">Codefragment</span><span class="sxs-lookup"><span data-stu-id="02565-399">Snippet</span></span> | <span data-ttu-id="02565-400">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02565-400">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="02565-401">☒</span><span class="sxs-lookup"><span data-stu-id="02565-401">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="02565-402">Gebruik spaties om binaire Opera tors.</span><span class="sxs-lookup"><span data-stu-id="02565-402">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="02565-403">☒</span><span class="sxs-lookup"><span data-stu-id="02565-403">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="02565-404">Gebruik spaties rondom type aantekening.</span><span class="sxs-lookup"><span data-stu-id="02565-404">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="02565-405">☑</span><span class="sxs-lookup"><span data-stu-id="02565-405">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="02565-406">De items in de invoer-tuple zijn op de juiste wijze voor de Lees baarheid.</span><span class="sxs-lookup"><span data-stu-id="02565-406">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="02565-407">☒</span><span class="sxs-lookup"><span data-stu-id="02565-407">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="02565-408">Spaties moeten worden onderdrukt na functie-, bewerking-of UDT-namen.</span><span class="sxs-lookup"><span data-stu-id="02565-408">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***
