---
title: Pull-aanvragen openen
description: Meer informatie over hoe u een GitHub pull-aanvraag indient, wanneer u klaar bent voor het bijdragen aan code of documentatie voor de Microsoft Quantum Development Kit.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.pulls
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8e04e6502e0a6005dfdf0f93450bf3ffd5aaa672
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866924"
---
# <a name="opening-pull-requests"></a>Pull-aanvragen openen #

Alle documentatie voor de Quantum Development Kit wordt beheerd met behulp van het git-versie beheersysteem door gebruik te maken van verschillende opslag plaatsen die worden gehost op GitHub.
Door git en GitHub samen te gebruiken, kunt u eenvoudig samen werken in de Quantum Development Kit.
Met name elke Git-opslag plaats kan worden gekloond of gevorkeerd om een volledig onafhankelijke kopie van die opslag plaats te maken.
Zo kunt u aan uw bijdrage werken met de hulp middelen en de gewenste snelheid.

Wanneer u klaar bent, kunt u ons een aanvraag sturen om uw bijdrage op te nemen in onze opslag plaatsen, met behulp van de _pull-aanvraag_ functionaliteit van github.
De pagina voor elke pull-aanvraag bevat details over alle wijzigingen die bijdragen aan uw bijdrage, een lijst met opmerkingen over uw bijdrage en een aantal beoordelings hulpprogramma's die andere leden van de community kunnen gebruiken om feedback en advies te geven.

> [!NOTE]
> Hoewel een volledige zelf studie op Git zich buiten het bereik van deze hand leiding bevindt, kunnen we de volgende koppelingen voor meer informatie vinden over git:
>
> - [Meer informatie over git](https://www.atlassian.com/git): een set Git-zelf studies van atlassian.
> - [Versie beheer in Visual Studio code](https://code.visualstudio.com/docs/editor/versioncontrol): een hand leiding voor het gebruik van Visual Studio code als een gebruikers interface voor git.
> - [Github Learning Lab](https://lab.github.com/): een reeks online cursussen voor het gebruik van Git, github en verwante technologieën.
> - [Git visualiseren](https://git-school.github.io/visualizing-git/): een interactief hulp programma voor het visualiseren van de manier waarop Git-opdrachten de status van een opslag plaats wijzigen.
> - [Versie beheer met Git (EPQIS 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): een Git-zelf studie gericht op weten schappelijk computing.
> - [Meer informatie over git-vertakkingen](https://learngitbranching.js.org/): een interactieve set vertakkingen en het opnieuw baseren van puzzels om nieuwe Git-functies te leren kennen.

## <a name="what-is-a-pull-request"></a>Wat is een pull-aanvraag? ##

Als u het bovenstaande hebt gezegd, is het handig om even te weten wat een pull-aanvraag **is**.
Wanneer u werkt met git, worden alle wijzigingen weer gegeven als _door voeringen_ die beschrijven hoe deze wijzigingen zijn gerelateerd aan de status van de opslag plaats voordat deze worden gewijzigd.
We tekenen vaak diagrammen waarin de door voeringen worden getekend als cirkels met pijlen van eerdere door voeringen.

Stel dat u een bijdrage hebt gestart in een _vertakking_ met de naam `feature` .
Uw Fork van **micro soft/Quantum** kan er ongeveer als volgt uitzien:

![Een werk vertakking in GitHub](~/media/git-workflow-step0.png)

Als u uw wijzigingen in uw lokale opslag plaats aanbrengt, _kunt u_ wijzigingen aanbrengen van een andere opslag plaats in uw bedrijf om alle wijzigingen te ondervangen die zijn doorgevoerd.

![Het ophalen en samen voegen van wijzigingen vanuit een upstream-opslag plaats](~/media/git-workflow-step1.png)

Pull-aanvragen werken op dezelfde manier, maar in omgekeerde volg orde: wanneer u een pull-aanvraag opent, vraagt u de upstream-opslag plaats om uw bijdrage te halen in.

![Er wordt gevraagd om uw wijzigingen terug te halen naar de oorspronkelijke opslag plaats](~/media/git-workflow-step2.png)

Wanneer u een pull-aanvraag opent in een van onze opslag plaatsen, biedt GitHub een kans voor anderen in de community om een samen vatting van uw wijzigingen te bekijken, een opmerking hierover te nemen en suggesties te doen voor het maken van een nog betere bijdrage.

![Scherm opname van een pull-aanvraag in GitHub](~/media/pull-request-header.png)

Met dit proces kunnen we de GitHub-functionaliteit gebruiken om bijdragen te verbeteren en een product van hoge kwaliteit te onderhouden voor de Quantum-programmeer community.

## <a name="how-to-make-a-pull-request"></a>Een pull-aanvraag maken ##

Er zijn twee belang rijke manieren om een pull-aanvraag uit te voeren.  
Voor kleine wijzigingen die alleen van invloed zijn op één bestand, kan de GitHub-webinterface worden gebruikt om een pull-aanvraag volledig online te maken. Navigeer naar het bestand dat u wilt bewerken en gebruik het bewerkings pictogram.  
Voor complexere bijdragen is het vaak eenvoudiger om de opslag plaats te klonen op uw lokale computer om eerst een pull-aanvraag voor te bereiden.

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

## <a name="next-steps"></a>Volgende stappen ##

Gefeliciteerd met het gebruik van Git om de Quantum Development Kit-community te helpen.
Ga verder met de volgende gids voor meer informatie over het bijdragen aan code.

> [!div class="nextstepaction"]
> [Meer informatie over het bijdragen aan code](xref:microsoft.quantum.contributing.code)
