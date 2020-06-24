---
title: Kwantumbibliotheek voor machine learning
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 11/22/2019
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.introduction
ms.openlocfilehash: 4c42612fee3a58e15368677bb2c77a70c5680f45
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275210"
---
# <a name="introduction-to-quantum-machine-learning"></a>Inleiding tot Quantum Machine Learning

## <a name="framework-and-goals"></a>Framework en doel stellingen

De Quantum encoding en verwerking van informatie is een krachtig alternatief voor klassieke machine learning Quantum-classificaties, met name het coderen van gegevens in Quantum registers die beknopt zijn ten opzichte van het aantal functies, waardoor de Quantum Entanglement als reken kundige resource wordt uitgevoerd en de quantum meting voor klasse-demijnen wordt uitgevoerd.
Circuit Center Quantum-classificatie is een relatief eenvoudige Quantum oplossing die gegevens codering combineert met een snel entangling/Disentangling Quantum circuit, gevolgd door meting om klassen labels van gegevens voorbeelden af te leiden.
Het doel is om te zorgen voor klassieke karakte Rise ring en opslag van subject-circuits, evenals hybride quantum/klassieke training van de para meters van de circuits, zelfs voor extreem grote functie ruimten.

## <a name="classifier-architecture"></a>Classificatie architectuur

Classificatie is een machine learning taak onder Super visie, waarbij het doel heeft om klassen labels $ \{ y_1, y_2, \ldots, y_d \} $ van bepaalde gegevens voorbeelden af te leiden. De ' training gegevensset ' is een verzameling van voor beelden $ \mathcal{D} = \{ (x, y)} $ met bekende vooraf toegewezen labels. Hier $x $ een gegevens voorbeeld is en $y $ is het bekend label met de naam training label.
Wat lijkt op traditionele methoden, de Quantum classificatie bestaat uit drie stappen:
- gegevens codering
- voor bereiding van een classificatie status
- meting als gevolg van de Probabilistic aard van de meting, moeten deze drie stappen meerdere keren worden herhaald. De meting kan worden gezien als een Quantum equivalent van niet-lineaire activering.
De code ring en het berekenen van de classificatie status worden uitgevoerd door middel van *Quantum circuits*. Terwijl het coderings circuit meestal gegevensgestuurd en zonder para meters is, bevat het classificatie circuit een voldoende set leer bare para meters. 

In de voorgestelde oplossing is het Classifier-circuit samengesteld uit single-Qubit rotaties en twee Qubit bestuurde rotaties. De para meters die hier kunnen worden beschreven, zijn de draai hoek. De rotatie-en beheerde rotatie poorten zijn bekend als *universeel* voor Quantum berekeningen, wat betekent dat elke matrix van unitary Weight kan worden opgesplitst in een lang genoeg circuit dat uit dergelijke Gates bestaat.

![Gecentreerde classificatie met meerdere lagen Perceptron versus circuit](~/media/DLvsQCC.png)

We kunnen dit model vergelijken met een Perceptron met meerdere lagen om een beter inzicht te krijgen in de basis structuur. In de Perceptron wordt de Voorspellings $p (y | x, \theta) $ parametrized door de set gewichten $ \theta $ waarmee de lineaire functies worden bepaald waarmee de niet-lineaire activerings functies worden verbonden (neurons). Deze para meters kunnen worden getraind om het model te maken. In de uitvoer slaag kan de kans van een voor beeld dat tot een klasse behoort, worden verkregen door gebruik te maken van niet-lineaire activerings functies, zoals Softmax. In de classificatie van het circuit Center is de voor spelling parametrized door de draai hoek van de door de Qubit beheerde rotaties van het model circuit. Op een vergelijk bare manier kunnen die para meters worden getraind met een hybride quantum/klassieke versie van het Daal-algoritme voor de kleur overgang. Voor het berekenen van de uitvoer, in plaats van het gebruik van niet-lineaire activerings functies, wordt de waarschijnlijkheid van de klasse verkregen door herhaalde metingen te lezen over een specifieke Qubit na de beheerde rotaties. Als u de klassieke gegevens in een Quantum status wilt coderen, gebruiken we een instelbaar coderings circuit voor status voorbereiding.

Onze architectuur verkent relatief recente circuits, die daarom snel moeten worden *entangling* om alle correlaties tussen de gegevens functies in alle bereiken vast te leggen. Hieronder ziet u een voor beeld van het handigste snelle entangling-circuit onderdeel. Hoewel een circuit met deze geometrie uit slechts $3 n + 1 $ Gates bestaat, zorgt de unitary-matrix van het gewicht dat deze reken kundige invloed heeft op een aanzienlijke Kruis communicatie tussen $2 ^ n $-functies.

![Snel entangling Quantum circuit op 5 qubits (met twee cyclische lagen).](~/media/5-qubit-qccc.png)

Het circuit in het bovenstaande voor beeld bestaat uit 6 single-Qubit Gates (G_1, \ldots, G_5; G_ {16} ) $ en 10 2-qubits Gates $ (G_6, \ldots, G_ {15} ) $. Ervan uitgaande dat elk van de poorten is gedefinieerd met één para meter die kan worden leren, hebben we 16 para meters die kunnen worden leren, terwijl de dimensie van de 5-Qubit Hilbert-ruimte 32 is. Een dergelijk circuit geometrie kan eenvoudig worden gegeneraliseerd tot een $n $-Qubit-REGI ster, wanneer $n $ oneven is, circuits met $3 n + 1 $ para meters voor $2 ^ n $-dimensionale functie ruimte.

## <a name="classifier-training-as-a-supervised-learning-task"></a>Geclassificeerde training als een gesuperd leer taak

De training van een classificatie model omvat het vinden van optimale waarden van de operationele para meters, zodat deze de gemiddelde waarschijnlijkheid van het uitstellen van de juiste opleidings labels in de trainings voorbeelden maximaliseren.
Hier hebben we zelf met alleen classificatie op twee niveaus, d.w.z. het geval van $d = $2 en slechts twee klassen met de labels $y _1, y_2 $.

> [!NOTE]
> Een methode om onze methoden te generaliseren voor een wille keurig aantal klassen is het vervangen van qubits met qudits, dat wil zeggen Quantum eenheden met $d $ basis Staten en de tweerichtings meting met $d $-Way meting.

### <a name="likelihood-as-the-training-goal"></a>Waarschijnlijkheid als het trainings doel

Gezien een lees bare Quantum circuit $U (\theta) $, waarbij $ \theta $ een vector van para meters is, en het identificeren van de uiteindelijke meting door $M $, is de gemiddelde kans op het juiste label degelijkheid $ $ \begin{align} \mathcal{L} (\theta) = \frac {1} {| \mathcal{D} |} \left (\ sum_ {(x, y_1) \In\mathcal{D}} P (M = y_1 | U (\theta) x) + \ sum_ {(x, y_2) \in\mathcal{D}} P (M = y_2 | U (\theta) x) \right) \end{align} $ $ waarbij $P (M = y | z) $ de kans is dat $y $ in de Quantum status $z $ wordt gemeten.
Hier is het goed om te begrijpen dat de waarschijnlijke functie $ \mathcal{L} (\theta) $ soepel is in $ \theta $ en de afgeleide in een $ \ theta_j $ kan worden berekend met behulp van het gebruikte Quantum protocol dat wordt gebruikt voor het berekenen van de waarschijnlijke functie. Hierdoor kunt u de $ \mathcal{L} (\theta) $ per verloop Daal optimaliseren.

### <a name="classifier-bias-and-training-score"></a>Classificatie afwijking en trainings Score

Gezien sommige tussenliggende (of laatste) waarden van de para meters in $ \theta $, moeten we een enkele reële waarde identificeren $b $ weet als *Classifier-afwijking* om de deinterferentie uit te voeren. De regel voor het afwijzen van labels werkt als volgt: 
- Een voor beeld $x $ is toegewezen label $y _2 $ if en alleen als $P (M = y_2 | U (\theta) x) + b > $0,5 (FIREWALLREGEL1) (anders is het label toegewezen $y _1 $)

Een duidelijk $b $ moet in het interval $ (-0,5, + 0,5) $ liggen om betekenisvol te zijn.

Een trainings case $ (x, y) \in \mathcal{D} $ wordt beschouwd als een onechte *classificatie* , gezien de bias $b $ als het label dat is uitgesteld voor $x $ zoals per firewallregel1 een andere naam heeft dan $y $. Het totale aantal misclassificaties is de *trainings Score* van de classificatie, gezien de bias $b $. De *optimale* Classifier-afwijking $b $ minimaliseert de trainings Score. Het is eenvoudig te zien dat, gezien de vooraf berekende waarschijnlijke schattingen $ \{ P (M = y_2 | U (\theta) x) | (x, *) \in\mathcal{D} \} $, de optimale classificatie afwijking kan worden gevonden door binaire zoek opdracht in interval $ (-0,5, + 0,5) $ door Maxi maal $ \ log_2 te maken (| \mathcal{D} |) $ stappen.

### <a name="reference"></a>Naslaginformatie

Deze informatie moet voldoende zijn om met de code te kunnen spelen. Als u echter meer wilt weten over dit model, leest u het oorspronkelijke voor stel: [ *' circuit-georiënteerde Quantum classificaties ', Maria schuld, Alex Bocharov, Krysta Svore en Nathan Wiebe*](https://arxiv.org/abs/1804.00633)
