---
title: 'Q # stijl gids | Microsoft Docs'
description: 'Q #-stijl gids'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
ms.openlocfilehash: 56455e9d5cd452b8620ee794f40563d1d3040193
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183842"
---
# <a name="q-style-guide"></a><span data-ttu-id="71e12-103">Q #-stijl gids</span><span class="sxs-lookup"><span data-stu-id="71e12-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="71e12-104">Algemene conventies</span><span class="sxs-lookup"><span data-stu-id="71e12-104">General Conventions</span></span> ##

<span data-ttu-id="71e12-105">De conventies die in deze hand leiding worden voorgesteld, zijn bedoeld om Program ma's en bibliotheken die zijn geschreven in Q # gemakkelijker te kunnen lezen en begrijpen.</span><span class="sxs-lookup"><span data-stu-id="71e12-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-106">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-106">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-107">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-107">We suggest:</span></span>

- <span data-ttu-id="71e12-108">Negeer nooit een Conventie, tenzij u dit opzettelijk doet om meer Lees bare en begrijpelijke code voor uw gebruikers te bieden.</span><span class="sxs-lookup"><span data-stu-id="71e12-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-109">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-109">Examples</span></span>](#tab/examples)

***

## <a name="naming-conventions"></a><span data-ttu-id="71e12-110">Naamgevings regels</span><span class="sxs-lookup"><span data-stu-id="71e12-110">Naming Conventions</span></span> ##

<span data-ttu-id="71e12-111">Om de Quantum Development Kit te bieden, streven we naar functie-en bewerkings namen die verquantumt ontwikkel aars om Program ma's te schrijven die gemakkelijk te lezen zijn en die verrassingen minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="71e12-111">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="71e12-112">Een belang rijk deel hiervan is dat wanneer we namen kiezen voor functies, bewerkingen en typen, de *woorden lijst* die programmeurs gebruiken om de Quantum concepten te Express, te bepalen. met onze keuzes kunnen we deze in hun inspanningen helpen om duidelijk te communiceren.</span><span class="sxs-lookup"><span data-stu-id="71e12-112">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="71e12-113">Dit is een verantwoordelijkheid voor ons om ervoor te zorgen dat de namen die we bieden, duidelijkheid geven in plaats van onduidelijkheid.</span><span class="sxs-lookup"><span data-stu-id="71e12-113">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="71e12-114">In deze sectie wordt beschreven hoe we voldoen aan deze verplichting in termen van expliciete richt lijnen die ons helpen bij het beste van de Q #-ontwikkel community.</span><span class="sxs-lookup"><span data-stu-id="71e12-114">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="71e12-115">Bewerkingen en functies</span><span class="sxs-lookup"><span data-stu-id="71e12-115">Operations and Functions</span></span> ###

<span data-ttu-id="71e12-116">Een van de eerste dingen die een naam moet bepalen, is of een bepaald symbool een functie of een bewerking vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="71e12-116">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="71e12-117">Het verschil tussen functies en bewerkingen is van cruciaal belang om te weten hoe een code blok zich gedraagt.</span><span class="sxs-lookup"><span data-stu-id="71e12-117">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="71e12-118">Om het onderscheid tussen functies en bewerkingen voor gebruikers te communiceren, vertrouwen we op die Q # modellen Quantum bewerkingen door het gebruik van neven effecten.</span><span class="sxs-lookup"><span data-stu-id="71e12-118">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="71e12-119">Dat wil zeggen dat een bewerking iets *doet* .</span><span class="sxs-lookup"><span data-stu-id="71e12-119">That is, an operation *does* something.</span></span>

<span data-ttu-id="71e12-120">Daarentegen beschrijven functies de wiskundige relaties tussen gegevens.</span><span class="sxs-lookup"><span data-stu-id="71e12-120">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="71e12-121">De expressie `Sin(PI() / 2.0)` *is* `1.0`en heeft niets te weten over de status van een programma of de qubits.</span><span class="sxs-lookup"><span data-stu-id="71e12-121">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="71e12-122">Samen vatting, bewerkingen doen zich voor in functies.</span><span class="sxs-lookup"><span data-stu-id="71e12-122">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="71e12-123">In dit onderscheid wordt gesuggereerd dat we bewerkingen als termen en functies als zelfstandig naam woord noemen.</span><span class="sxs-lookup"><span data-stu-id="71e12-123">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="71e12-124">Wanneer een door de gebruiker gedefinieerd type wordt gedeclareerd, wordt tegelijkertijd een nieuwe functie voor het maken van exemplaren van dat type gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="71e12-124">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="71e12-125">Vanuit dat perspectief moeten door de gebruiker gedefinieerde typen worden benoemd als zelfstandig naam woord, zodat zowel het type zelf als de functie-constructor consistente namen hebben.</span><span class="sxs-lookup"><span data-stu-id="71e12-125">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="71e12-126">Als dat het geval is, moet u ervoor zorgen dat de naam van de bewerking begint met de termen die duidelijk aangeven wat het effect van de bewerking is.</span><span class="sxs-lookup"><span data-stu-id="71e12-126">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="71e12-127">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="71e12-127">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="71e12-128">Een voor beeld van een specifieke bewerking in de duur van het verdient wanneer een bewerking een andere handeling als invoer gebruikt en aanroept.</span><span class="sxs-lookup"><span data-stu-id="71e12-128">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="71e12-129">In dergelijke gevallen is de actie die door de invoer bewerking wordt uitgevoerd niet duidelijk wanneer de buitenste bewerking is gedefinieerd, zodat de juiste term niet onmiddellijk wordt gewist.</span><span class="sxs-lookup"><span data-stu-id="71e12-129">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="71e12-130">We raden u aan om de term `Apply`, zoals in `ApplyIf`, `ApplyToEach`en `ApplyToFirst`.</span><span class="sxs-lookup"><span data-stu-id="71e12-130">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="71e12-131">Andere woorden kunnen in dit geval ook nuttig zijn, zoals in `IterateThroughCartesianPower`.</span><span class="sxs-lookup"><span data-stu-id="71e12-131">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="71e12-132">Term</span><span class="sxs-lookup"><span data-stu-id="71e12-132">Verb</span></span> | <span data-ttu-id="71e12-133">Verwacht effect</span><span class="sxs-lookup"><span data-stu-id="71e12-133">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="71e12-134">Aanvragen</span><span class="sxs-lookup"><span data-stu-id="71e12-134">Apply</span></span> | <span data-ttu-id="71e12-135">Een bewerking die is opgegeven als invoer, wordt aangeroepen</span><span class="sxs-lookup"><span data-stu-id="71e12-135">An operation provided as input is called</span></span> |
| <span data-ttu-id="71e12-136">Assert</span><span class="sxs-lookup"><span data-stu-id="71e12-136">Assert</span></span> | <span data-ttu-id="71e12-137">Een hypo these over het resultaat van een mogelijke quantum meting wordt gecontroleerd door een simulator</span><span class="sxs-lookup"><span data-stu-id="71e12-137">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="71e12-138">Bestek</span><span class="sxs-lookup"><span data-stu-id="71e12-138">Estimate</span></span> | <span data-ttu-id="71e12-139">Er wordt een klassieke waarde geretourneerd die een schatting vertegenwoordigt die uit een of meer metingen is getrokken</span><span class="sxs-lookup"><span data-stu-id="71e12-139">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="71e12-140">Maateenheidfilters</span><span class="sxs-lookup"><span data-stu-id="71e12-140">Measure</span></span> | <span data-ttu-id="71e12-141">Er wordt een quantum meting uitgevoerd en het resultaat wordt geretourneerd aan de gebruiker</span><span class="sxs-lookup"><span data-stu-id="71e12-141">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="71e12-142">Voorbereiden</span><span class="sxs-lookup"><span data-stu-id="71e12-142">Prepare</span></span> | <span data-ttu-id="71e12-143">Een bepaald REGI ster van qubits wordt geïnitialiseerd in een bepaalde status</span><span class="sxs-lookup"><span data-stu-id="71e12-143">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="71e12-144">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="71e12-144">Sample</span></span> | <span data-ttu-id="71e12-145">Er wordt een klassieke waarde geretourneerd op wille keurige wijze van distributie</span><span class="sxs-lookup"><span data-stu-id="71e12-145">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="71e12-146">Voor-functies voor komt u dat het gebruik van woorden wordt voor komen voor veelvoorkomende naam woorden (Zie de richt lijnen voor de onderstaande juiste naam woorden) of bijvoeglijke naam woorden:</span><span class="sxs-lookup"><span data-stu-id="71e12-146">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="71e12-147">In nagenoeg alle gevallen raden we u aan om eerdere participles te gebruiken, waar dat nodig is om aan te geven dat een functie naam sterk is verbonden met een actie of een neven effect ergens anders in een Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="71e12-147">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="71e12-148">`ControlledOnInt` maakt bijvoorbeeld gebruik van de participle-vorm van de term ' besturings element ' om aan te geven dat de functie fungeert als een bijvoeger om het argument te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="71e12-148">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="71e12-149">Deze naam heeft een extra voor deel van het afstemmen van de semantiek van de ingebouwde `Controlled` functor, zoals hieronder wordt besproken.</span><span class="sxs-lookup"><span data-stu-id="71e12-149">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="71e12-150">Op dezelfde manier kunnen zelfstandige naam van _agents_ worden gebruikt om functie-en UDT-namen te maken op basis van bewerkings namen, zoals in het geval van de name `Encoder` voor een UDT die sterk is gekoppeld aan `Encode`.</span><span class="sxs-lookup"><span data-stu-id="71e12-150">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-151">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-151">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-152">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-152">We suggest:</span></span>

- <span data-ttu-id="71e12-153">Termen gebruiken voor bewerkings namen.</span><span class="sxs-lookup"><span data-stu-id="71e12-153">Use verbs for operation names.</span></span>
- <span data-ttu-id="71e12-154">Gebruik naam woorden of bijvoegingen voor functie namen.</span><span class="sxs-lookup"><span data-stu-id="71e12-154">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="71e12-155">Gebruik zelfstandige naam woorden voor door de gebruiker gedefinieerde typen en kenmerken.</span><span class="sxs-lookup"><span data-stu-id="71e12-155">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="71e12-156">Voor alle aanroep bare namen gebruikt u `CamelCase` in een sterke voor keur om `pascalCase`, `snake_case`of `ANGRY_CASE`te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e12-156">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="71e12-157">Zorg er met name voor dat oproep bare namen beginnen met hoofd letters.</span><span class="sxs-lookup"><span data-stu-id="71e12-157">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="71e12-158">Gebruik voor alle lokale variabelen `pascalCase` in een sterke voor keur om `CamelCase`, `snake_case`of `ANGRY_CASE`te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e12-158">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="71e12-159">Zorg er met name voor dat lokale variabelen beginnen met kleine letters.</span><span class="sxs-lookup"><span data-stu-id="71e12-159">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="71e12-160">Vermijd het gebruik van onderstrepings `_` in functie-en bewerkings namen. gebruik naam ruimten en naam ruimte aliassen wanneer er extra hiërarchie niveaus nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="71e12-160">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-161">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-161">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="71e12-162">Naam</span><span class="sxs-lookup"><span data-stu-id="71e12-162">Name</span></span> | <span data-ttu-id="71e12-163">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71e12-163">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="71e12-164">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-164">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="71e12-165">Het gebruik van een term (' reflectie ') wissen om het effect van de bewerking aan te geven.</span><span class="sxs-lookup"><span data-stu-id="71e12-165">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="71e12-166">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-166">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="71e12-167">Het gebruik van de woord groep frase suggesties voor de functie, in plaats van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="71e12-167">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="71e12-168">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-168">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="71e12-169">Gebruik van `snake_case` Q #-notatie van contravenes.</span><span class="sxs-lookup"><span data-stu-id="71e12-169">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="71e12-170">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-170">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="71e12-171">Het gebruik van onderstrepings tekens intern voor de bewerkings naam contravenes Q #-notatie.</span><span class="sxs-lookup"><span data-stu-id="71e12-171">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="71e12-172">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-172">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="71e12-173">Als u een woord groep gebruikt, wordt gesuggereerd dat de functie een bewerking retourneert.</span><span class="sxs-lookup"><span data-stu-id="71e12-173">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="71e12-174">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-174">☑</span></span> | `function EqualityFact` | <span data-ttu-id="71e12-175">Het gebruik van zelfstandig naam woord ("feit") wissen om aan te geven dat dit een functie is, terwijl de bijvoeger.</span><span class="sxs-lookup"><span data-stu-id="71e12-175">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="71e12-176">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-176">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="71e12-177">Bij gebruik van term (' Get ') wordt voorgesteld dat dit een bewerking is.</span><span class="sxs-lookup"><span data-stu-id="71e12-177">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="71e12-178">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-178">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="71e12-179">Het gebruik van de woord groep van een zelfstandig nummer verwijst duidelijk naar het resultaat van het aanroepen van de UDT-constructor.</span><span class="sxs-lookup"><span data-stu-id="71e12-179">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="71e12-180">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-180">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="71e12-181">Het gebruik van een verbale woord groep adviseert dat de UDT-constructor een bewerking is.</span><span class="sxs-lookup"><span data-stu-id="71e12-181">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="71e12-182">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-182">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="71e12-183">Gebruik van de woord groep met zelfstandig naam communicatie communiceert het gebruik van het kenmerk.</span><span class="sxs-lookup"><span data-stu-id="71e12-183">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="71e12-184">Steno en afkortingen</span><span class="sxs-lookup"><span data-stu-id="71e12-184">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="71e12-185">Het bovenstaande advies ondanks dat er sprake is van een groot aantal vormen van steno met een gemeen schappelijke en pervasive gebruik in de Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="71e12-185">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="71e12-186">We raden u aan bestaande en algemene steno te gebruiken waar deze zich bevinden, met name voor bewerkingen die intrinsiek zijn voor de werking van een doel machine.</span><span class="sxs-lookup"><span data-stu-id="71e12-186">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="71e12-187">We kiezen bijvoorbeeld de naam `X` in plaats van `ApplyX`en `Rz` in plaats van `RotateAboutZ`.</span><span class="sxs-lookup"><span data-stu-id="71e12-187">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="71e12-188">Bij het gebruik van deze steno moeten de namen van de bewerkingen allemaal hoofd letters zijn (bijvoorbeeld: `MAJ`).</span><span class="sxs-lookup"><span data-stu-id="71e12-188">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="71e12-189">Bij het Toep assen van deze Conventie is een zorgvuldige toepassing vereist voor een vaak gebruikte acroniemen en initialisms zoals ' QFT ' voor ' Quantum Fourier Transform '.</span><span class="sxs-lookup"><span data-stu-id="71e12-189">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="71e12-190">We suggereren de volgende algemene .NET-conventies voor het gebruik van acroniemen en initialisms in volledige namen, waarbij u moet bepalen dat:</span><span class="sxs-lookup"><span data-stu-id="71e12-190">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="71e12-191">afkortingen van twee letters en initialisms worden in hoofd letters genoemd (bijvoorbeeld: `BE` voor "big-endian"),</span><span class="sxs-lookup"><span data-stu-id="71e12-191">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="71e12-192">alle langere acroniemen en initialisms worden genoemd in `CamelCase` (bijvoorbeeld: `Qft` voor "Quantum Fourier Transform")</span><span class="sxs-lookup"><span data-stu-id="71e12-192">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="71e12-193">Een bewerking die de QFT implementeert, kan dus `QFT` als steno worden genoemd, of als `ApplyQft`zijn geschreven.</span><span class="sxs-lookup"><span data-stu-id="71e12-193">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="71e12-194">Voor bijzonder gebruikte bewerkingen en functies kan het wenselijk zijn om een steno naam op te geven als _alias_ voor een langer formulier:</span><span class="sxs-lookup"><span data-stu-id="71e12-194">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-195">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-195">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-196">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-196">We suggest:</span></span>

- <span data-ttu-id="71e12-197">Overweeg vaak geaccepteerde en veelgebruikte steno namen als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="71e12-197">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="71e12-198">Gebruik hoofd letters voor Steno.</span><span class="sxs-lookup"><span data-stu-id="71e12-198">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="71e12-199">Gebruik hoofd letters voor korte (twee letters) acroniemen en initialisms.</span><span class="sxs-lookup"><span data-stu-id="71e12-199">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="71e12-200">Gebruik `CamelCase` langer (drie of meer letter) acroniemen en initialisms.</span><span class="sxs-lookup"><span data-stu-id="71e12-200">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-201">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-201">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="71e12-202">Naam</span><span class="sxs-lookup"><span data-stu-id="71e12-202">Name</span></span> | <span data-ttu-id="71e12-203">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71e12-203">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="71e12-204">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-204">☑</span></span> | `X` | <span data-ttu-id="71e12-205">Goed te begrijpen steno voor ' een $X $ Transformation ' toep assen '</span><span class="sxs-lookup"><span data-stu-id="71e12-205">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="71e12-206">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-206">☑</span></span> | `CNOT` | <span data-ttu-id="71e12-207">Goed te begrijpen steno voor "Controlled-NOT"</span><span class="sxs-lookup"><span data-stu-id="71e12-207">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="71e12-208">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-208">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="71e12-209">Steno mag niet `CamelCase`.</span><span class="sxs-lookup"><span data-stu-id="71e12-209">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="71e12-210">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-210">☑</span></span> | `ApplyQft` | <span data-ttu-id="71e12-211">Common Initiation "QFT" wordt weer gegeven als onderdeel van een lange formulier naam.</span><span class="sxs-lookup"><span data-stu-id="71e12-211">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="71e12-212">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-212">☑</span></span> | `QFT` | <span data-ttu-id="71e12-213">Common Initiation "QFT" wordt weer gegeven als onderdeel van een steno naam.</span><span class="sxs-lookup"><span data-stu-id="71e12-213">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="71e12-214">Juiste naam woorden in namen</span><span class="sxs-lookup"><span data-stu-id="71e12-214">Proper Nouns in Names</span></span> ###

<span data-ttu-id="71e12-215">In het geval van een fysieke waarde is het gebruikelijk om dingen te benoemen na de eerste persoon die over hen publiceert. de meeste niet-physicists zijn niet bekend met de namen van iedereen en alle geschiedenis.</span><span class="sxs-lookup"><span data-stu-id="71e12-215">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="71e12-216">Het is te sterk om te voldoen aan de naamgevings conventies van de fysica, waardoor er een aanzienlijke barrière kan worden ingevoerd, omdat gebruikers van andere achtergronden een groot aantal schijnbaar ondoorzichtige namen moeten leren om veelvoorkomende bewerkingen en concepten te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e12-216">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="71e12-217">Daarom is het raadzaam om, waar mogelijk, veelvoorkomende algemene naam woorden die een concept beschrijven, in hoge voor keur te worden aangenomen voor de juiste naam woorden die de publicatie geschiedenis van een concept beschrijven.</span><span class="sxs-lookup"><span data-stu-id="71e12-217">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="71e12-218">Een voor beeld hiervan is dat de afzonderlijk beheerde SWAPs en dubbele controle niet worden uitgevoerd, ook wel de "Fredkin"-en "Toffoli"-bewerkingen worden genoemd in academische literatuur, maar worden aangeduid met Q #, voornamelijk als `CSWAP` en `CCNOT`.</span><span class="sxs-lookup"><span data-stu-id="71e12-218">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="71e12-219">In beide gevallen bieden de API-documentatie opmerkingen synoniemen op basis van de juiste naam woorden, samen met alle relevante bron vermeldingen.</span><span class="sxs-lookup"><span data-stu-id="71e12-219">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="71e12-220">Deze voor keur is vooral belang rijk, omdat het gebruik van de juiste zelfstandige naam woorden altijd nood zakelijk is. Q # volgt de traditie die is ingesteld door veel klassieke talen, bijvoorbeeld, en verwijst naar `Bool` typen in verwijzingen naar Booleaanse logica, die op zijn beurt de naam in acht neemt van George Boole.</span><span class="sxs-lookup"><span data-stu-id="71e12-220">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="71e12-221">Enkele Quantum concepten worden op een vergelijk bare manier genoemd, met inbegrip van het `Pauli` type ingebouwd in de Q #-taal.</span><span class="sxs-lookup"><span data-stu-id="71e12-221">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="71e12-222">Door het gebruik van de juiste zelfstandige naam woorden, waarbij dit gebruik niet essentieel is, te minimaliseren, kunnen we de impact verminderen waarbij de juiste zelfstandige naam woorden niet redelijkerwijs worden vermeden.</span><span class="sxs-lookup"><span data-stu-id="71e12-222">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-223">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-223">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="71e12-224">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-224">We suggest:</span></span>

- <span data-ttu-id="71e12-225">Vermijd het gebruik van de juiste zelfstandige naam woorden in namen.</span><span class="sxs-lookup"><span data-stu-id="71e12-225">Avoid the use of proper nouns in names.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-226">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-226">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="71e12-227">Type conversies</span><span class="sxs-lookup"><span data-stu-id="71e12-227">Type Conversions</span></span> ###

<span data-ttu-id="71e12-228">Aangezien Q # een sterk en statisch getypte taal is, kan een waarde van één type alleen worden gebruikt als waarde van een ander type met behulp van een expliciete aanroep van een type conversie functie.</span><span class="sxs-lookup"><span data-stu-id="71e12-228">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="71e12-229">Dit is in tegens telling tot talen waarmee waarden typen impliciet kunnen worden gewijzigd (bijvoorbeeld: type promotie) of via casting.</span><span class="sxs-lookup"><span data-stu-id="71e12-229">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="71e12-230">Als gevolg hiervan spelen functies van het type conversie een belang rijke rol bij het ontwikkelen van Q #-bibliotheken en vormen ze een van de vaak voorkomende beslissingen over de naamgeving.</span><span class="sxs-lookup"><span data-stu-id="71e12-230">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="71e12-231">Maar omdat type conversies altijd _deterministisch_zijn, kunnen ze worden geschreven als functies en dus onder de bovenstaande aanbeveling vallen.</span><span class="sxs-lookup"><span data-stu-id="71e12-231">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="71e12-232">In het bijzonder raden we aan dat type conversie functies nooit moeten worden benoemd als woorden (bijvoorbeeld: `ConvertToX`) of woord voorstandlijke voor keuren (`ToX`), maar moeten worden benoemd als voor zetsels van bijvoeglijke woord groepen die de bron-en doel typen aangeven (`XAsY`).</span><span class="sxs-lookup"><span data-stu-id="71e12-232">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="71e12-233">Bij het weer geven van matrix typen in functie namen van type conversie wordt aangeraden de steno `Arr`.</span><span class="sxs-lookup"><span data-stu-id="71e12-233">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="71e12-234">Als buitengewone omstandigheden worden geblokkeerd, wordt aangeraden alle type conversie functies te gebruiken met `As` zodat ze snel kunnen worden geïdentificeerd.</span><span class="sxs-lookup"><span data-stu-id="71e12-234">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-235">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-235">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-236">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-236">We suggest:</span></span>

- <span data-ttu-id="71e12-237">Als een functie een waarde van het type `X` converteert naar een waarde van het type `Y`, gebruikt u de naam `AsY` of `XAsY`.</span><span class="sxs-lookup"><span data-stu-id="71e12-237">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-238">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-238">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="71e12-239">Naam</span><span class="sxs-lookup"><span data-stu-id="71e12-239">Name</span></span> | <span data-ttu-id="71e12-240">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71e12-240">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="71e12-241">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-241">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="71e12-242">De voor positie ' to ' resulteert in een verbale woord groep, wat een bewerking aangeeft en niet een functie.</span><span class="sxs-lookup"><span data-stu-id="71e12-242">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="71e12-243">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-243">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="71e12-244">Het invoer type is niet duidelijk uit de functie naam.</span><span class="sxs-lookup"><span data-stu-id="71e12-244">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="71e12-245">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-245">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="71e12-246">De invoer-en uitvoer typen worden in de verkeerde volg orde weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="71e12-246">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="71e12-247">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-247">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="71e12-248">Zowel de invoer typen als de uitvoer typen zijn duidelijk.</span><span class="sxs-lookup"><span data-stu-id="71e12-248">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="71e12-249">Privé-of interne namen</span><span class="sxs-lookup"><span data-stu-id="71e12-249">Private or Internal Names</span></span> ###

<span data-ttu-id="71e12-250">In veel gevallen is een naam uitsluitend bedoeld voor intern gebruik in een bibliotheek of project en is dit geen gegarandeerd deel van de API die wordt aangeboden door een bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="71e12-250">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="71e12-251">Het is handig om duidelijk aan te geven dat dit het geval is bij het benoemen van functies en bewerkingen, zodat onbedoelde afhankelijkheden op interne code duidelijk worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="71e12-251">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="71e12-252">Als een bewerking of functie niet bedoeld is voor direct gebruik, maar moet worden gebruikt door een overeenkomende aanroep die door een gedeeltelijke toepassing wordt uitgevoerd, kunt u overwegen een naam te gebruiken die begint met `_` voor de aanroep bare die gedeeltelijk is toegepast.</span><span class="sxs-lookup"><span data-stu-id="71e12-252">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with `_` for the callable that is partially applied.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-253">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-253">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-254">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-254">We suggest:</span></span>

- <span data-ttu-id="71e12-255">Wanneer een functie, bewerking of door de gebruiker gedefinieerd type geen deel uitmaakt van de open bare API voor een Q #-bibliotheek of-programma, moet u ervoor zorgen dat de naam begint met een onderstrepings teken (`_`).</span><span class="sxs-lookup"><span data-stu-id="71e12-255">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that its name begins with a leading underscore (`_`).</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-256">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-256">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="71e12-257">Naam</span><span class="sxs-lookup"><span data-stu-id="71e12-257">Name</span></span> | <span data-ttu-id="71e12-258">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71e12-258">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="71e12-259">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-259">☒</span></span> | <s>`ApplyDecomposedOperation_`</s> | <span data-ttu-id="71e12-260">Het onderstrepings teken `_` mag niet aan het einde van de naam worden weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="71e12-260">The underscore `_` should not appear at the end of the name.</span></span> |
| <span data-ttu-id="71e12-261">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-261">☑</span></span> | `_ApplyDecomposedOperation` | <span data-ttu-id="71e12-262">Het onderstrepings teken `_` op het begin duidelijk aangeeft dat deze bewerking alleen voor intern gebruik is.</span><span class="sxs-lookup"><span data-stu-id="71e12-262">The underscore `_` at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***

### <a name="variants"></a><span data-ttu-id="71e12-263">Qua</span><span class="sxs-lookup"><span data-stu-id="71e12-263">Variants</span></span> ###

<span data-ttu-id="71e12-264">Hoewel deze beperking mogelijk niet persistent is in toekomstige versies van Q #, is het altijd zo dat er vaak groepen van gerelateerde bewerkingen of functies zijn die worden onderscheiden door welke functors hun invoer ondersteunen, of op basis van de concrete typen van de argumenten.</span><span class="sxs-lookup"><span data-stu-id="71e12-264">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="71e12-265">Deze groepen kunnen worden onderscheiden met dezelfde hoofd naam, gevolgd door een of twee letters die de variant aangeven.</span><span class="sxs-lookup"><span data-stu-id="71e12-265">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="71e12-266">Achtervoegsel</span><span class="sxs-lookup"><span data-stu-id="71e12-266">Suffix</span></span> | <span data-ttu-id="71e12-267">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71e12-267">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="71e12-268">Verwachte invoer voor ondersteuning van `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="71e12-268">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="71e12-269">Verwachte invoer voor ondersteuning van `Controlled`</span><span class="sxs-lookup"><span data-stu-id="71e12-269">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="71e12-270">Verwachte invoer voor ondersteuning van `Controlled` en `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="71e12-270">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="71e12-271">Invoer-of invoer gegevens zijn van het type `Int`</span><span class="sxs-lookup"><span data-stu-id="71e12-271">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="71e12-272">Invoer-of invoer gegevens zijn van het type `Double`</span><span class="sxs-lookup"><span data-stu-id="71e12-272">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="71e12-273">Invoer-of invoer gegevens zijn van het type `BigInt`</span><span class="sxs-lookup"><span data-stu-id="71e12-273">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-274">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-274">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-275">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-275">We suggest:</span></span>

- <span data-ttu-id="71e12-276">Als een functie of bewerking niet is gerelateerd aan vergelijk bare functies of bewerkingen door de typen en functor-ondersteuning van de invoer, mag u geen achtervoegsel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e12-276">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="71e12-277">Als een functie of bewerking is gerelateerd aan vergelijk bare functies of bewerkingen door de typen en functor-ondersteuning van de invoer, gebruikt u achtervoegsels zoals in de bovenstaande tabel om varianten te onderscheiden.</span><span class="sxs-lookup"><span data-stu-id="71e12-277">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-278">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-278">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="71e12-279">Argumenten en variabelen</span><span class="sxs-lookup"><span data-stu-id="71e12-279">Arguments and Variables</span></span> ###

<span data-ttu-id="71e12-280">Een belang rijk doel van de Q #-code voor een functie of bewerking is dat deze eenvoudig kan worden gelezen en begrepen.</span><span class="sxs-lookup"><span data-stu-id="71e12-280">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="71e12-281">Op dezelfde manier moeten de namen van invoer-en type argumenten communiceren hoe een functie of argument wordt gebruikt wanneer dit wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="71e12-281">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-282">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-282">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-283">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-283">We suggest:</span></span>

- <span data-ttu-id="71e12-284">Voor alle variabelen en invoer namen gebruikt u `pascalCase` in een sterke voor keur om `CamelCase`, `snake_case`of `ANGRY_CASE`te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e12-284">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="71e12-285">De invoer namen moeten een beschrijvende naam hebben. Vermijd waar mogelijk een of twee letter namen.</span><span class="sxs-lookup"><span data-stu-id="71e12-285">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="71e12-286">Bewerkingen en functies die precies één type argument accepteren, moeten dit type argument aangeven door `T` als de bijbehorende rol duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="71e12-286">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="71e12-287">Als een functie of bewerking meerdere type argumenten nodig heeft, of als de rol van een enkel type argument niet duidelijk is, kunt u een korte, gekapitale woord, voorafgegaan door `T` (bijvoorbeeld: `TOutput`) gebruiken voor elk type.</span><span class="sxs-lookup"><span data-stu-id="71e12-287">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="71e12-288">Typ geen type namen in argument-en variabelenamen; deze informatie kan worden verstrekt door uw ontwikkel omgeving.</span><span class="sxs-lookup"><span data-stu-id="71e12-288">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="71e12-289">Denoteer scalaire typen met hun letterlijke namen (`flagQubit`) en matrix typen met een meervoud (`measResults`).</span><span class="sxs-lookup"><span data-stu-id="71e12-289">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="71e12-290">Voor matrices van qubits met name kunt u deze typen identificeren door `Register` waarbij de naam verwijst naar een reeks qubits die op een of andere manier nauw verwant zijn.</span><span class="sxs-lookup"><span data-stu-id="71e12-290">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="71e12-291">Variabelen die als indexen worden gebruikt in matrices, moeten beginnen met `idx` en moeten een enkelvoud (bijvoorbeeld: `things[idxThing]`) zijn.</span><span class="sxs-lookup"><span data-stu-id="71e12-291">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="71e12-292">In het bijzonder Vermijd het gebruik van variabelen namen met één letter als indices. Overweeg het gebruik van `idx` mini maal.</span><span class="sxs-lookup"><span data-stu-id="71e12-292">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="71e12-293">Variabelen die worden gebruikt om de lengte van matrices te bewaren, moeten beginnen met `n` en moeten worden gemeervoudt (bijvoorbeeld: `nThings`).</span><span class="sxs-lookup"><span data-stu-id="71e12-293">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-294">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-294">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="71e12-295">Door de gebruiker gedefinieerd type met de naam items</span><span class="sxs-lookup"><span data-stu-id="71e12-295">User Defined Type Named Items</span></span> ###

<span data-ttu-id="71e12-296">Benoemde items in door de gebruiker gedefinieerde typen moeten worden aangeduid als `CamelCase`, zelfs invoer voor UDT-constructors.</span><span class="sxs-lookup"><span data-stu-id="71e12-296">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="71e12-297">Dit helpt om benoemde items duidelijk te scheiden van verwijzingen naar variabelen met een lokaal bereik bij gebruik van een accessor-notatie (bijvoorbeeld: `callable::Apply`) of Copy-and-update-notatie (`set arr w/= Data <- newData`).</span><span class="sxs-lookup"><span data-stu-id="71e12-297">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-298">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-298">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-299">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-299">We suggest:</span></span>

- <span data-ttu-id="71e12-300">Benoemde items in UDT-constructors moeten worden aangeduid als `CamelCase`; dat wil zeggen dat ze met een begin hoofdletter beginnen.</span><span class="sxs-lookup"><span data-stu-id="71e12-300">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="71e12-301">Benoemde items die aan bewerkingen worden omgezet, moeten de naam werk woord fasen hebben.</span><span class="sxs-lookup"><span data-stu-id="71e12-301">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="71e12-302">Benoemde items die niet naar bewerkingen worden omgezet, moeten een naam hebben als woord groepen.</span><span class="sxs-lookup"><span data-stu-id="71e12-302">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="71e12-303">Voor UDTs moet er een enkel benoemd item met de naam `Apply` worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="71e12-303">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-304">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-304">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="71e12-305">Fragment</span><span class="sxs-lookup"><span data-stu-id="71e12-305">Snippet</span></span> | <span data-ttu-id="71e12-306">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71e12-306">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="71e12-307">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-307">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="71e12-308">De naam `Apply` is `CamelCase`een onopgemaakte verbale woord groep waarmee wordt voorgesteld dat het benoemde item een bewerking is.</span><span class="sxs-lookup"><span data-stu-id="71e12-308">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="71e12-309">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-309">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="71e12-310">Benoemde items moeten beginnen met een eerste hoofd letter.</span><span class="sxs-lookup"><span data-stu-id="71e12-310">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="71e12-311">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-311">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="71e12-312">Benoemde items die worden omgezet in-functies, moeten worden benoemd als woord groepen, niet als verbale woord groepen.</span><span class="sxs-lookup"><span data-stu-id="71e12-312">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="71e12-313">Invoer conventies</span><span class="sxs-lookup"><span data-stu-id="71e12-313">Input Conventions</span></span> ##

<span data-ttu-id="71e12-314">Wanneer een ontwikkelaar een bewerking of functie aanroept, moeten de verschillende invoer waarden voor die bewerking of functie worden opgegeven in een bepaalde volg orde, waardoor de cognitieve belasting die een ontwikkelaar gemerkt, wordt gebruikt om een bibliotheek te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e12-314">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="71e12-315">Met name de taak van het onthouden van invoer orders is vaak een afleiding van de taak bij de hand: het Program meren van een implementatie van een Quantum algoritme.</span><span class="sxs-lookup"><span data-stu-id="71e12-315">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="71e12-316">Hoewel uitgebreide ondersteuning voor IDE dit in grote mate kan beperken, kan een goed ontwerp en de gang bare conventies ook helpen om de cognitieve belasting van een API te minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="71e12-316">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="71e12-317">Waar mogelijk kan het nuttig zijn om het aantal ingevoerde invoer waarden te verminderen dat wordt verwacht door een bewerking of functie, zodat de rol van elke invoer onmiddellijk duidelijker is voor ontwikkel aars die de bewerking of functie aanroepen, en naar ontwikkel aars die code later lezen.</span><span class="sxs-lookup"><span data-stu-id="71e12-317">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="71e12-318">Met name wanneer het niet mogelijk is om het aantal argumenten voor een bewerking of functie te verminderen, is het belang rijk om een consistente volg orde te hebben die het voors pellen van de gebruiker bij de voor spelling van de invoer verkleint.</span><span class="sxs-lookup"><span data-stu-id="71e12-318">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="71e12-319">We raden u aan om de conventies voor invoer volgorde in te stellen die grotendeels afleiden van een deel van de toepassing als generalisatie van currying f (x, y) ≡ f (x) (y).</span><span class="sxs-lookup"><span data-stu-id="71e12-319">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="71e12-320">Het Toep assen van de eerste argumenten zou dus gedeeltelijk van toepassing moeten zijn en die nuttig is voor eigen rechts, wanneer dat redelijk is.</span><span class="sxs-lookup"><span data-stu-id="71e12-320">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="71e12-321">U kunt de volgende volg orde van argumenten gebruiken om dit principe te volgen:</span><span class="sxs-lookup"><span data-stu-id="71e12-321">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="71e12-322">Klassieke niet-aanroep bare argumenten, zoals hoeken, vectoren van bevoegdheden, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="71e12-322">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="71e12-323">Aanroep bare argumenten (functies en argumenten).</span><span class="sxs-lookup"><span data-stu-id="71e12-323">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="71e12-324">Als beide functies en bewerkingen worden uitgevoerd als argumenten, kunt u de bewerkingen na functies plaatsen.</span><span class="sxs-lookup"><span data-stu-id="71e12-324">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="71e12-325">Verzamelingen `Map`die op een vergelijk bare manier worden verwerkt door aanroepen van argumenten, `Iter`, `Enumerate`en `Fold`.</span><span class="sxs-lookup"><span data-stu-id="71e12-325">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="71e12-326">Qubit argumenten gebruikt als besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="71e12-326">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="71e12-327">Qubit argumenten die als doelen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71e12-327">Qubit arguments used as targets.</span></span>

<span data-ttu-id="71e12-328">Bekijk een bewerkings `ApplyPhaseEstimationIteration` voor gebruik in de fase-schatting die een hoek en een Oracle afneemt, de hoek door gegeven aan `Rz` gewijzigd door een matrix met verschillende schaal factoren en vervolgens de toepassingen van de Oracle beheert.</span><span class="sxs-lookup"><span data-stu-id="71e12-328">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="71e12-329">De invoer wordt op de volgende manier door `ApplyPhaseEstimationIteration`:</span><span class="sxs-lookup"><span data-stu-id="71e12-329">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

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
<span data-ttu-id="71e12-330">Als een speciaal geval van het minimaliseren van de verrassingen, simuleren sommige functies en bewerkingen het gedrag van de ingebouwde functors-`Adjoint` en `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="71e12-330">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="71e12-331">`ControlledOnInt<'T>` is bijvoorbeeld van het type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, zodanig dat `ControlledOnInt<Qubit[]>(5, _)` fungeert als de `Controlled` functor, maar op de voor waarde dat het controle register de status $ \ket{5} = \ket{101}$ vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="71e12-331">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="71e12-332">Daarom verwacht een ontwikkelaar dat de invoer van `ControlledOnInt` de aanroepable te zetten die het laatst is getransformeerd en dat de resulterende bewerking de invoer `(Qubit[], 'T)`---dezelfde volg orde gebruikt, gevolgd door de uitvoer van de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="71e12-332">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-333">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-333">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-334">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-334">We suggest:</span></span>

- <span data-ttu-id="71e12-335">Gebruik invoer volgorden die consistent zijn met het gebruik van een gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="71e12-335">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="71e12-336">Gebruik invoer volgorden die consistent zijn met ingebouwde functors.</span><span class="sxs-lookup"><span data-stu-id="71e12-336">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="71e12-337">Plaats alle klassieke invoer vóór een Quantum invoer.</span><span class="sxs-lookup"><span data-stu-id="71e12-337">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-338">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-338">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="71e12-339">Documentatie conventies</span><span class="sxs-lookup"><span data-stu-id="71e12-339">Documentation Conventions</span></span> ##

<span data-ttu-id="71e12-340">De Q #-taal maakt het mogelijk om documentatie toe te voegen aan bewerkingen, functies en door de gebruiker gedefinieerde typen door het gebruik van speciaal opgemaakte documentatie opmerkingen.</span><span class="sxs-lookup"><span data-stu-id="71e12-340">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="71e12-341">Deze documentatie opmerkingen worden aangeduid met drievoudige slashes (`///`) en zijn kleine [GeDocFXeerde](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documenten die kunnen worden gebruikt voor het beschrijven van het doel van elke bewerking, functie en door de gebruiker gedefinieerd type, welke invoer elk verwacht, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="71e12-341">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="71e12-342">De compiler die wordt geleverd met de Quantum Development Kit, haalt deze opmerkingen op en gebruikt deze om documentatie van de typeset te helpen typen die op https://docs.microsoft.com/quantum lijkt.</span><span class="sxs-lookup"><span data-stu-id="71e12-342">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="71e12-343">Op dezelfde manier gebruikt de taal server van de Quantum Development Kit deze opmerkingen om gebruikers te helpen bij het aanwijzen van de muis aanwijzer over symbolen in hun Q #-code.</span><span class="sxs-lookup"><span data-stu-id="71e12-343">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="71e12-344">Het gebruik van documentatie opmerkingen kan gebruikers helpen om code te maken met behulp van een nuttige referentie voor informatie die niet eenvoudig kan worden weer gegeven met de andere conventies in dit document.</span><span class="sxs-lookup"><span data-stu-id="71e12-344">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

<div class="nextstepaction"><span data-ttu-id="71e12-345">
    [Naslag informatie](xref:microsoft.quantum.language.statements#documentation-comments) voor de syntaxis van documentatie-opmerkingen
</span><span class="sxs-lookup"><span data-stu-id="71e12-345">
    [Documentation comment syntax reference](xref:microsoft.quantum.language.statements#documentation-comments)
</span></span></div>

<span data-ttu-id="71e12-346">Als u deze functionaliteit effectief wilt gebruiken om gebruikers te helpen, raden we u aan om een aantal zaken te houden wanneer u documentatie opmerkingen schrijft.</span><span class="sxs-lookup"><span data-stu-id="71e12-346">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-347">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-347">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="71e12-348">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-348">We suggest:</span></span>

- <span data-ttu-id="71e12-349">Elke open bare functie, bewerking en door de gebruiker gedefinieerd type moeten onmiddellijk worden voorafgegaan door een documentatie opmerking.</span><span class="sxs-lookup"><span data-stu-id="71e12-349">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="71e12-350">Elke documentatie opmerking moet mini maal de volgende secties bevatten:</span><span class="sxs-lookup"><span data-stu-id="71e12-350">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="71e12-351">Samenvatting</span><span class="sxs-lookup"><span data-stu-id="71e12-351">Summary</span></span>
    - <span data-ttu-id="71e12-352">Invoer</span><span class="sxs-lookup"><span data-stu-id="71e12-352">Input</span></span>
    - <span data-ttu-id="71e12-353">Uitvoer (indien van toepassing)</span><span class="sxs-lookup"><span data-stu-id="71e12-353">Output (if applicable)</span></span>
- <span data-ttu-id="71e12-354">Zorg ervoor dat alle samen vattingen twee zinnen of minder zijn.</span><span class="sxs-lookup"><span data-stu-id="71e12-354">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="71e12-355">Als er meer ruimte nodig is, geeft u een `# Description` sectie direct na `# Summary` met volledige informatie.</span><span class="sxs-lookup"><span data-stu-id="71e12-355">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="71e12-356">Als dat niet het geval is, kunt u geen wiskundige formules in samen vattingen gebruiken, omdat niet alle clients TeX-notatie in samen vattingen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="71e12-356">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="71e12-357">Houd er rekening mee dat bij het schrijven van Prose-documenten (bijvoorbeeld TeX of prijs verlaging) het voor keur is dat er langere lijn lengten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71e12-357">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="71e12-358">Geef alle relevante wiskundige expressies op in de sectie `# Description`.</span><span class="sxs-lookup"><span data-stu-id="71e12-358">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="71e12-359">Herhaal bij het beschrijven van invoer de typen van elke invoer niet, aangezien deze kunnen worden afgeleid door de compiler en het risico dat inconsistentie wordt geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="71e12-359">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="71e12-360">Geef voor beelden op die van toepassing zijn, elk in hun eigen `# Example` sectie.</span><span class="sxs-lookup"><span data-stu-id="71e12-360">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="71e12-361">Geef een korte beschrijving van elk voor beeld voordat u code vermeldt.</span><span class="sxs-lookup"><span data-stu-id="71e12-361">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="71e12-362">Vermeld alle relevante academische publicaties (bijvoorbeeld: papers, procedures, blog berichten en alternatieve implementaties) in een `# References` sectie als een lijst met opsommings tekens van koppelingen.</span><span class="sxs-lookup"><span data-stu-id="71e12-362">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="71e12-363">Zorg ervoor dat alle bron vermelding-koppelingen, waar mogelijk, permanent en onveranderbare id's (DOIs of genummerde arXiv) zijn.</span><span class="sxs-lookup"><span data-stu-id="71e12-363">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="71e12-364">Wanneer een bewerking of functie is gerelateerd aan andere bewerkingen of functies van functor varianten, vermeldt u andere varianten als opsommings tekens in het gedeelte `# See Also`.</span><span class="sxs-lookup"><span data-stu-id="71e12-364">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="71e12-365">Laat een lege opmerkings regel staan tussen de secties van niveau 1 (`/// #`), maar laat geen lege regel staan tussen de secties van niveau 2 (`/// ##`).</span><span class="sxs-lookup"><span data-stu-id="71e12-365">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-366">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-366">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="71e12-367">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-367">☑</span></span> ####

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

## <a name="formatting-conventions"></a><span data-ttu-id="71e12-368">Opmaak conventies</span><span class="sxs-lookup"><span data-stu-id="71e12-368">Formatting Conventions</span></span> ##

<span data-ttu-id="71e12-369">Naast de voor gaande suggesties is het handig om code zo leesbaar mogelijk te maken voor het gebruik van consistente opmaak regels.</span><span class="sxs-lookup"><span data-stu-id="71e12-369">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="71e12-370">Dergelijke opmaak regels worden op een wille keurige manier en in het algemeen op persoonlijke wijze in het gepaareerd.</span><span class="sxs-lookup"><span data-stu-id="71e12-370">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="71e12-371">Het is echter raadzaam een consistente set opmaak conventies binnen een groep mede werkers te onderhouden, met name voor grote Q #-projecten, zoals de Quantum Development Kit zelf.</span><span class="sxs-lookup"><span data-stu-id="71e12-371">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="71e12-372">Deze regels kunnen automatisch worden toegepast met behulp van het opmaak programma dat is geïntegreerd met de compiler Q #.</span><span class="sxs-lookup"><span data-stu-id="71e12-372">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="71e12-373">Hulp</span><span class="sxs-lookup"><span data-stu-id="71e12-373">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="71e12-374">Suggesties voor:</span><span class="sxs-lookup"><span data-stu-id="71e12-374">We suggest:</span></span>

- <span data-ttu-id="71e12-375">Gebruik vier spaties in plaats van tabs voor portabiliteit.</span><span class="sxs-lookup"><span data-stu-id="71e12-375">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="71e12-376">Bijvoorbeeld in VS code:</span><span class="sxs-lookup"><span data-stu-id="71e12-376">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="71e12-377">Regel terugloop om 79 tekens waar redelijk.</span><span class="sxs-lookup"><span data-stu-id="71e12-377">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="71e12-378">Gebruik spaties om binaire Opera tors.</span><span class="sxs-lookup"><span data-stu-id="71e12-378">Use spaces around binary operators.</span></span>
- <span data-ttu-id="71e12-379">Gebruik spaties aan beide zijden van de dubbele punten die worden gebruikt voor type annotaties.</span><span class="sxs-lookup"><span data-stu-id="71e12-379">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="71e12-380">Gebruik één spatie na komma's die worden gebruikt in matrix-en tuple-letterlijke waarden (bijvoorbeeld: in ingangen naar functies en bewerkingen).</span><span class="sxs-lookup"><span data-stu-id="71e12-380">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="71e12-381">Gebruik geen spaties na een functie, bewerking of UDT-naam, of na de `@` in kenmerk declaraties.</span><span class="sxs-lookup"><span data-stu-id="71e12-381">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="71e12-382">Elke kenmerk declaratie moet op een eigen regel staan.</span><span class="sxs-lookup"><span data-stu-id="71e12-382">Each attribute declaration should be on its own line.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="71e12-383">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71e12-383">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="71e12-384">Fragment</span><span class="sxs-lookup"><span data-stu-id="71e12-384">Snippet</span></span> | <span data-ttu-id="71e12-385">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71e12-385">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="71e12-386">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-386">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="71e12-387">Gebruik spaties om binaire Opera tors.</span><span class="sxs-lookup"><span data-stu-id="71e12-387">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="71e12-388">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-388">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="71e12-389">Gebruik spaties rondom type aantekening.</span><span class="sxs-lookup"><span data-stu-id="71e12-389">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="71e12-390">☑</span><span class="sxs-lookup"><span data-stu-id="71e12-390">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="71e12-391">De items in de invoer-tuple zijn op de juiste wijze voor de Lees baarheid.</span><span class="sxs-lookup"><span data-stu-id="71e12-391">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="71e12-392">☒</span><span class="sxs-lookup"><span data-stu-id="71e12-392">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="71e12-393">Spaties moeten worden onderdrukt na functie-, bewerking-of UDT-namen.</span><span class="sxs-lookup"><span data-stu-id="71e12-393">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***

