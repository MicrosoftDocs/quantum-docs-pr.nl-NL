---
title: Code bijdragen aan de micro soft-QDK
description: Meer informatie over het bijdragen van voorbeeld-en bibliotheek code aan de Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: contributor-guide
uid: microsoft.quantum.contributing.code
no-loc:
- Q#
- $$v
ms.openlocfilehash: 54ef15db2b850e6a3bff38945c57129361517bfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856680"
---
# <a name="contributing-code"></a><span data-ttu-id="1d09f-103">Code bijdragen</span><span class="sxs-lookup"><span data-stu-id="1d09f-103">Contributing Code</span></span>

<span data-ttu-id="1d09f-104">Naast het melden van problemen en het verbeteren van documentatie, kan bijdragen aan code in de Quantum Development Kit een zeer directe manier zijn om uw collega's in de Quantum-programmeer community te helpen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-104">In addition to reporting issues and improving documentation, contributing code to the Quantum Development Kit can be a very direct way to help your peers in the quantum programming community.</span></span>
<span data-ttu-id="1d09f-105">Door code te leveren, kunt u problemen oplossen, nieuwe voor beelden bieden, bestaande bibliotheken eenvoudiger te gebruiken of zelfs volledig nieuwe functies toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-105">By contributing code, you can help to fix issues, provide new examples, make existing libraries easier to use, or even add entirely new features.</span></span>

<span data-ttu-id="1d09f-106">In deze hand leiding wordt een overzicht gegeven van wat er wordt gezocht wanneer we pull-aanvragen bekijken om uw bijdrage te helpen het meest geschikt te maken.</span><span class="sxs-lookup"><span data-stu-id="1d09f-106">In this guide, we'll detail a bit of what we look for when we review pull requests to help your contribution do the most good.</span></span>

## <a name="what-we-look-for"></a><span data-ttu-id="1d09f-107">Wat we zoeken</span><span class="sxs-lookup"><span data-stu-id="1d09f-107">What We Look For</span></span>

<span data-ttu-id="1d09f-108">Een ideale code bijdrage bouwt voort op de bestaande werkzaamheden in een Quantum Development Kit-opslag plaats om problemen op te lossen, bestaande functies uit te breiden of nieuwe functies toe te voegen die binnen het bereik van een opslag plaats vallen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-108">An ideal code contribution builds on the existing work in a Quantum Development Kit repository to fix issues, expand existing features, or to add new features that are within the scope of a repository.</span></span>
<span data-ttu-id="1d09f-109">Wanneer we een code bijdrage accepteren, wordt het een deel van de Quantum Development Kit zelf, zodat nieuwe functies worden vrijgegeven, onderhouden en ontwikkeld op dezelfde manier als de rest van de Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="1d09f-109">When we accept a code contribution, it becomes a part of the Quantum Development Kit itself, such that new features will be released, maintained, and developed in the same way as the rest of the Quantum Development Kit.</span></span>
<span data-ttu-id="1d09f-110">Het is dus handig wanneer de functionaliteit die door een bijdrage wordt toegevoegd, goed is getest en is gedocumenteerd.</span><span class="sxs-lookup"><span data-stu-id="1d09f-110">Thus, it is helpful when functionality added by a contribution is well-tested and is documented.</span></span>

### <a name="unit-tests"></a><span data-ttu-id="1d09f-111">Eenheids tests</span><span class="sxs-lookup"><span data-stu-id="1d09f-111">Unit Tests</span></span>

<span data-ttu-id="1d09f-112">De Q# functies, bewerkingen en door de gebruiker gedefinieerde typen die bibliotheken vormen zoals de Canon, worden automatisch getest als onderdeel van de ontwikkeling van de [**micro soft/QuantumLibraries-**](https://github.com/Microsoft/QuantumLibraries/) opslag plaats.</span><span class="sxs-lookup"><span data-stu-id="1d09f-112">The Q# functions, operations, and user-defined types that make up libraries such as the canon are automatically tested as a part of development on the [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) repository.</span></span>
<span data-ttu-id="1d09f-113">Wanneer er een nieuwe pull-aanvraag wordt geopend, bijvoorbeeld de configuratie van [Azure-pijp lijnen](https://azure.microsoft.com/services/devops/pipelines/) , wordt gecontroleerd of de wijzigingen in de pull-aanvraag geen invloed hebben op de bestaande functionaliteit waarvan de Quantum-programmeer Community afhankelijk is.</span><span class="sxs-lookup"><span data-stu-id="1d09f-113">When a new pull request is opened, for instance, our [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) configuration will check that the changes in the pull request do not break any existing functionality that the quantum programming community depends on.</span></span>

<span data-ttu-id="1d09f-114">Met de nieuwste Q# versie worden eenheids tests gedefinieerd met behulp van het- `@Test("QuantumSimulator")` kenmerk.</span><span class="sxs-lookup"><span data-stu-id="1d09f-114">With the latest Q# version, unit tests are defined using the `@Test("QuantumSimulator")` attribute.</span></span> <span data-ttu-id="1d09f-115">Het argument kan ' QuantumSimulator ', ' ToffoliSimulator ', ' TraceSimulator ' zijn of een volledig gekwalificeerde naam die het doel van de uitvoering aangeeft.</span><span class="sxs-lookup"><span data-stu-id="1d09f-115">The argument may be either "QuantumSimulator", "ToffoliSimulator", "TraceSimulator", or any fully qualified name specifying the run target.</span></span> <span data-ttu-id="1d09f-116">Verschillende kenmerken die verschillende uitvoerings doelen definiëren, kunnen worden gekoppeld aan dezelfde aanroepable.</span><span class="sxs-lookup"><span data-stu-id="1d09f-116">Several attributes defining different run targets may be attached to the same callable.</span></span> <span data-ttu-id="1d09f-117">Sommige van onze tests maken nog steeds gebruik van het afgeschafte [micro soft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) -pakket dat alle Q# functies en bewerkingen bevat die eindigen op `Test` het [xUnit](https://xunit.github.io/) -Framework.</span><span class="sxs-lookup"><span data-stu-id="1d09f-117">Some of our tests still use the deprecated [Microsoft.Quantum.Xunit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) package that exposes all Q# functions and operations ending in `Test` to the [xUnit](https://xunit.github.io/) framework.</span></span> <span data-ttu-id="1d09f-118">Dit pakket is niet meer nodig om de eenheids tests te definiëren.</span><span class="sxs-lookup"><span data-stu-id="1d09f-118">This package is no longer needed for defining unit tests.</span></span> 

<span data-ttu-id="1d09f-119">De volgende functie wordt gebruikt om ervoor te zorgen dat de <xref:Microsoft.Quantum.Canon.Fst> en- <xref:Microsoft.Quantum.Canon.Snd> functies de juiste uitvoer in een representatief voor beeld retour neren.</span><span class="sxs-lookup"><span data-stu-id="1d09f-119">The following function is used to ensure that the <xref:Microsoft.Quantum.Canon.Fst> and <xref:Microsoft.Quantum.Canon.Snd> functions both return the right outputs in a representative example.</span></span>
<span data-ttu-id="1d09f-120">Als de uitvoer van `Fst` of `Snd` onjuist is, `fail` wordt de instructie gebruikt om te zorgen dat de test mislukt.</span><span class="sxs-lookup"><span data-stu-id="1d09f-120">If the output of `Fst` or `Snd` is incorrect, the `fail` statement is used to cause the test to fail.</span></span>

```qsharp
@Test("QuantumSimulator")
function PairTest () : Unit {
    let pair = (12, PauliZ);

    if (Fst(pair) != 12) {
        let actual = Fst(pair);
        fail $"Expected 12, actual {actual}.";
    }

    if (Snd(pair) != PauliZ) {
        let actual = Snd(pair);
        fail $"Expected PauliZ, actual {actual}.";
    }
}
```

<span data-ttu-id="1d09f-121">Complexere voor waarden kunnen worden gecontroleerd met behulp van de technieken in het [gedeelte testen](xref:microsoft.quantum.libraries.diagnostics) van de hand leiding standaard bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="1d09f-121">More complicated conditions can be checked using the techniques in the [testing section](xref:microsoft.quantum.libraries.diagnostics) of the standard libraries guide.</span></span>
<span data-ttu-id="1d09f-122">De volgende test controleert bijvoorbeeld of de `H(q); X(q); H(q);` naam wordt aangeroepen door <xref:Microsoft.Quantum.Canon.ApplyWith> `Z(q)` .</span><span class="sxs-lookup"><span data-stu-id="1d09f-122">For instance, the following test checks that `H(q); X(q); H(q);` as called by <xref:Microsoft.Quantum.Canon.ApplyWith> does the same thing as `Z(q)`.</span></span>

```qsharp
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

<span data-ttu-id="1d09f-123">Bij het toevoegen van nieuwe functies is het een goed idee om ook nieuwe tests toe te voegen, zodat u zeker weet dat uw bijdrage de bedoeling is.</span><span class="sxs-lookup"><span data-stu-id="1d09f-123">When adding new features, it's a good idea to also add new tests to make sure that your contribution does what it's supposed to.</span></span>
<span data-ttu-id="1d09f-124">Dit helpt de rest van de community om uw functie te onderhouden en te ontwikkelen, met name om andere ontwikkel aars te helpen weten dat ze op uw functie kunnen vertrouwen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-124">This helps the rest of the community to maintain and develop your feature, and in particular helps other developers know that they can rely on your feature.</span></span>

> [!NOTE]
> <span data-ttu-id="1d09f-125">Dit werkt op de andere manier.</span><span class="sxs-lookup"><span data-stu-id="1d09f-125">This works the other way around, too!</span></span>
> <span data-ttu-id="1d09f-126">Als er sprake is van een bestaande functie waarvoor bepaalde tests ontbreken, helpt we bij het toevoegen van test dekking een uitstekende bijdrage aan de community.</span><span class="sxs-lookup"><span data-stu-id="1d09f-126">If there's an existing feature that's missing some tests, helping us add test coverage would make a great contribution to the community.</span></span>

<span data-ttu-id="1d09f-127">Lokale tests kunnen worden uitgevoerd met Visual Studio test Explorer of de `dotnet test` opdracht, zodat u uw bijdrage kunt controleren voordat u een pull-aanvraag opent.</span><span class="sxs-lookup"><span data-stu-id="1d09f-127">Locally, unit tests can be run using the Visual Studio Test Explorer or the `dotnet test` command, so that you can check your contribution before opening up a pull request.</span></span>

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->

## <a name="pull-requests"></a><span data-ttu-id="1d09f-128">Pull-aanvragen</span><span class="sxs-lookup"><span data-stu-id="1d09f-128">Pull Requests</span></span>

<span data-ttu-id="1d09f-129">Wanneer u klaar bent om uw werk bij te dragen, verzendt u een pull-aanvraag via GitHub naar de bijbehorende opslag plaats.</span><span class="sxs-lookup"><span data-stu-id="1d09f-129">When you are ready to contribute your work, please send a Pull Request via GitHub to the corresponding repository.</span></span>
<span data-ttu-id="1d09f-130">Het team zal controleren en feedback geven.</span><span class="sxs-lookup"><span data-stu-id="1d09f-130">The team will review and provide feedback.</span></span> <span data-ttu-id="1d09f-131">Alle opmerkingen moeten worden beantwoord en opgelost en alle controles moeten worden door gegeven voordat de code wordt samengevoegd met de `main` vertakking.</span><span class="sxs-lookup"><span data-stu-id="1d09f-131">All comments need to be answered and resolved and all checks need to pass before the code is merged to the `main` branch.</span></span>

## <a name="when-well-reject-a-pull-request"></a><span data-ttu-id="1d09f-132">Wanneer we een pull-aanvraag afwijzen</span><span class="sxs-lookup"><span data-stu-id="1d09f-132">When We'll Reject a Pull Request</span></span>

<span data-ttu-id="1d09f-133">Soms wordt de pull-aanvraag voor een bijdrage geweigerd.</span><span class="sxs-lookup"><span data-stu-id="1d09f-133">Sometimes, we'll reject the pull request for a contribution.</span></span>
<span data-ttu-id="1d09f-134">Als dit het geval is, betekent dit niet dat het defect is, omdat er een aantal redenen zijn waarom we een bepaalde bijdrage mogelijk niet kunnen accepteren.</span><span class="sxs-lookup"><span data-stu-id="1d09f-134">If this happens to you, it doesn't mean that it's bad, as there's a number of reasons why we might not be able to accept a particular contribution.</span></span>
<span data-ttu-id="1d09f-135">Mogelijk is een bijdrage aan de Quantum-programmeer Community heel goed, maar de Quantum Development Kit-opslag plaatsen zijn niet de juiste plaats om deze te ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-135">Perhaps most commonly, a contribution to the quantum programming community is a really good one, but the Quantum Development Kit repositories aren't the right place to develop it.</span></span>
<span data-ttu-id="1d09f-136">In dergelijke gevallen kunt u het beste uw eigen opslag plaats---deel van de kracht van de Quantum Development Kit maken, waarmee u eenvoudig uw eigen bibliotheken kunt maken en distribueren met behulp van GitHub en NuGet.org, op dezelfde manier als u de Canon-en chemie-bibliotheken vandaag nog distribueert.</span><span class="sxs-lookup"><span data-stu-id="1d09f-136">In such cases, we strongly encourage you to make your own repository --- part of the strength of the Quantum Development Kit is that it's easy to make and distribute your own libraries using GitHub and NuGet.org, the same way that we distribute the canon and chemistry libraries today.</span></span>

<span data-ttu-id="1d09f-137">Op andere momenten kunnen we een goede bijdrage afwijzen, omdat we nog niet klaar zijn om deze te onderhouden en te ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-137">At other times, we may reject a good contribution simply because we aren't yet ready to maintain and develop it.</span></span>
<span data-ttu-id="1d09f-138">Het kan lastig zijn om alles te doen, dus we plannen welke functies u het beste kunt gebruiken als een route kaart.</span><span class="sxs-lookup"><span data-stu-id="1d09f-138">It can be difficult to do everything, so we plan out what features we're best able to work on as a roadmap.</span></span>
<span data-ttu-id="1d09f-139">Dit kan een andere situatie zijn waarbij het loslaten van een functie als een bibliotheek van derden een hoop idee kan maken.</span><span class="sxs-lookup"><span data-stu-id="1d09f-139">This can be another case where releasing a feature as a third-party library can make a lot of sense.</span></span>
<span data-ttu-id="1d09f-140">Het is ook mogelijk om uw hulp te vragen bij het wijzigen van een functie zodat deze beter past in onze route kaart, zodat we het beste werk kunnen doen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-140">Alternatively, we may ask for your help in modifying a feature to better fit into our roadmap so that we can do the best work we can with it.</span></span>

<span data-ttu-id="1d09f-141">We vragen u ook om wijzigingen in een pull-aanvraag als er meer documentatie of eenheids tests nodig zijn om ons te helpen hun gebruik te maken, of als het verschilt van de stijl van de rest van de Q# bibliotheken waardoor het voor gebruikers moeilijker wordt om uw functie te vinden.</span><span class="sxs-lookup"><span data-stu-id="1d09f-141">We'll also ask for changes to a pull request if it requires more documentation or unit tests to help us make use of it, or if it differs enough in style from the rest of the Q# libraries that it will make it harder for users to find your feature.</span></span>
<span data-ttu-id="1d09f-142">In deze gevallen proberen we een aantal adviezen te geven over wat er kan worden toegevoegd of gewijzigd om uw bijdrage voor ons gemakkelijker te maken.</span><span class="sxs-lookup"><span data-stu-id="1d09f-142">In these cases, we'll try to offer some advice in code reviews about what can be added or changed to make your contribution easier for us to include.</span></span>

<span data-ttu-id="1d09f-143">Ten slotte kunnen we geen bijdragen accepteren die schade aanrichten aan de quantum computer Community, zoals beschreven in de [micro soft open source-gedrags code](https://opensource.microsoft.com/codeofconduct/).</span><span class="sxs-lookup"><span data-stu-id="1d09f-143">Finally, we cannot accept contributions that cause harm the quantum computing community, as outlined in the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="1d09f-144">We willen er zeker van zijn dat de bijdragen van toepassing zijn op de volledige quantum computer-Community, zowel in de huidige fantastische diversiteit als in de toekomst, naarmate deze nog steeds groter wordt.</span><span class="sxs-lookup"><span data-stu-id="1d09f-144">We want to ensure that contributions serve the entire quantum computing community, both in its current wonderful diversity, and in the future as it grows to become still more inclusive.</span></span>
<span data-ttu-id="1d09f-145">Bedankt voor uw hulp bij het realiseren van dit doel.</span><span class="sxs-lookup"><span data-stu-id="1d09f-145">We appreciate your help in realizing this goal.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1d09f-146">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="1d09f-146">Next steps</span></span>

<span data-ttu-id="1d09f-147">Hartelijk dank dat u de Quantum Development Kit een fantastische resource wilt maken voor de hele Quantum-programmeer community.</span><span class="sxs-lookup"><span data-stu-id="1d09f-147">Thanks for helping to make the Quantum Development Kit a great resource for the entire quantum programming community!</span></span>
<span data-ttu-id="1d09f-148">Ga voor meer informatie naar de volgende hand leiding voor Q# stijl.</span><span class="sxs-lookup"><span data-stu-id="1d09f-148">To learn more, please continue with the following guide on Q# style.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="1d09f-149">Meer informatie over Q# stijl richtlijnen</span><span class="sxs-lookup"><span data-stu-id="1d09f-149">Learn about Q# style guidelines</span></span>](xref:microsoft.quantum.contributing.style)

<span data-ttu-id="1d09f-150">Afhankelijk van wat voor soort code u bijdraagt, zijn er mogelijk extra zaken die u kunnen helpen om uw bijdrage zo goed mogelijk voor de community te laten doen.</span><span class="sxs-lookup"><span data-stu-id="1d09f-150">Depending on what kind of code you're contributing, there may be additional things to keep in mind that can help you make your contribution do as much good for the community as possible.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="1d09f-151">Meer informatie over bijdragende voor beelden</span><span class="sxs-lookup"><span data-stu-id="1d09f-151">Learn about contributing samples</span></span>](xref:microsoft.quantum.contributing.samples)
