---
title: Kwantumbibliotheek voor machine learning
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 2/27/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.training
ms.openlocfilehash: f9b33a607a892179795d0700ba3080f9a24ab94a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275226"
---
# <a name="quantum-machine-learning-glossary"></a>Woorden lijst Quantum Machine Learning

De training van een circuit-georiënteerde Quantum classificeerder is een proces waarbij veel bewegende onderdelen zijn die dezelfde (of iets grotere) hoeveelheid kalibratie nodig hebben met een proef versie en fout als opleiding van traditionele classificaties. Hier worden de belangrijkste concepten en ingrediënten van dit trainings proces gedefinieerd.

## <a name="trainingtesting-schedules"></a>Planningen voor training en tests

In de context van een classificatie training wordt in een *planning* een subset van gegevens voorbeelden beschreven in een algemene training of testset. Een planning wordt meestal gedefinieerd als een verzameling van voor beelden van indices.

## <a name="parameterbias-scores"></a>Para meter/bias-scores

Op basis van een para meter voor de kandidaten en een classifier-afwijking wordt de *validatie Score* gemeten ten opzichte van een gekozen validatie schema en wordt aangegeven door een aantal onvolledige classificaties voor alle voor beelden in de planning S.

## <a name="hyperparameters"></a>Hyper parameters

Het model trainings proces is onderworpen aan bepaalde vooraf ingestelde waarden met de naam *Hyper parameters*:

### <a name="learning-rate"></a>Leersnelheid

Het is een van de Key Hyper parameters. Hiermee wordt gedefinieerd hoeveel huidige stochastische verlopen schatting van invloed is op de parameter update. De grootte van de Delta parameter update verschilt in verhouding tot het leer tempo. De waarden voor een kortere leer factor leiden tot tragere parameter ontwikkeling en langzamere convergentie, maar buitensporig grote waarden van LR kunnen de convergentie helemaal verstoren, omdat de verloop Daal nooit wordt doorgevoerd in een bepaald lokaal minimum. Hoewel het leer tempo op een zekere hoogte adaptief wordt aangepast door het trainings algoritme, is het belang rijk dat u een goede initiële waarde selecteert. Een gebruikelijke standaard waarde voor het leer tempo is 0,1. Het selecteren van de beste waarde voor het trainings tempo is een fijne illustratie (zie bijvoorbeeld sectie 4,3 van Goodfellow et al. ' diep leren ', MIT Press, 2017).

### <a name="minibatch-size"></a>Grootte van Minibatch

Hiermee definieert u hoeveel gegevens voorbeelden worden gebruikt voor één schatting van de stochastische kleur overgang. Grotere waarden van de grootte van minibatch leiden doorgaans tot robuustere en meer monotone convergentie, maar kunnen het trainings proces vertragen, omdat de kosten van een raming van één kleur overgang evenredig zijn met de minimatch grootte. Een gebruikelijke standaard waarde voor de grootte van de minibatch is 10.

### <a name="training-epochs-tolerance-gridlocks"></a>Trainings-epoches, tolerantie, gridlocks

' Epoche ' betekent één volledige Pass-Through de geplande trainings gegevens.
Het maximum aantal epochen per trainings thread (zie hieronder) moet worden afgelimiteerd. De trainings thread is gedefinieerd om te beëindigen (met de best bekende kandidaat-para meters) wanneer het maximum aantal epoches is uitgevoerd. Deze training zou echter eerder worden beëindigd wanneer het classificatie niveau voor het validatie schema lager is dan de gekozen tolerantie. Stel bijvoorbeeld dat de tolerantie van een onwaarschijnlijke classificatie 0,01 (1%) is. als op de validatieset van 2000-voor beelden wordt aangegeven dat er minder dan 20 misindelingen worden weer gegeven, is het tolerantie niveau bereikt. Een trainings thread wordt voor tijdig beëindigd als de validatie Score van het kandidaten model geen verbetering heeft vertoond ten opzichte van verschillende opeenvolgende epoches (een gridlock). De logica voor de gridlock-beëindiging is momenteel hardcoded.

### <a name="measurements-count"></a>Aantal metingen

Het schatten van de trainings-en validatie scores en de onderdelen van de stochastische kleur overgang op een Quantum apparaat bedragen voor het schatten van de Quantum status overlap pingen waarvoor meerdere metingen van de juiste observables zijn vereist. Het aantal metingen moet worden geschaald als $O (1/\ Epsilon ^ 2) $ waarbij $ \epsilon $ de gewenste schattings fout is.
Als vuist regel kan het aantal oorspronkelijke metingen ongeveer $1/\ mbox {tolerantie} ^ 2 $ zijn (Zie de definitie van tolerantie in de vorige alinea). Een voor waarde is dat het aantal metingen omhoog moet worden gewijzigd als de verloop Daal te schokkerig lijkt en de convergentie te moeilijk te verloopt.

### <a name="training-threads"></a>Trainings threads

De waarschijnlijke functie die het trainings hulpprogramma voor de classificatie is, is zeer zelden, wat inhoudt dat er meestal een groot aantal lokale optimaies is in de parameter ruimte die aanzienlijk kan variëren per kwaliteit. Omdat het SGD-proces kan convergeren naar slechts één specifiek optimaal, is het belang rijk om meerdere start parameter vectoren te verkennen. Een veelvoorkomende procedure in machine learning is om dergelijke begin vectoren wille keurig te initialiseren. De Q #-trainings-API accepteert een wille keurige matrix van dergelijke begin vectoren, maar de onderliggende code verkennen ze sequentieel. Op een computer met meerdere kernen of in feite is het raadzaam om verschillende aanroepen naar Q # trainings-API parallel uit te voeren met verschillende parameter initialisaties in de-aanroepen.

#### <a name="how-to-modify-the-hyperparameters"></a>De Hyper parameters wijzigen

De QML-bibliotheek is de beste manier om de Hyper parameters te wijzigen door de standaard waarden van de UDT te vervangen [`TrainingOptions`](xref:microsoft.quantum.machinelearning.trainingoptions) . Daarom noemen we het met de functie [`DefaultTrainingOptions`](xref:microsoft.quantum.machinelearning.defaulttrainingoptions) en past u de operator `w/` toe om de standaard waarden te overschrijven. Als u bijvoorbeeld 100.000-metingen en een leer tempo van 0,01 wilt gebruiken:
 ```qsharp
let options = DefaultTrainingOptions()
w/ LearningRate <- 0.01
w/ NMeasurements <- 100000;
 ```
