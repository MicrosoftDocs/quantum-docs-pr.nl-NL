---
title: Documentatie over micro soft QDK
description: Meer informatie over het bijdragen van conceptuele of API-inhoud aan de micro soft Quantum documentation set.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
ms.openlocfilehash: ed5ab5df9de5d71ccd922cd430cf15779806dd6a
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022638"
---
# <a name="improving-documentation"></a><span data-ttu-id="331ad-103">Documentatie verbeteren</span><span class="sxs-lookup"><span data-stu-id="331ad-103">Improving Documentation</span></span>

<span data-ttu-id="331ad-104">De documentatie voor de Quantum Development Kit gaat over verschillende formulieren, waardoor de informatie gemakkelijk beschikbaar is voor Quantum ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="331ad-104">The documentation for the Quantum Development Kit takes on several different forms, such that information is readily available to quantum developers.</span></span>

<span data-ttu-id="331ad-105">Aan de hand van de beginselen van [documenten als code](https://www.writethedocs.org/guide/docs-as-code/)is alle Quantum Development Kit-documentatie ingedeeld als code en wordt beheerd met behulp van Git op dezelfde manier als de bron code die wordt gebruikt om de Quantum Development Kit te bouwen.</span><span class="sxs-lookup"><span data-stu-id="331ad-105">Following the principles of [Docs as Code](https://www.writethedocs.org/guide/docs-as-code/), all Quantum Development Kit documentation is formatted as code and is managed using Git in the same way as the source code that is used to build the Quantum Development Kit.</span></span>
<span data-ttu-id="331ad-106">In het algemeen is de code-documentatie voor het terugzetten van verschillende vormen van [prijs verlaging](https://daringfireball.net/projects/markdown/), een taal voor het schrijven van RTF-tekst in een onbewerkte tekst indeling die eenvoudig te gebruiken is op de opdracht regel, in ide's en met broncode beheer.</span><span class="sxs-lookup"><span data-stu-id="331ad-106">For the most part, the code backing documentation consists of various forms of [Markdown](https://daringfireball.net/projects/markdown/), a language for writing out richly formatted text in a plain text format that's easy to use at the command line, in IDEs, and with source control.</span></span>
<span data-ttu-id="331ad-107">We gaan de [MathJax](https://www.mathjax.org/) -bibliotheek op dezelfde manier gebruiken voor het opmaken van wiskunde in documentatie met behulp van de latex-taal, zoals hieronder beschreven.</span><span class="sxs-lookup"><span data-stu-id="331ad-107">We similarly adopt the [MathJax](https://www.mathjax.org/) library to allow for formatting mathematics in documentation using the LaTeX language, as detailed further below.</span></span>


<span data-ttu-id="331ad-108">Dit betekent dat elke vorm van documentatie enigszins in de details kan verschillen:</span><span class="sxs-lookup"><span data-stu-id="331ad-108">That said, each form of documentation does vary somewhat in the details:</span></span>

- <span data-ttu-id="331ad-109">De **conceptuele documentatie** bestaat uit een set artikelen die worden gepubliceerd op https://docs.microsoft.com/quantumen die alles beschrijft uit de basis beginselen van Quantum Computing tot de technische specificaties voor Interchange-indelingen.</span><span class="sxs-lookup"><span data-stu-id="331ad-109">The **conceptual documentation** consists of a set of articles that are published to https://docs.microsoft.com/quantum, and that describe everything from the basics of quantum computing to the technical specifications for interchange formats.</span></span> <span data-ttu-id="331ad-110">Deze artikelen worden geschreven in [DocFXe prijs verlaging (dfm)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), een afkortings variant die wordt gebruikt voor het maken van uitgebreide documentatie sets.</span><span class="sxs-lookup"><span data-stu-id="331ad-110">These articles are written in [DocFX-Flavored Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), a Markdown variant used for creating rich documentation sets.</span></span>
- <span data-ttu-id="331ad-111">De **API-verwijzing** is een set pagina's voor elke Q #-functie,-bewerking en door de gebruiker gedefinieerd type, gepubliceerd op https://docs.microsoft.com/qsharp/api/.</span><span class="sxs-lookup"><span data-stu-id="331ad-111">The **API reference** is a set of pages for each Q# function, operation, and user-defined type, published to https://docs.microsoft.com/qsharp/api/.</span></span> <span data-ttu-id="331ad-112">Deze pagina's documenteren de invoer en bewerkingen van elke aanroep, samen met voor beelden en koppelingen naar meer informatie.</span><span class="sxs-lookup"><span data-stu-id="331ad-112">These pages document the inputs and operations to each callable, along with examples and links to more information.</span></span> <span data-ttu-id="331ad-113">De API-verwijzing wordt automatisch geëxtraheerd uit kleine DFM-documenten in Q #-bron code als onderdeel van elke release.</span><span class="sxs-lookup"><span data-stu-id="331ad-113">The API reference is automatically extracted from small DFM documents in Q# source code as a part of each release.</span></span>
- <span data-ttu-id="331ad-114">De **Leesmij-bestanden<!---->. MD** die zijn opgenomen in elk voor beeld en Kata beschrijven hoe u dit voor beeld of Kata gebruikt, wat het dekt en hoe het werkt met de rest van de Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="331ad-114">The **README<!---->.md** files included with each sample and kata describe how to use that sample or kata is used, what it covers, and how it relates to the rest of the Quantum Development Kit.</span></span> <span data-ttu-id="331ad-115">Deze bestanden worden geschreven met behulp van github geringte [prijs verlaging (GFM)](https://github.github.com/gfm/), een licht gewicht alternatief voor dfm dat populair is voor het rechtstreeks koppelen van documentatie aan code opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="331ad-115">These files are written using [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/), a more lightweight alternative to DFM that's popular for attaching documentation directly to code repositories.</span></span>

## <a name="contributing-to-the-conceptual-documentation"></a><span data-ttu-id="331ad-116">Bijdragen aan de conceptuele documentatie</span><span class="sxs-lookup"><span data-stu-id="331ad-116">Contributing to the Conceptual Documentation</span></span>

<span data-ttu-id="331ad-117">Voor een verbetering van de conceptuele of leesmij-documentatie, begint met een pull-aanvraag op [**MicrosoftDocs/Quantum-docs-PR**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**micro soft/Quantum**](https://github.com/Microsoft/Quantum)of [**micro soft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas), zoals van toepassing.</span><span class="sxs-lookup"><span data-stu-id="331ad-117">To contribute an improvement to the conceptual or README documentation, then, starts with a pull request onto either [**MicrosoftDocs/quantum-docs-pr**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/Quantum**](https://github.com/Microsoft/Quantum), or [**Microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas), as is appropriate.</span></span>
<span data-ttu-id="331ad-118">Hieronder vindt u meer informatie over pull-aanvragen. er is nu een paar dingen die u in aanmerking kunt nemen bij het verbeteren van de documentatie:</span><span class="sxs-lookup"><span data-stu-id="331ad-118">We'll describe more about pull requests below, but for now there's a few things that are good to keep in mind as you improve documentation:</span></span>

- <span data-ttu-id="331ad-119">Lezers worden door de Quantum Development Kit-documentatie van een breed scala aan achtergronden geleverd.</span><span class="sxs-lookup"><span data-stu-id="331ad-119">Readers come to the Quantum Development Kit documentation from a very wide range of backgrounds.</span></span> <span data-ttu-id="331ad-120">Iedereen van hoge school studenten die meer willen weten over een nieuwe en interessante tenurede faculteit bij het uitvoeren van het gebruik van Quantum Computing, moeten in staat zijn om de documentatie te lezen.</span><span class="sxs-lookup"><span data-stu-id="331ad-120">Everyone from high school students looking to learn something new and exciting through to tenured faculty performing quantum computing research should be able to get something out of reading the documentation.</span></span> <span data-ttu-id="331ad-121">Als dat mogelijk is, neemt u geen uitgebreide kennis op over het deel van uw lezers, aangezien ze alleen kunnen worden gestart. Het is handig als u duidelijke en toegankelijke beschrijvingen kunt opgeven, of als u koppelingen naar andere bronnen kunt opgeven voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="331ad-121">To the extent that's possible, please don't assume extensive knowledge on the part of your readers, as they may just be starting out. It's most helpful if you can provide clear and accessible descriptions, or can provide links to other resources for more information.</span></span>
- <span data-ttu-id="331ad-122">Het is niet mogelijk om documentatie sets op te stellen als boeken of documenten, in die lezers die in de ' middle ' lijken te komen.</span><span class="sxs-lookup"><span data-stu-id="331ad-122">Documentation sets aren't laid out like books or papers, in that readers will arrive in what might seem like the "middle."</span></span> <span data-ttu-id="331ad-123">Zoek machines maken bijvoorbeeld mogelijk geen suggesties voor de index of ze hebben mogelijk een koppeling verzonden door een vriend om hen te helpen. Probeer uw lezer te helpen door altijd een duidelijke context te geven, samen met koppelingen waar dat van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="331ad-123">For example, search engines might not suggest the index, or they might have been sent a link by a friend trying to help them out. Try to help your reader by always providing a clear context, along with links where appropriate.</span></span>
- <span data-ttu-id="331ad-124">Sommige lezers vinden de meest nuttige samen vattingen en definities, terwijl andere lezers het meest geschikt zijn voor het extrapoleren van concrete voor beelden.</span><span class="sxs-lookup"><span data-stu-id="331ad-124">Some readers will find abstract statements and definitions most helpful, while other readers work best by extrapolating from concrete examples.</span></span> <span data-ttu-id="331ad-125">Door zowel het algemene als het specifieke voor beeld te bieden, kunnen beide lezers optimaal profiteren van Quantum programmering.</span><span class="sxs-lookup"><span data-stu-id="331ad-125">Providing both the general case and specific examples can help both readers get the most out of quantum programming.</span></span>
- <span data-ttu-id="331ad-126">Met name als u de code die wordt gedocumenteerd ook hebt geschreven, zijn de dingen mogelijk duidelijk voor uw lezers.</span><span class="sxs-lookup"><span data-stu-id="331ad-126">Especially if you also wrote the code being documented, things may be obvious to you that are not at all obvious to your reader.</span></span> <span data-ttu-id="331ad-127">Er is geen unieke beste manier om Program ma's aan te bieden, dus het is niet mogelijk om te zien welke ontwerp patronen u hebt gevonden en wat u het nuttigst vindt om uw ideeën in code uit te drukken.</span><span class="sxs-lookup"><span data-stu-id="331ad-127">There's no one unique best way to program, so no matter how clever or experienced a reader might be, they can't guess at what design patterns you found the most helpful to express your ideas in code.</span></span> <span data-ttu-id="331ad-128">Het is duidelijk om te zien hoe een lezer het gebruik van uw code kan verwachten door deze context te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="331ad-128">Being clear about how a reader can expect to make use of your code can help provide that context.</span></span>
- <span data-ttu-id="331ad-129">Veel leden van de Quantum-programmeer Community zijn academische onderzoekers en worden voornamelijk door middel van citaten voor hun bijdragen aan de Community herkend.</span><span class="sxs-lookup"><span data-stu-id="331ad-129">Many members of the quantum programming community are academic researchers, and are recognized mainly through citations for their contributions to the community.</span></span> <span data-ttu-id="331ad-130">U kunt niet alleen lezers helpen om aanvullende materialen te vinden, maar ook om academische uitvoer, zoals papers, besprekingen, blog berichten en software tools te vermelden, kunnen academische mede werkers helpen om de beste werkzaamheden te blijven uitvoeren om de community te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="331ad-130">In addition to helping readers find additional materials, making sure to properly cite academic outputs such as papers, talks, blog posts, and software tools can help academic contributors to keep doing their best work to improve the community.</span></span>
- <span data-ttu-id="331ad-131">De Quantum-programmeer Community is een brede en veelzijdige community.</span><span class="sxs-lookup"><span data-stu-id="331ad-131">The quantum programming community is a broad and wonderfully diverse community.</span></span> <span data-ttu-id="331ad-132">Het gebruik van geslachte promaakte in voor beelden van derden (bijvoorbeeld: "als een gebruiker..., hij...) kan worden gebruikt om uit te sluiten in plaats van op te nemen.</span><span class="sxs-lookup"><span data-stu-id="331ad-132">The use of gendered pronouns in third-person examples (e.g.: "if a user ..., he will ...") can work to exclude rather than include.</span></span> <span data-ttu-id="331ad-133">Het Cognizant van de namen van mensen in citaten en koppelingen, en van de juiste insluiting van niet-ASCII-tekens, kan de diversiteit van de Community opleveren door de leden van de Gemeenschap te laten zien.</span><span class="sxs-lookup"><span data-stu-id="331ad-133">Being cognizant of people's names in citations and links, and of the correct inclusion of non-ASCII characters can serve the diversity of the community by showing respect to its members.</span></span> <span data-ttu-id="331ad-134">Evenzo worden veel woorden in de Engelse taal vaak op een hatefule manier gebruikt, zodat het gebruik ervan in technische documentatie kan leiden tot beschadiging van zowel individuele lezers als de community.</span><span class="sxs-lookup"><span data-stu-id="331ad-134">Similarly, many words in the English language are often used in a hateful manner, such that their use in technical documentation can cause harm both to individual readers and to the community at large.</span></span>

### <a name="referencing-sample-code-from-conceptual-articles"></a><span data-ttu-id="331ad-135">Verwijzen naar voorbeeld code van conceptuele artikelen</span><span class="sxs-lookup"><span data-stu-id="331ad-135">Referencing Sample Code from Conceptual Articles</span></span>

<span data-ttu-id="331ad-136">Als u code wilt toevoegen uit de [opslag plaats voor beelden](https://github.com/Microsoft/Quantum), kunt u dit doen met behulp van een speciale DocFX-opdracht voor korting:</span><span class="sxs-lookup"><span data-stu-id="331ad-136">If you want to include code from the [samples repository](https://github.com/Microsoft/Quantum), you can do so using a special DocFX-Flavored Markdown command:</span></span>

```markdown
:::code language="qsharp" source="~/quantum/samples/algorithms/chsh-game/Game.qs" range="4-8":::
```

<span data-ttu-id="331ad-137">Met deze opdracht worden regels 4 tot en met 8 van het [`Game.qs` bestand geïmporteerd uit het `chsh-game`](https://github.com/microsoft/Quantum/blob/master/samples/algorithms/chsh-game/Game.qs)-voor beeld, waarbij ze worden gemarkeerd als Q #-code voor het markeren van syntaxis.</span><span class="sxs-lookup"><span data-stu-id="331ad-137">This command will import lines 4 to 8 of the [`Game.qs` file from the `chsh-game` sample](https://github.com/microsoft/Quantum/blob/master/samples/algorithms/chsh-game/Game.qs), marking them as Q# code for the purpose of syntax highlighting.</span></span>
<span data-ttu-id="331ad-138">Met deze opdracht kunt u voor komen dat code wordt gedupliceerd tussen conceptuele artikelen en de opslag plaats voor beelden, zodat voorbeeld code in de documentatie altijd zo actueel mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="331ad-138">Using this command, you can avoid duplicating code between conceptual articles and the samples repository, so that sample code in documentation is always as up to date as possible.</span></span>

## <a name="contributing-to-the-api-references"></a><span data-ttu-id="331ad-139">Bijdragen aan de API-verwijzingen</span><span class="sxs-lookup"><span data-stu-id="331ad-139">Contributing to the API References</span></span>

<span data-ttu-id="331ad-140">Om een verbetering van de API-verwijzingen bij te dragen, is het handig om een pull-aanvraag rechtstreeks te openen in de code die wordt gedocumenteerd.</span><span class="sxs-lookup"><span data-stu-id="331ad-140">To contribute an improvement to the API references, it's most helpful to open a pull request directly on the code being documented.</span></span>
<span data-ttu-id="331ad-141">Elke functie, bewerking of door de gebruiker gedefinieerd type ondersteunt een documentatie opmerking (aangeduid met `///` in plaats van `//`).</span><span class="sxs-lookup"><span data-stu-id="331ad-141">Each function, operation, or user-defined type supports a documentation comment (denoted with `///` instead of `//`).</span></span>
<span data-ttu-id="331ad-142">Wanneer we elke release van de Quantum Development Kit compileren, worden deze opmerkingen gebruikt voor het genereren van de API-verwijzing op https://docs.microsoft.com/qsharp/api/, met inbegrip van gegevens over de invoer van en uitvoer van elke aanroep bare, de veronderstellingen die elk aanroepbaar zijn, en voor beelden van het gebruik ervan.</span><span class="sxs-lookup"><span data-stu-id="331ad-142">When we compile each release of the Quantum Development Kit, these comments are used to generate the API reference at https://docs.microsoft.com/qsharp/api/, including details about the inputs to and outputs from each callable, the assumptions each callable makes, and examples of how to use them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="331ad-143">Zorg ervoor dat u de gegenereerde API-documentatie niet hand matig bewerkt, omdat deze bestanden worden overschreven door elke nieuwe release.</span><span class="sxs-lookup"><span data-stu-id="331ad-143">Please make sure to not manually edit the generated API documentation, as these files are overwritten with each new release.</span></span>
> <span data-ttu-id="331ad-144">We stellen uw bijdrage aan de community op prijs en willen er zeker van zijn dat uw wijzigingen blijven bijdragen aan de release van gebruikers na de release.</span><span class="sxs-lookup"><span data-stu-id="331ad-144">We value your contribution to the community, and want to make sure that your changes continue to help users release after release.</span></span>

<span data-ttu-id="331ad-145">Neem bijvoorbeeld de functie `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="331ad-145">For example, consider the function `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="331ad-146">Een documentatie opmerking moet een gebruiker helpen informatie te lezen over het interpreteren van `bits` en `oracle` en waarvoor de functie is.</span><span class="sxs-lookup"><span data-stu-id="331ad-146">A documentation comment should help a user learn how to interpret `bits` and `oracle` and what the function is for.</span></span>
<span data-ttu-id="331ad-147">Elk van deze verschillende informatie kan worden verstrekt aan de sectie Q # van een speciaal benoemde prijs opgave in de documentatie opmerking.</span><span class="sxs-lookup"><span data-stu-id="331ad-147">Each of these different pieces of information can be provided to the Q# compiler by a specially named Markdown section in the documentation comment.</span></span>
<span data-ttu-id="331ad-148">Voor het voor beeld van `ControlledOnBitString`kunnen we een van de volgende zaken schrijven:</span><span class="sxs-lookup"><span data-stu-id="331ad-148">For the example of `ControlledOnBitString`, we might write something like the following:</span></span>

```qsharp
 /// # Summary
 /// Returns a unitary operation that applies an oracle on the target register if the 
 /// control register state corresponds to a specified bit mask.
 ///
 /// # Description
 /// The output of this function is an operation that can be represented by a
 /// unitary transformation $U$ such that
 /// \begin{align}
 ///     U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes
 ///     \begin{cases}
 ///         V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\
 ///         \ket{\psi} & \textrm{otherwise}
 ///     \end{cases},
 /// \end{align}
 /// where $V$ is a unitary transformation that represents the action of the
 /// `oracle` operation.
 ///
 /// # Input
 /// ## bits
 /// The bit string to control the given unitary operation on.
 /// ## oracle
 /// The unitary operation to be applied on the target register.
 ///
 /// # Output
 /// A unitary operation that applies `oracle` on the target register if the control 
 /// register state corresponds to the bit mask `bits`.
 ///
 /// # Remarks
 /// The length of `bits` and `controlRegister` must be equal.
 ///
 /// Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function
 /// is an operation that performs the following steps:
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits`;
 /// * apply `Controlled oracle` to the control and target registers;
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits` again to return the control register to the original state.
 ///
 /// The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.
 ///
 /// # Example
 /// The following code snippets are equivalent:
 /// ```qsharp
 /// (ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
 /// ```
 /// and
 /// ```qsharp
 /// within {
 ///     ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
 /// } apply {
 ///     Controlled oracle(controlRegister, targetRegister);
 /// }
 /// ```
 ///
 /// The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:
 /// ```qsharp
 /// using (register = Qubit[2]) {
 ///     ApplyToEach(H, register);
 ///     (ControlledOnBitString([false], Z))(register[0..0], register[1]);
 /// }
 /// ```
 function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
 {
     return ControlledOnBitStringImpl(bits, oracle, _, _);
 }
```

<span data-ttu-id="331ad-149">U kunt de gerenderde versie van de bovenstaande code bekijken in de [API-documentatie voor de functie `ControlledOnBitString`](xref:microsoft.quantum.canon.controlledonbitstring).</span><span class="sxs-lookup"><span data-stu-id="331ad-149">You can see the rendered version of the code above in the [API documentation for the `ControlledOnBitString` function](xref:microsoft.quantum.canon.controlledonbitstring).</span></span>

<span data-ttu-id="331ad-150">Naast de algemene procedures voor het schrijven van documentatie, in het schrijven van API-documentatie opmerkingen, is het handig om een aantal zaken in acht te nemen:</span><span class="sxs-lookup"><span data-stu-id="331ad-150">In addition to the general practice of documentation writing, in writing API documentation comments it helps to keep a few things in mind:</span></span>

- <span data-ttu-id="331ad-151">De indeling van elke documentatie opmerking moet overeenkomen met wat de Q #-compiler verwacht dat uw documentatie correct wordt weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="331ad-151">The format of each documentation comment has to match what the Q# compiler expects for your documentation to appear correctly.</span></span> <span data-ttu-id="331ad-152">Sommige secties, zoals `/// # Remarks` toestaan voor vrije-vorm inhoud, terwijl secties zoals `/// # See Also` sectie meer beperkend zijn.</span><span class="sxs-lookup"><span data-stu-id="331ad-152">Some sections, such as `/// # Remarks` allow for freeform content, while sections such as `/// # See Also` section are more restrictive.</span></span>
- <span data-ttu-id="331ad-153">Een lezer kan uw API-documentatie lezen op de belangrijkste API-referentie site, op basis van de samen vatting van elke naam ruimte of zelfs vanuit de IDE door het gebruik van de aanwijs informatie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="331ad-153">A reader may read your API documentation on the main API reference site, on the summary for each namespace, or even from within their IDE through the use of hover information.</span></span> <span data-ttu-id="331ad-154">Als u er zeker van wilt zijn dat `/// # Summary` niet langer is dan een zin, kunt u met uw lezer snel zien of ze verder moeten worden gelezen of ergens anders moeten kijken en kunt u helpen bij het snel scannen van naam ruimte overzichten.</span><span class="sxs-lookup"><span data-stu-id="331ad-154">Making sure that `/// # Summary` isn't longer than about a sentence helps your reader quickly sort out whether they need to read further or look elsewhere, and can help in quickly scanning through namespace summaries.</span></span>
- <span data-ttu-id="331ad-155">Het is mogelijk dat uw documentatie veel langer is dan de code zelf, maar dat is wel goed.</span><span class="sxs-lookup"><span data-stu-id="331ad-155">Your documentation may well wind up being much longer than the code itself, but that's OK!</span></span> <span data-ttu-id="331ad-156">Zelfs een klein stukje code kan onverwachte gevolgen hebben voor gebruikers die niet weten in welke context de code zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="331ad-156">Even a small piece of code can have unexpected effects to users that don't know the context in which that code exists.</span></span> <span data-ttu-id="331ad-157">Door concrete voor beelden te bieden en duidelijke uitleg te geven, kunt u gebruikers helpen het beste gebruik te maken van de code die voor hen van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="331ad-157">By providing concrete examples and clear explanations, you can help users make the best use of the code that's available to them.</span></span>

<!-- ## LaTeX Formatting ##

**TODO** -->
