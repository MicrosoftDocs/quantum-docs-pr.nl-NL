---
title: 'Q # API-ontwerp principes'
description: 'Q # API-ontwerp principes'
author: cgranade
ms.author: chgranad
ms.date: 3/9/2020
ms.topic: article
uid: microsoft.quantum.contributing.api-design
ms.openlocfilehash: a8e830e8f46ac6bd53ed5c607ca8cc2897721a20
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82687345"
---
# <a name="q-api-design-principles"></a>Q # API-ontwerp principes

## <a name="introduction"></a>Inleiding

Als taal en als platform biedt Q # gebruikers de mogelijkheid om Quantum toepassingen te schrijven, uit te voeren, te begrijpen en te verkennen.
Om gebruikers te helpen bij het ontwerpen van Q #-Bibliotheken, volgen we een aantal API-ontwerp principes om onze ontwerpen te begeleiden en om ervoor te zorgen dat we bruikbare bibliotheken kunnen maken voor de Quantum Development Community.
Dit artikel bevat een overzicht van deze principes en biedt voor beelden om te leren hoe u deze toepast bij het ontwerpen van Q # Api's.

> [!TIP]
> Dit is een redelijk gedetailleerd document dat is bedoeld om de ontwikkeling van bibliotheken en diep gaande bibliotheek bijdragen te helpen begeleiden.
> Waarschijnlijk zult u het het meest nuttig vinden als u uw eigen bibliotheken schrijft in Q # of als u grotere functies bijwerkt naar de [bibliotheek met q #-bibliotheken](https://github.com/microsoft/QuantumLibraries).
>
> Als u daarentegen meer wilt weten hoe u een bijdrage levert aan de Quantum Development Kit in het algemeen, kunt u beginnen met de [bijdrage gids](xref:microsoft.quantum.contributing).
> Als u meer algemene informatie wilt over hoe we u aanraden om uw Q #-code te Format teren, bent u mogelijk geïnteresseerd in het uitchecken van de [stijl gids](xref:microsoft.quantum.contributing.style).

## <a name="general-principles"></a>Algemene principes

**Sleutel principe:** Stel Api's beschikbaar die de focus op Quantum toepassingen plaatsen.

- ✅**Kies bewerkingen** en functie namen die de structuur van algoritmen en toepassingen op hoog niveau weer spie gelen.
- ⛔️ **geen** api's beschikbaar stellen die voornamelijk gericht zijn op implementatie details op laag niveau.

**Sleutel principe:** Begin elk API-ontwerp met voorbeeld cases om ervoor te zorgen dat Api's intuïtief zijn voor gebruik.

- ✅**Zorg ervoor dat** elk onderdeel van een open bare API een bijbehorende use-case heeft, in plaats van te ontwerpen voor alle mogelijke toepassingen vanaf het begin.
    Leg anders geen open bare Api's toe als ze nuttig zijn, maar zorg ervoor dat elk deel van een API een *concreet* voor beeld heeft waarin het handig is.

  *Voorbeelden:*
  - @"microsoft.quantum.canon.applytoeachca"kan worden gebruikt `ApplyToEachCA(H, _)` voor het voorbereiden van registers in een uniforme superpositie status, een veelvoorkomende taak in veel Quantum algoritmen. Dezelfde bewerking kan ook worden gebruikt voor veel andere taken in voor bereiding, numerieke tekens en op Oracle gebaseerde algoritmen.

- ✅**Maak** brainstorm en workshop nieuwe API-ontwerpen om te controleren of ze intuïtief zijn en voldoen aan de voorgestelde gebruiks voorbeelden.

  *Voorbeelden:*
  - Inspecteer de\# huidige Q-code om te zien hoe nieuwe API-ontwerpen de bestaande implementaties kunnen vereenvoudigen en verduidelijken.
  - Bekijk voorgestelde API-ontwerpen met vertegenwoordigers van primaire doel groepen.

**Sleutel principe:** Ontwerp Api's om Lees bare code te ondersteunen en te stimuleren.

- ✅Zorg **ervoor dat code kan worden gelezen** door domein experts en niet-experts.
- ✅**Plaats de** focus op de effecten van elke bewerking en functie binnen het algoritme op hoog niveau, met behulp van documentatie voor meer informatie over de implementatie, indien van toepassing.
- ✅Volg de algemene [Q\# -stijl gids](xref:microsoft.quantum.contributing.style) als **Dit** van toepassing is.

**Sleutel principe:** Ontwerp Api's stabiel en om voorwaartse compatibiliteit te bieden.

- ✅**DO** Verouderde api's op de juiste wijze af als er wijzigingen zijn vereist.

- ✅**Geef bewerkingen** en functies op waarmee de bestaande gebruikers code op de juiste wijze kan worden uitgevoerd tijdens de afschaffing.

  *Voorbeelden:*
  - Bij het wijzigen van de naam `EstimateExpectation` van `EstimateAverage`een bewerking die wordt aangeroepen in `EstimateExpectation` , wordt een nieuwe bewerking aangeroepen die de oorspronkelijke bewerking aanroept met de nieuwe naam, zodat bestaande code correct kan blijven werken.

- ✅**Gebruik het** @"microsoft.quantum.core.deprecated" kenmerk om afschaffing van de gebruiker te communiceren.

- ✅Als u de naam van een bewerking of functie **wijzigt, geeft** u de nieuwe naam op `@Deprecated`als een teken reeks invoer.

- ⛔️ **geen** bestaande functies of bewerkingen verwijderen zonder een afschaffing van ten minste zes maanden voor Preview-versies of ten minste twee jaar voor ondersteunde releases.

## <a name="functions-and-operations"></a>Functies en bewerkingen

**Sleutel principe:** zorg ervoor dat elke functie en bewerking een enkel goed gedefinieerd doel hebben in de API.

- ⛔️ **geen** functies en bewerkingen beschikbaar stellen waarmee meerdere niet-gerelateerde taken worden uitgevoerd.

**Sleutel principe:** ontwerp functies en-bewerkingen die zo mogelijk kunnen worden gebruikt en om te anticiperen op toekomstige behoeften.

- ✅Ontwerp functies en-bewerkingen om goed te kunnen samen **werken** met andere functies en bewerkingen, zowel in dezelfde API als in eerdere bestaande bibliotheken.

  *Voorbeelden:*
  - De @"microsoft.quantum.canon.delay" bewerking maakt minimale veronderstellingen over de invoer en kan dus worden gebruikt voor het uitstellen van toepassingen van bewerkingen in de standaard bibliotheek van Q # of zoals gedefinieerd door gebruikers.
    <!-- TODO: define bad example. -->

- ✅**Zorg** dat er louter deterministische, klassieke logica als functies beschikbaar zijn in plaats van bewerkingen.

  *Voorbeelden:*
  - Een subroutine waarmee de drijvende-komma invoer kan worden gedeterministisch, en moet dus worden blootgesteld aan de gebruiker, `Squared : Double -> Double` in plaats van als een bewerking `Square : Double => Double`. Op die manier kan de subroutine op meer locaties worden aangeroepen (bijvoorbeeld: binnen andere functies) en kunnen er nuttige optimalisatie gegevens worden verstrekt aan de compiler die van invloed kan zijn op de prestaties en Optima Lise ring.
  - `ForEach<'TInput, 'TOutput>('TInput => 'TOutput, 'TInput[]) => 'TOutput[]`en `Mapped<'TInput, 'TOutput>('TInput -> 'TOutput, 'TInput[]) -> 'TOutput[]` verschillen van de garanties die zijn aangebracht met betrekking tot determinism; beide zijn handig in verschillende omstandigheden.
  - API-routines waarmee de toepassing van Quantum bewerkingen wordt getransformeerd, kunnen vaak op een deterministische manier worden uitgevoerd en kunnen daarom beschikbaar worden `CControlled<'T>(op : 'T => Unit) => ((Bool, 'T) => Unit)`gemaakt als functies zoals.

- ✅**Generaliseer** het invoer type zoveel mogelijk voor elke functie en bewerking, met behulp van type parameters als dat nodig is.

  *Voorbeelden:*
  - `ApplyToEach`heeft type `<'T>(('T => Unit), 'T[]) => Unit` in plaats van het specifieke type van de meest voorkomende toepassing `((Qubit => Unit), Qubit[]) => Unit`,.

> [!TIP]
> Het is belang rijk om toekomstige behoeften te anticiperen, maar het is ook belang rijk om concrete problemen voor uw gebruikers op te lossen.
> Op basis van dit belang rijk beginsel moet altijd zorgvuldig worden gekeken en gebalanceerd om het ontwikkelen van Api's "alleen in het geval" te voor komen.

**Sleutel principe:** Kies invoer-en uitvoer typen voor functies en bewerkingen die voorspelbaar zijn en die het doel van een aanroep bare communicatie geven.

- ✅**Gebruik tuple** -typen om invoer en uitvoer logisch te groeperen die alleen aanzienlijk zijn wanneer deze samen worden beschouwd. U kunt in deze gevallen gebruikmaken van een door de gebruiker gedefinieerd type.

  *Voorbeelden:*
  - Een functie voor het uitvoeren van de lokale minima van een andere functie moet mogelijk grenzen van een zoek interval als invoer hebben, zodat `LocalMinima(fn : (Double -> Double), (left : Double, right : Double)) : Double` dit een juiste hand tekening kan zijn.
  - Een bewerking voor het ramen van een afgeleide van een machine learning classificatie met behulp van de para meter Shift-techniek moet mogelijk zowel de verschoven als niet-verwerkte parameter vectoren als invoer hebben. In dit geval kan `(unshifted : Double[], shifted : Double[])` een invoer vergelijkbaar zijn met die van toepassing.

- ✅**Volg items** in de invoer-en uitvoer-Tuples consistent in de verschillende functies en bewerkingen.

  *Voorbeelden:*
  - Als u twee of functions of bewerkingen overweegt die elk een rotatie hoek hebben en een doel-Qubit als invoer, moet u ervoor zorgen dat ze hetzelfde zijn gerangschikt in elke ingevoerde tuple. Dat wil zeggen, `ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl` liever `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` en `ApplyRotation(target : Qubit, angle : Double) : Unit is Adj + Ctl` aan `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)`en.

**Sleutel principe:** ontwerp functies en bewerkingen die goed werken met Q\# -taal functies zoals gedeeltelijke toepassingen.

- ✅**Bestel items** in invoer-Tuples, zodat de meest voorkomende invoer het eerst wordt uitgevoerd (dat wil zeggen: zodat gedeeltelijke toepassingen op dezelfde manier reageren op currying).

  *Voorbeelden:*
  - Een bewerking `ApplyRotation` waarbij een drijvende-komma nummer en een Qubit worden gebruikt als invoer wordt vaak gedeeltelijk toegepast met de drijvende-komma invoer voor gebruik met bewerkingen waarvoor een invoer van het `Qubit => Unit`type wordt verwacht. Daarom is een hand tekening van`operation ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl`
      werkt het meest consistent met een gedeeltelijke toepassing.
  - Normaal gesp roken houdt dit in dat alle klassieke gegevens worden geplaatst vóór alle qubits in de invoer-Tuples, maar een goede arrest gebruiken en onderzoeken hoe uw API in de praktijk wordt genoemd.

## <a name="user-defined-types"></a>Door de gebruiker gedefinieerde typen

**Belangrijkste methode:** gebruik door de gebruiker gedefinieerde typen om api's duidelijker en handiger te maken.

- ✅**Introduceer** nieuwe door de gebruiker gedefinieerde typen om nuttige steno te bieden voor lange en/of gecompliceerde typen.

  *Voorbeelden:*
  - In gevallen waarin een bewerkings type met drie Qubit-matrix invoer meestal als invoer wordt beschouwd of als uitvoer wordt geretourneerd, waardoor een UDT zoals`newtype TimeDependentBlockEncoding = ((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl)`
      kan u helpen een nuttige steno te bieden.

- ✅**Voer** nieuwe door de gebruiker gedefinieerde typen in om aan te geven dat een bepaald basis type alleen in een zeer bepaalde zin moet worden gebruikt.

  *Voorbeelden:*
  - Een bewerking die specifiek moet worden geïnterpreteerd als een bewerking die klassieke gegevens in een Quantum REGI ster codeert, kan geschikt zijn voor een label met een door `newtype InputEncoder = (Apply : (Qubit[] => Unit))`de gebruiker gedefinieerd type.

- ✅**Introduceer** nieuwe door de gebruiker gedefinieerde typen met benoemde items die toekomstige uitbreid baarheid mogelijk maken (bijvoorbeeld: een structuur van resultaten die in de toekomst extra benoemde items kan bevatten).

  *Voorbeelden:*
  - Wanneer een bewerking `TrainModel` een groot aantal configuratie opties beschikbaar stelt, worden deze opties weer gegeven als een nieuwe `TrainingOptions` UDT en kunnen gebruikers met een `DefaultTrainingOptions : Unit -> TrainingOptions` nieuwe functie specifieke, benoemde items in TrainingOptions UDT-waarden overschrijven, terwijl bibliotheken ontwikkel aars nog steeds nieuwe UDT-items kunnen toevoegen.

- ✅**Declareer** benoemde items voor nieuwe door de gebruiker gedefinieerde typen in de voor keur om te vereisen dat gebruikers de juiste tuple-ontbouwing kennen.

  *Voorbeelden:*
  - Als u een complex getal in de polaire ontleding vertegenwoordigt `newtype ComplexPolar = (Magnitude: Double, Argument: Double)` , `newtype ComplexPolar = (Double, Double)`krijgt u de voor keur.

**Belang rijk:** gebruik door de gebruiker gedefinieerde typen op manieren om de cognitieve belasting te reduceren en niet dat de gebruiker aanvullende concepten en de nomenclatuur hoeft te leren.

- ⛔️ **geen** door de gebruiker gedefinieerde typen die de gebruiker nodig heeft om veelvuldig gebruik te maken van de operator voor`!`uitpakken (), of waarvoor vaak meerdere niveaus van het uitpakken nodig zijn. Mogelijke strategieën voor risico beperking zijn:

  - Wanneer u een door de gebruiker gedefinieerd type zichtbaar maakt met één item, kunt u een naam voor dat item definiëren. Overweeg `newtype Encoder = (Apply : (Qubit[] => Unit is Adj + Ctl))` bijvoorbeeld bij voor keur aan `newtype Encoder = (Qubit[] => Unit is Adj + Ctl)`.

  - Zorg ervoor dat andere functies en bewerkingen de ' verpakte ' UDT-instanties rechtstreeks kunnen accepteren.

- ⛔️ **geen** nieuwe door de gebruiker gedefinieerde typen voor het dupliceren van ingebouwde typen, zonder extra betrouwbaarheid te bieden.

  *Voorbeelden:*
  - Een UDT `newtype QubitRegister = Qubit[]` biedt geen extra `Qubit[]`duidelijkheid en is dus moeilijker te gebruiken zonder te voor deel.
  - Een UDT `newtype LittleEndian = Qubit[]` -document geeft aan hoe het onderliggende REGI ster moet worden gebruikt en geïnterpreteerd, en biedt daarom een extra beschrijving van het basis type.

- ⛔️ **geen** accessor-functies, tenzij strikt vereist;   in dit geval is het zeer handig om benoemde items te noemen.

  *Voorbeelden:*
  - Wanneer u een UDT `newtype Complex = (Double, Double)`introduceert, wijzigt u de definitie `newtype Complex = (Real : Double, Imag : Double)` voor het introduceren van functies `GetReal : Complex -> Double` en `GetImag : Complex -> Double`.

## <a name="namespaces-and-organization"></a>Naam ruimten en organisatie

**Sleutel principe:** Kies naam ruimte namen die voorspelbaar zijn en waarmee duidelijk het doel van functies, bewerkingen en door de gebruiker gedefinieerde typen in elke naam ruimte kan worden gecommuniceerd.

- ✅**Geef** naam ruimten op als `Publisher.Product.DomainArea`.

  *Voorbeelden:*
  - Functies, bewerkingen en UDTs die door micro soft zijn gepubliceerd als onderdeel van de Quantum simulatie functie van de Quantum Development Kit, worden in `Microsoft.Quantum.Simulation` de naam ruimte geplaatst.
  - `Microsoft.Quantum.Math`vertegenwoordigt een naam ruimte die door micro soft is gepubliceerd als onderdeel van de Quantum Development Kit die betrekking heeft op het wiskunde domein gebied.

- ✅**Plaats bewerkingen** , functies en door de gebruiker gedefinieerde typen die worden gebruikt voor specifieke functionaliteit in een naam ruimte die deze functionaliteit beschrijft, zelfs wanneer die functionaliteit wordt gebruikt in verschillende probleem domeinen.

  *Voorbeelden:*
  - Status voorbereiding-Api's die door micro soft zijn gepubliceerd als onderdeel van de Quantum Development Kit, `Microsoft.Quantum.Preparation`worden opgenomen in.
  - Quantum simulatie Api's die door micro soft zijn gepubliceerd als onderdeel van de Quantum Development Kit, worden `Microsoft.Quantum.Simulation`opgenomen in.

- ✅**Plaatsen bewerkingen** , functies en door de gebruiker gedefinieerde typen die alleen binnen specifieke domeinen worden gebruikt in naam ruimten die het domein van het hulp programma aangeven. Gebruik, indien nodig, subnaam ruimten om taken binnen elke domein-specifieke naam ruimte aan te duiden.

  *Voorbeelden:*
  - De Quantum machine learning bibliotheek die door micro soft is gepubliceerd, wordt @"microsoft.quantum.machinelearning" voornamelijk in de naam ruimte geplaatst, maar voor @"microsoft.quantum.machinelearning.datasets" beelden van gegevens sets worden door de naam ruimte verschaft.
  - Quantum chemie-Api's die door micro soft zijn gepubliceerd als onderdeel van de Quantum Development Kit, `Microsoft.Quantum.Chemistry`moeten in worden geplaatst. De functionaliteit die specifiek is voor het implementeren van de Wigner-ontleding, `Microsoft.Quantum.Chemistry.JordanWigner`kan in worden geplaatst, zodat de primaire interface voor het domein gebied van de quantum chemie geen betrekking heeft op implementaties.

**Sleutel principe:** Gebruik naam ruimten en toegangs parameters samen om het API-Opper vlak dat wordt blootgesteld aan gebruikers te gebruiken en om interne gegevens te verbergen met betrekking tot de implementatie en het testen van uw Api's.

- ✅Indien redelijk moeten alle functies en bewerkingen **worden uitgevoerd die** nodig zijn om een API te implementeren in dezelfde naam ruimte als de API die wordt geïmplementeerd, maar gemarkeerd met de sleutel woorden ' privé ' of ' intern ' om aan te geven dat ze geen deel uitmaken van het open bare API-Opper vlak voor een tape wisselaar. Gebruik een naam die begint met een onderstrepings teken (`_`) om persoonlijke en interne bewerkingen en functies van open bare callables visueel te onderscheiden.

  *Voorbeelden:*
  - De naam `_Features` van de bewerking geeft een functie aan die privé is voor een bepaalde naam ruimte en assembly, en moet `internal` vergezeld gaan van het sleutel woord.

- ✅In het zeldzame geval dat een uitgebreide set persoonlijke functies of bewerkingen nodig zijn om de API voor een bepaalde naam ruimte te implementeren, **moet u** deze in een nieuwe naam ruimte plaatsen die overeenkomt met de `.Private`naam ruimte die wordt geïmplementeerd en eindigt op.

- ✅**Plaats alle** eenheids tests in naam ruimten die overeenkomen met de naam ruimte onder `.Tests`testen en eindigend op.

## <a name="naming-conventions-and-vocabulary"></a>Naam conventies en woordenlijst

**Sleutel principe:** Kies namen en terminologie die duidelijk, toegankelijk en leesbaar zijn in een verscheidenheid aan doel groepen, met inbegrip van beide quantums en experts.

- ⛔️ **geen** discriminerende of uitgesloten id-namen en terminologie in API-documentatie opmerkingen gebruiken.

- ✅**Gebruik API** -documentatie opmerkingen om relevante context, voor beelden en verwijzingen te bieden, met name voor meer moeilijke concepten.

- ⛔️ **geen** id-namen gebruiken die onnodig esoterische zijn, of waarvoor belang rijke Quantum algoritmen kennis hebben om te lezen.

  *Voorbeelden:*
  - Kies voor keur voor ' amplitude versterking ' naar ' Grover iteratie '.

- ✅**Kies bewerkingen** en functie namen waarmee duidelijk het beoogde effect van een aanroepbaar en niet de implementatie wordt gecommuniceerd. Houd er rekening mee dat de implementatie kan en moet worden beschreven in [API-documentatie opmerkingen](xref:microsoft.quantum.language.statements#documentation-comments).

  *Voorbeelden:*
  - De voor keur ' schatting overlappen ' op ' Hadamard test ', aangezien de laatste wordt gecommuniceerd hoe de voormalige wordt geïmplementeerd.

- ✅**Gebruik woorden** op een consistente manier in alle Q\# -api's:

  - **Termen**

    - **Assert**: Controleer of een veronderstelling over de status van een doel computer en de qubits-bewaringen mogelijk is door gebruik te maken van niet-fysieke resources. Bewerkingen die gebruikmaken van deze term moeten altijd veilig kunnen worden verwijderd zonder dat dit van invloed is op de functionaliteit van bibliotheken en uitvoer bare Program ma's. Houd er rekening mee dat de beweringen in het algemeen afhankelijk zijn van externe status, zoals de status van een Qubit-REGI ster, de uitvoerings omgeving of dergelijke. Als afhankelijkheid van de externe status is een soort neven effect, moeten beweringen worden weer gegeven als bewerkingen in plaats van functions.

    - **Schatting**: als u een of meer mogelijk herhaalde metingen gebruikt, moet u een klassiek aantal van meet resultaten schatten.

      *Voorbeelden:*
      - @"microsoft.quantum.characterization.estimatefrequency"
      - @"microsoft.quantum.characterization.estimateoverlapbetweenstates"

    - **Voorbereiden**: een Quantum bewerking of volg orde van bewerkingen Toep assen op een of meer qubits, aangenomen dat deze wordt gestart met een bepaalde begin status (doorgaans $ \ket{00\cdots 0} $), waardoor de status van die qubits naar een gewenste eind status kan worden gegroeid. Over het algemeen **kan** het optreden op andere statussen dan de opgegeven start status leiden tot een niet-gedefinieerde unitary-trans formatie, maar **moet** nog steeds zorgen dat een bewerking en de adjoint ' annuleren ' worden bewaard en er geen op worden toegepast.

      *Voorbeelden:*
      - @"microsoft.quantum.preparation.preparearbitrarystate"
      - @"microsoft.quantum.preparation.prepareuniformsuperposition"

    - **Meting**: een Quantum bewerking of een reeks bewerkingen Toep assen op een of meer qubits. er wordt een back-up van klassieke gegevens weer gegeven.

      *Voorbeelden:*
      - @"microsoft.quantum.intrinsic.measure"
      - @"microsoft.quantum.arithmetic.measurefxp"
      - @"microsoft.quantum.arithmetic.measureinteger"

    - **Toep assen**: een Quantum bewerking of reeks bewerkingen Toep assen op een of meer qubits, waardoor de status van die qubits op een samenhangende manier kan worden gewijzigd. Dit woord is de meest algemene term in Q\# -nomenclatuur en **mag niet worden** gebruikt wanneer een meer specifieke term direct relevant is.

  - **Zelfstandige naam woorden**:

    - **Fact**: een Booleaanse voor waarde die alleen afhankelijk is van de invoer en niet van de status van een doel computer, de omgeving of de status van de qubits van de machine. In tegens telling tot een bevestiging is een feit alleen gevoelig voor de *waarden* die aan dat feit worden gegeven. Bijvoorbeeld:

      *Voorbeelden:*
      - @"microsoft.quantum.diagnostics.equalityfacti": vertegenwoordigt een gelijkheids feit over twee integer-invoer; de gehele getallen die als invoer worden opgegeven, zijn gelijk aan elkaar of ze zijn niet onafhankelijk van een andere programma status.

    - **Opties:** Een UDT met meerdere benoemde items die als optionele argumenten kunnen fungeren voor een functie of bewerking. Bijvoorbeeld:

      *Voorbeelden:*
      - De @"microsoft.quantum.machinelearning.trainingoptions" UDT bevat benoemde items voor Learning rate, minibatch-grootte en andere Configureer bare para meters voor ml-training.

  - **Bijvoegingen**:

    - ⛔️ **Nieuw**: deze bijvoeger **mag niet** worden gebruikt, om Verwar ring met het gebruik als een werk woord te voor komen in veel programmeer talen (bijvoorbeeld: C++, C#, Java, type script, Power shell).

  - Voor **zetsels:** In sommige gevallen kunnen preposities worden gebruikt om de rollen van zelfstandige naam woorden en termen in functie-en bewerkings namen verder te dubbel zinnigheid of te verduidelijken. Zorg ervoor dat dit echter spaarzaam en consistent is.

    - **Als:** Hiermee wordt aangegeven dat de invoer en uitvoer van een functie dezelfde informatie vertegenwoordigen, maar dat de uitvoer de gegevens vertegenwoordigt **als** een *X* in plaats van de oorspronkelijke weer gave. Dit is met name gebruikelijk voor functies van type conversie.

      *Voorbeelden:*
      - `IntAsDouble(2)`Hiermee wordt aangegeven dat zowel de`2`invoer () als de`2.0`uitvoer () op kwalitatieve manier dezelfde informatie vertegenwoordigen, maar met\# verschillende gegevens typen van Q.

    - **Van:** Om consistentie te garanderen, mag deze voor positie **niet** worden gebruikt om type conversie functies of een ander geval waar **dat** van toepassing is, aan te geven.

    - ⛔️ **:** deze voor positie **mag niet** worden gebruikt, zodat Verwar ring met het gebruik als een werk woord in veel programmeer talen wordt voor komen.
