---
title: Pull-aanvragen openen
description: Meer informatie over hoe u een GitHub pull-aanvraag indient, wanneer u klaar bent voor het bijdragen aan code of documentatie voor de Microsoft Quantum Development Kit.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.pulls
ms.openlocfilehash: 82af3b5123588cc06882f746ffcb0402ad3f0f2e
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274543"
---
# <a name="opening-pull-requests"></a><span data-ttu-id="68254-103">Pull-aanvragen openen</span><span class="sxs-lookup"><span data-stu-id="68254-103">Opening Pull Requests</span></span> #

<span data-ttu-id="68254-104">Alle documentatie voor de Quantum Development Kit wordt beheerd met behulp van het git-versie beheersysteem door gebruik te maken van verschillende opslag plaatsen die worden gehost op GitHub.</span><span class="sxs-lookup"><span data-stu-id="68254-104">All of the documentation for the Quantum Development Kit is managed using the Git version control system through the use of several repositories hosted on GitHub.</span></span>
<span data-ttu-id="68254-105">Door git en GitHub samen te gebruiken, kunt u eenvoudig samen werken in de Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="68254-105">Using Git and GitHub together makes it easy to collaborate widely on the Quantum Development Kit.</span></span>
<span data-ttu-id="68254-106">Met name elke Git-opslag plaats kan worden gekloond of gevorkeerd om een volledig onafhankelijke kopie van die opslag plaats te maken.</span><span class="sxs-lookup"><span data-stu-id="68254-106">In particular, any Git repository can be cloned or forked to make a completely independent copy of that repository.</span></span>
<span data-ttu-id="68254-107">Zo kunt u aan uw bijdrage werken met de hulp middelen en de gewenste snelheid.</span><span class="sxs-lookup"><span data-stu-id="68254-107">This allows you to work on your contribution with the tools and at a pace that you prefer.</span></span>

<span data-ttu-id="68254-108">Wanneer u klaar bent, kunt u ons een aanvraag sturen om uw bijdrage op te nemen in onze opslag plaatsen, met behulp van de _pull-aanvraag_ functionaliteit van github.</span><span class="sxs-lookup"><span data-stu-id="68254-108">When you're ready, you can send us a request to include your contribution into our repos, using GitHub's _pull request_ functionality.</span></span>
<span data-ttu-id="68254-109">De pagina voor elke pull-aanvraag bevat details over alle wijzigingen die bijdragen aan uw bijdrage, een lijst met opmerkingen over uw bijdrage en een aantal beoordelings hulpprogramma's die andere leden van de community kunnen gebruiken om feedback en advies te geven.</span><span class="sxs-lookup"><span data-stu-id="68254-109">The page for each pull request includes details of all the changes that make your contribution, a list of comments on your contribution, and a set of review tools that other members of the community can use to provide feedback and advice.</span></span>

> [!NOTE]
> <span data-ttu-id="68254-110">Hoewel een volledige zelf studie op Git zich buiten het bereik van deze hand leiding bevindt, kunnen we de volgende koppelingen voor meer informatie vinden over git:</span><span class="sxs-lookup"><span data-stu-id="68254-110">While a full tutorial on Git is beyond the scope of this guide, we can suggest the following links for more resources on learning Git:</span></span>
>
> - <span data-ttu-id="68254-111">[Meer informatie over git](https://www.atlassian.com/git): een set Git-zelf studies van atlassian.</span><span class="sxs-lookup"><span data-stu-id="68254-111">[Learn Git](https://www.atlassian.com/git): A set of Git tutorials from Atlassian.</span></span>
> - <span data-ttu-id="68254-112">[Versie beheer in Visual Studio code](https://code.visualstudio.com/docs/editor/versioncontrol): een hand leiding voor het gebruik van Visual Studio code als een gebruikers interface voor git.</span><span class="sxs-lookup"><span data-stu-id="68254-112">[Version Control in Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol): A guide on how to use Visual Studio Code as a GUI for Git.</span></span>
> - <span data-ttu-id="68254-113">[Github Learning Lab](https://lab.github.com/): een reeks online cursussen voor het gebruik van Git, github en verwante technologieën.</span><span class="sxs-lookup"><span data-stu-id="68254-113">[GitHub Learning Lab](https://lab.github.com/): A set of online courses for using Git, GitHub, and related technologies.</span></span>
> - <span data-ttu-id="68254-114">[Git visualiseren](https://git-school.github.io/visualizing-git/): een interactief hulp programma voor het visualiseren van de manier waarop Git-opdrachten de status van een opslag plaats wijzigen.</span><span class="sxs-lookup"><span data-stu-id="68254-114">[Visualizing Git](https://git-school.github.io/visualizing-git/): An interactive tool for visualizing how Git commands change the state of a repository.</span></span>
> - <span data-ttu-id="68254-115">[Versie beheer met Git (EPQIS 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): een Git-zelf studie gericht op weten schappelijk computing.</span><span class="sxs-lookup"><span data-stu-id="68254-115">[Version Control with Git (EPQIS 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): A Git tutorial oriented towards scientific computing.</span></span>
> - <span data-ttu-id="68254-116">[Meer informatie over git-vertakkingen](https://learngitbranching.js.org/): een interactieve set vertakkingen en het opnieuw baseren van puzzels om nieuwe Git-functies te leren kennen.</span><span class="sxs-lookup"><span data-stu-id="68254-116">[Learn Git Branching](https://learngitbranching.js.org/): An interactive set of branching and rebasing puzzles to help learn new Git features.</span></span>

## <a name="what-is-a-pull-request"></a><span data-ttu-id="68254-117">Wat is een pull-aanvraag?</span><span class="sxs-lookup"><span data-stu-id="68254-117">What is a Pull Request?</span></span> ##

<span data-ttu-id="68254-118">Als u het bovenstaande hebt gezegd, is het handig om even te weten wat een pull-aanvraag **is**.</span><span class="sxs-lookup"><span data-stu-id="68254-118">Having said the above, it's helpful to take a few moments to say what a pull request **is**.</span></span>
<span data-ttu-id="68254-119">Wanneer u werkt met git, worden alle wijzigingen weer gegeven als _door voeringen_ die beschrijven hoe deze wijzigingen zijn gerelateerd aan de status van de opslag plaats voordat deze worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="68254-119">When working with Git, any changes are represented as _commits_ that describe how those changes are related to the state of the repository before those changes.</span></span>
<span data-ttu-id="68254-120">We tekenen vaak diagrammen waarin de door voeringen worden getekend als cirkels met pijlen van eerdere door voeringen.</span><span class="sxs-lookup"><span data-stu-id="68254-120">We'll often draw diagrams in which commits are drawn as circles with arrows from previous commits.</span></span>

<span data-ttu-id="68254-121">Stel dat u een bijdrage hebt gestart in een _vertakking_ met de naam `feature` .</span><span class="sxs-lookup"><span data-stu-id="68254-121">Suppose you have started a contribution in a _branch_ called `feature`.</span></span>
<span data-ttu-id="68254-122">Uw Fork van **micro soft/Quantum** kan er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="68254-122">Then your fork of **Microsoft/Quantum** might look something like this:</span></span>

![Een werk vertakking in GitHub](~/media/git-workflow-step0.png)

<span data-ttu-id="68254-124">Als u uw wijzigingen in uw lokale opslag plaats aanbrengt, _kunt u_ wijzigingen aanbrengen van een andere opslag plaats in uw bedrijf om alle wijzigingen te ondervangen die zijn doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="68254-124">If you make your changes in your local repository, you can _pull_ changes from another repository into yours to catch up to any changes that happened upstream.</span></span>

![Het ophalen en samen voegen van wijzigingen vanuit een upstream-opslag plaats](~/media/git-workflow-step1.png)

<span data-ttu-id="68254-126">Pull-aanvragen werken op dezelfde manier, maar in omgekeerde volg orde: wanneer u een pull-aanvraag opent, vraagt u de upstream-opslag plaats om uw bijdrage te halen in.</span><span class="sxs-lookup"><span data-stu-id="68254-126">Pull requests work the same way, but in reverse: when you open a pull request, you ask for the upstream repository to pull your contribution in.</span></span>

![Er wordt gevraagd om uw wijzigingen terug te halen naar de oorspronkelijke opslag plaats](~/media/git-workflow-step2.png)

<span data-ttu-id="68254-128">Wanneer u een pull-aanvraag opent in een van onze opslag plaatsen, biedt GitHub een kans voor anderen in de community om een samen vatting van uw wijzigingen te bekijken, een opmerking hierover te nemen en suggesties te doen voor het maken van een nog betere bijdrage.</span><span class="sxs-lookup"><span data-stu-id="68254-128">When you open a pull request to one of our repositories, GitHub will offer an opportunity for others in the community to see a summary of your changes, to comment on them, and to make suggestions for how to help make an even better contribution.</span></span>

![Scherm opname van een pull-aanvraag in GitHub](~/media/pull-request-header.png)

<span data-ttu-id="68254-130">Met dit proces kunnen we de GitHub-functionaliteit gebruiken om bijdragen te verbeteren en een product van hoge kwaliteit te onderhouden voor de Quantum-programmeer community.</span><span class="sxs-lookup"><span data-stu-id="68254-130">Using this process helps us use GitHub functionality to improve contributions and to maintain a high-quality product for the quantum programming community.</span></span>

## <a name="how-to-make-a-pull-request"></a><span data-ttu-id="68254-131">Een pull-aanvraag maken</span><span class="sxs-lookup"><span data-stu-id="68254-131">How to Make a Pull Request</span></span> ##

<span data-ttu-id="68254-132">Er zijn twee belang rijke manieren om een pull-aanvraag uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="68254-132">There are two main ways to make a pull request.</span></span>  
<span data-ttu-id="68254-133">Voor kleine wijzigingen die alleen van invloed zijn op één bestand, kan de GitHub-webinterface worden gebruikt om een pull-aanvraag volledig online te maken.</span><span class="sxs-lookup"><span data-stu-id="68254-133">For small changes that only affect a single file, the GitHub web interface can be used to make a pull request entirely online.</span></span> <span data-ttu-id="68254-134">Navigeer naar het bestand dat u wilt bewerken en gebruik het bewerkings pictogram.</span><span class="sxs-lookup"><span data-stu-id="68254-134">Simply navigate to the file you want to edit and use the edit icon.</span></span>  
<span data-ttu-id="68254-135">Voor complexere bijdragen is het vaak eenvoudiger om de opslag plaats te klonen op uw lokale computer om eerst een pull-aanvraag voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="68254-135">For more complicated contributions, it's most often easier to clone the repository to your local computer to prepare for a pull request first.</span></span>

<!--
### Using the Web Interface ###

**TODO**

### Command-Line and GitHub Flow ###

Most of the time, it's easier to prepare a pull request on your own computer; that makes it easier to work incrementally, and to test your changes.
If you haven't already done so, the first step is to _fork_ the repository that you'd like to contribute to.
Forking makes a complete clone of the original repository, but under your GitHub account instead of under [Microsoft](http://github.com/Microsoft/) or [MicrosoftDocs](http://github.com/MicrosoftDocs/).
This way, you can edit your personal fork to your heart's content before making a pull request for your work.

**TODO: pick up here**

## Code Review and Etiquette ##

**TODO: PR ettiquette, reviews, etc.**

-->

## <a name="next-steps"></a><span data-ttu-id="68254-136">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="68254-136">Next steps</span></span> ##

<span data-ttu-id="68254-137">Gefeliciteerd met het gebruik van Git om de Quantum Development Kit-community te helpen.</span><span class="sxs-lookup"><span data-stu-id="68254-137">Congratulations on using Git to help out the Quantum Development Kit community!</span></span>
<span data-ttu-id="68254-138">Ga verder met de volgende gids voor meer informatie over het bijdragen aan code.</span><span class="sxs-lookup"><span data-stu-id="68254-138">To learn more about how to contribute code, please continue with the following guide.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="68254-139">Meer informatie over het bijdragen aan code</span><span class="sxs-lookup"><span data-stu-id="68254-139">Learn how to contribute code</span></span>](xref:microsoft.quantum.contributing.code)