---
title: 'Q # API-ontwerp principes'
description: 'Q # API-ontwerp principes'
author: cgranade
ms.author: chgranad
ms.date: 3/9/2020
ms.topic: article
uid: microsoft.quantum.contributing.api-design
ms.openlocfilehash: 03c32331f8988181ec6fedcfc207d752b4a880b2
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024199"
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

- ✅ **Kies** bewerking en functie namen die de structuur van algoritmen en toepassingen op hoog niveau weer spie gelen.
- ⛔️ **geen** api's beschikbaar stellen die voornamelijk gericht zijn op implementatie details op laag niveau.

**Sleutel principe:** Begin elk API-ontwerp met voorbeeld cases om ervoor te zorgen dat Api's intuïtief zijn voor gebruik.

- ✅ **moet u** ervoor zorgen dat elk onderdeel van een open bare API een bijbehorende use-case heeft, in plaats van te ontwerpen voor alle mogelijke toepassingen vanaf het begin.
    Leg anders geen open bare Api's toe als ze nuttig zijn, maar zorg ervoor dat elk deel van een API een *concreet* voor beeld heeft waarin het handig is.

  *Vindt*
  - @"microsoft.quantum.canon.applytoeachca" kunnen worden gebruikt als `ApplyToEachCA(H, _)` om registers voor te bereiden in een uniforme superpositie status, een gemeen schappelijke taak in veel Quantum algoritmen. Dezelfde bewerking kan ook worden gebruikt voor veel andere taken in voor bereiding, numerieke tekens en op Oracle gebaseerde algoritmen.

- ✅ **brainstorm** en workshop nieuwe API ontwerpen om te controleren of ze intuïtief zijn en voldoen aan de voorgestelde gebruiks voorbeelden.

  *Vindt*
  - Inspecteer huidige Q\#-code om te zien hoe nieuwe API-ontwerpen de bestaande implementaties kunnen vereenvoudigen en verduidelijken.
  - Bekijk voorgestelde API-ontwerpen met vertegenwoordigers van primaire doel groepen.

**Sleutel principe:** Ontwerp Api's om Lees bare code te ondersteunen en te stimuleren.

- ✅ **moet u** ervoor zorgen dat code leesbaar is voor domein experts en niet-experts.
- ✅ **doen** de focus op de effecten van elke bewerking en functie binnen het algoritme op hoog niveau, met behulp van documentatie voor meer informatie over de implementatie.
- Volg de algemene [Q\# stijl handleiding](xref:microsoft.quantum.contributing.style) ✅ als **Dit** van toepassing is.

**Sleutel principe:** Ontwerp Api's stabiel en om voorwaartse compatibiliteit te bieden.

- ✅ **oude** api's op de juiste wijze af als er wijzigingen zijn vereist.

- ✅ **do** ' Shim ' bewerkingen en functies waarmee bestaande gebruikers code op de juiste wijze kan worden uitgevoerd tijdens de afschaffing.

  *Vindt*
  - Bij het wijzigen van de naam van een bewerking met de naam `EstimateExpectation` op `EstimateAverage`, wordt een nieuwe bewerking met de naam `EstimateExpectation` geïntroduceerd die de oorspronkelijke bewerking aanroept met de nieuwe naam, zodat bestaande code correct kan blijven werken.

- Gebruik **✅** het kenmerk @"microsoft.quantum.core.deprecated" om afschaffings naar de gebruiker te communiceren.

- ✅ bij het wijzigen van de naam van een bewerking of **functie, geeft u de** nieuwe naam op als een teken reeks invoer voor `@Deprecated`.

- ⛔️ **geen** bestaande functies of bewerkingen verwijderen zonder een afschaffing van ten minste zes maanden voor Preview-versies of ten minste twee jaar voor ondersteunde releases.

## <a name="functions-and-operations"></a>Functies en bewerkingen

**Sleutel principe:** zorg ervoor dat elke functie en bewerking een enkel goed gedefinieerd doel hebben in de API.

- ⛔️ **geen** functies en bewerkingen beschikbaar stellen waarmee meerdere niet-gerelateerde taken worden uitgevoerd.

**Sleutel principe:** ontwerp functies en-bewerkingen die zo mogelijk kunnen worden gebruikt en om te anticiperen op toekomstige behoeften.

- ✅ **ontwerp** functies en-bewerkingen goed samen met andere functies en bewerkingen, zowel in dezelfde API als in eerdere bestaande bibliotheken.

  *Vindt*
  - Met de @"microsoft.quantum.canon.delay" bewerking worden minimale veronderstellingen over de invoer gemaakt en kunnen ze worden gebruikt voor het uitstellen van toepassingen van bewerkingen in de standaard bibliotheek van Q # of zoals gedefinieerd door gebruikers.
    <!-- TODO: define bad example. -->

- ✅ **do** louter deterministische klassieke logica als functies beschikbaar in plaats van bewerkingen.

  *Vindt*
  - Een subroutine waarmee de drijvende-komma invoer kan worden gedeterministisch, en moet dus worden blootgesteld aan de gebruiker als `Squared : Double -> Double` in plaats van als een bewerking `Square : Double => Double`. Op die manier kan de subroutine op meer locaties worden aangeroepen (bijvoorbeeld: binnen andere functies) en kunnen er nuttige optimalisatie gegevens worden verstrekt aan de compiler die van invloed kan zijn op de prestaties en Optima Lise ring.
  - `ForEach<'TInput, 'TOutput>('TInput => 'TOutput, 'TInput[]) => 'TOutput[]` en `Mapped<'TInput, 'TOutput>('TInput -> 'TOutput, 'TInput[]) -> 'TOutput[]` verschillen van de garanties die zijn aangebracht met betrekking tot determinism; beide zijn handig in verschillende omstandigheden.
  - API-routines waarmee de toepassing van Quantum bewerkingen wordt getransformeerd, kunnen vaak op een deterministische manier worden uitgevoerd en kunnen daarom beschikbaar worden gemaakt als functies als `CControlled<'T>(op : 'T => Unit) => ((Bool, 'T) => Unit)`.

- ✅ **generaliseert u het** invoer type zoveel mogelijk voor elke functie en bewerking, met behulp van type parameters als dat nodig is.

  *Vindt*
  - `ApplyToEach` is van het type `<'T>(('T => Unit), 'T[]) => Unit` in plaats van het specifieke type van de meest voorkomende toepassing `((Qubit => Unit), Qubit[]) => Unit`.

> [!TIP]
> Het is belang rijk om toekomstige behoeften te anticiperen, maar het is ook belang rijk om concrete problemen voor uw gebruikers op te lossen.
> Op basis van dit belang rijk beginsel moet altijd zorgvuldig worden gekeken en gebalanceerd om het ontwikkelen van Api's "alleen in het geval" te voor komen.

**Sleutel principe:** Kies invoer-en uitvoer typen voor functies en bewerkingen die voorspelbaar zijn en die het doel van een aanroep bare communicatie geven.

- ✅ **gebruik** tuple-typen om invoer en uitvoer logisch te groeperen die alleen aanzienlijk zijn wanneer deze samen worden beschouwd. U kunt in deze gevallen gebruikmaken van een door de gebruiker gedefinieerd type.

  *Vindt*
  - Een functie voor het uitvoeren van de lokale minima van een andere functie moet mogelijk grenzen hebben van een zoek interval als invoer, zodat `LocalMinima(fn : (Double -> Double), (left : Double, right : Double)) : Double` mogelijk een juiste hand tekening is.
  - Een bewerking voor het ramen van een afgeleide van een machine learning classificatie met behulp van de para meter Shift-techniek moet mogelijk zowel de verschoven als niet-verwerkte parameter vectoren als invoer hebben. In dit geval kan een invoer vergelijkbaar zijn met `(unshifted : Double[], shifted : Double[])`.

- ✅ **Volg** items in de invoer-en uitvoer-Tuples consistent in de verschillende functies en bewerkingen.

  *Vindt*
  - Als u twee of functions of bewerkingen overweegt die elk een rotatie hoek hebben en een doel-Qubit als invoer, moet u ervoor zorgen dat ze hetzelfde zijn gerangschikt in elke ingevoerde tuple. Dat wil zeggen dat u de voor keur geeft `ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl` en `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` `ApplyRotation(target : Qubit, angle : Double) : Unit is Adj + Ctl` en `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)`.

**Belang rijk:** ontwerp functies en bewerkingen die goed werken met Q\#-taal functies zoals gedeeltelijke toepassingen.

- ✅ **do** items in invoer Tuples, zodat de meest voorkomende invoer het eerst wordt uitgevoerd (dat wil zeggen, zodat gedeeltelijke toepassingen op dezelfde manier reageren op currying).

  *Vindt*
  - Een bewerking `ApplyRotation` die een drijvende-komma nummer en een Qubit gebruikt omdat invoer vaak gedeeltelijk wordt toegepast met de drijvende-komma invoer voor gebruik met bewerkingen waarvoor een invoer van het type `Qubit => Unit`wordt verwacht. Daarom is een hand tekening van `operation ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl`
      werkt het meest consistent met een gedeeltelijke toepassing.
  - Normaal gesp roken houdt dit in dat alle klassieke gegevens worden geplaatst vóór alle qubits in de invoer-Tuples, maar een goede arrest gebruiken en onderzoeken hoe uw API in de praktijk wordt genoemd.

## <a name="user-defined-types"></a>Door de gebruiker gedefinieerde typen

**Belangrijkste methode:** gebruik door de gebruiker gedefinieerde typen om api's duidelijker en handiger te maken.

- ✅ voeren nieuwe door de gebruiker gedefinieerde typen **uit** om nuttige steno te bieden voor lange en/of gecompliceerde typen.

  *Vindt*
  - In gevallen waarin een bewerkings type met drie Qubit-matrix invoer meestal als invoer wordt beschouwd of als uitvoer wordt geretourneerd, waardoor een UDT, zoals `newtype TimeDependentBlockEncoding = ((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl)`
      kan u helpen een nuttige steno te bieden.

- ✅ voeren nieuwe door de gebruiker gedefinieerde **typen uit om** aan te geven dat een bepaald basis type alleen in een zeer bepaalde zin moet worden gebruikt.

  *Vindt*
  - Een bewerking die specifiek moet worden geïnterpreteerd als een bewerking die klassieke gegevens in een Quantum REGI ster codeert, kan geschikt zijn voor een label met een door de gebruiker gedefinieerd type `newtype InputEncoder = (Apply : (Qubit[] => Unit))`.

- ✅ voeren nieuwe door de gebruiker gedefinieerde **typen uit met** benoemde items die toekomstige uitbreid baarheid mogelijk maken (bijvoorbeeld: een resultaten structuur die in de toekomst extra benoemde items kan bevatten).

  *Vindt*
  - Wanneer een bewerking `TrainModel` een groot aantal configuratie opties beschikbaar stelt, worden deze opties weer gegeven als een nieuwe `TrainingOptions` UDT en een nieuwe functie `DefaultTrainingOptions : Unit -> TrainingOptions` kunnen gebruikers specifieke benoemde items in TrainingOptions UDT-waarden overschrijven, terwijl ontwikkel aars van de bibliotheek nog steeds nieuwe UDT-items kunnen toevoegen.

- ✅ zou benoemde items voor nieuwe door de gebruiker gedefinieerde typen in de voor keur declareren om gebruikers te laten weten dat ze de juiste tuple-ontbouwing **hebben** .

  *Vindt*
  - Wanneer een complex getal in de polaire ontleding vertegenwoordigt, wordt de voor keur `newtype ComplexPolar = (Magnitude: Double, Argument: Double)` `newtype ComplexPolar = (Double, Double)`.

**Belang rijk:** gebruik door de gebruiker gedefinieerde typen op manieren om de cognitieve belasting te reduceren en niet dat de gebruiker aanvullende concepten en de nomenclatuur hoeft te leren.

- ⛔️ **geen** door de gebruiker gedefinieerde typen die de gebruiker nodig heeft om veelvuldig gebruik te maken van de operator voor uitpakken (`!`) of waarvoor vaak meerdere niveaus van het uitpakken nodig zijn. Mogelijke strategieën voor risico beperking zijn:

  - Wanneer u een door de gebruiker gedefinieerd type zichtbaar maakt met één item, kunt u een naam voor dat item definiëren. Overweeg bijvoorbeeld `newtype Encoder = (Apply : (Qubit[] => Unit is Adj + Ctl))` in de voor keur aan `newtype Encoder = (Qubit[] => Unit is Adj + Ctl)`.

  - Zorg ervoor dat andere functies en bewerkingen de ' verpakte ' UDT-instanties rechtstreeks kunnen accepteren.

- ⛔️ **geen** nieuwe door de gebruiker gedefinieerde typen voor het dupliceren van ingebouwde typen, zonder extra betrouwbaarheid te bieden.

  *Vindt*
  - Een UDT-`newtype QubitRegister = Qubit[]` biedt geen extra duidelijkheid voor `Qubit[]`en is dus moeilijker te gebruiken zonder te profiteren van voor deel.
  - Een UDT `newtype LittleEndian = Qubit[]` documenten hoe het onderliggende REGI ster moet worden gebruikt en geïnterpreteerd, en biedt daarom een extra duidelijkheid van het basis type.

- ⛔️ **geen** accessor-functies, tenzij strikt vereist;   in dit geval is het zeer handig om benoemde items te noemen.

  *Vindt*
  - Wanneer u een UDT-`newtype Complex = (Double, Double)`introduceert, wijzigt u de voor keur voor het wijzigen van de definitie in `newtype Complex = (Real : Double, Imag : Double)` om functies `GetReal : Complex -> Double` en `GetImag : Complex -> Double`te introduceren.

## <a name="namespaces-and-organization"></a>Naam ruimten en organisatie

**Sleutel principe:** Kies naam ruimte namen die voorspelbaar zijn en waarmee duidelijk het doel van functies, bewerkingen en door de gebruiker gedefinieerde typen in elke naam ruimte kan worden gecommuniceerd.

- ✅ **do** naam ruimten als `Publisher.Product.DomainArea`.

  *Vindt*
  - Functies, bewerkingen en UDTs die door micro soft zijn gepubliceerd als onderdeel van de Quantum simulatie functie van de Quantum Development Kit, worden in de naam ruimte `Microsoft.Quantum.Simulation` geplaatst.
  - `Microsoft.Quantum.Math` vertegenwoordigt een naam ruimte die door micro soft is gepubliceerd als onderdeel van de Quantum Development Kit die betrekking heeft op het wiskunde domein gebied.

- ✅ bewerkingen, functies en door de gebruiker gedefinieerde typen **die worden gebruikt** voor specifieke functionaliteit, plaatsen in een naam ruimte die deze functionaliteit beschrijft, zelfs wanneer die functionaliteit wordt gebruikt in verschillende probleem domeinen.

  *Vindt*
  - Status voorbereiding-Api's die door micro soft zijn gepubliceerd als onderdeel van de Quantum Development Kit, worden in `Microsoft.Quantum.Preparation`geplaatst.
  - De Quantum simulatie Api's die door micro soft zijn gepubliceerd als onderdeel van de Quantum Development Kit, worden in `Microsoft.Quantum.Simulation`geplaatst.

- ✅ bewerkingen, functies en door de gebruiker gedefinieerde typen die alleen binnen specifieke **domeinen worden gebruikt** in naam ruimten die het domein van het hulp programma zijn. Gebruik, indien nodig, subnaam ruimten om taken binnen elke domein-specifieke naam ruimte aan te duiden.

  *Vindt*
  - De Quantum machine learning bibliotheek die door micro soft is gepubliceerd, wordt in het grootst in de @"microsoft.quantum.machinelearning" naam ruimte geplaatst, maar voor beelden van gegevens sets worden gegeven door de @"microsoft.quantum.machinelearning.datasets" naam ruimte.
  - Quantum chemie-Api's die door micro soft zijn gepubliceerd als onderdeel van de Quantum Development Kit, moeten in `Microsoft.Quantum.Chemistry`worden geplaatst. De functionaliteit die specifiek is voor het implementeren van de Wigner-ontleding, kan in `Microsoft.Quantum.Chemistry.JordanWigner`worden geplaatst, zodat de primaire interface voor het domein gebied van de quantum chemie geen betrekking heeft op implementaties.

**Sleutel principe:** Gebruik naam ruimten en toegangs parameters samen om het API-Opper vlak dat wordt blootgesteld aan gebruikers te gebruiken en om interne gegevens te verbergen met betrekking tot de implementatie en het testen van uw Api's.

- ✅ indien redelijk alle **DO** functies en bewerkingen die nodig zijn voor het implementeren van een API in dezelfde naam ruimte als de API die wordt geïmplementeerd, maar gemarkeerd met de sleutel woorden ' privé ' of ' intern ' om aan te geven dat ze geen deel uitmaken van het open bare API-Opper vlak voor een tape wisselaar. Gebruik een naam die begint met een onderstrepings teken (`_`) om persoonlijke en interne bewerkingen en functies van open bare callables visueel te onderscheiden.

  *Vindt*
  - De naam van de bewerking `_Features` geeft een functie aan die privé is voor een bepaalde naam ruimte en assembly, en moet vergezeld gaan van het sleutel woord `internal`.

- ✅ in het zeldzame geval dat een uitgebreide set persoonlijke functies of bewerkingen nodig zijn om de API voor een bepaalde naam ruimte te implementeren, **moet u** deze in een nieuwe naam ruimte plaatsen die overeenkomt met de naam ruimte die wordt geïmplementeerd en eindigt in `.Private`.

- ✅ **plaats** alle eenheids tests in naam ruimten die overeenkomen met de naam ruimte onder testen en eindigend in `.Tests`.

## <a name="naming-conventions-and-vocabulary"></a>Naam conventies en woordenlijst

**Sleutel principe:** Kies namen en terminologie die duidelijk, toegankelijk en leesbaar zijn in een verscheidenheid aan doel groepen, met inbegrip van beide quantums en experts.

- ⛔️ **geen** discriminerende of uitgesloten id-namen en terminologie in API-documentatie opmerkingen gebruiken.

- ✅ **gebruik** API-documentatie opmerkingen om relevante context, voor beelden en verwijzingen te bieden, met name voor meer moeilijke concepten.

- ⛔️ **geen** id-namen gebruiken die onnodig esoterische zijn, of waarvoor belang rijke Quantum algoritmen kennis hebben om te lezen.

  *Vindt*
  - Kies voor keur voor ' amplitude versterking ' naar ' Grover iteratie '.

- ✅ **Kies** bewerkingen en functie namen waarmee duidelijk het beoogde effect van een aanroepbaar en niet de implementatie wordt gecommuniceerd. Houd er rekening mee dat de implementatie kan en moet worden

  *Vindt*
  - De voor keur ' schatting overlappen ' op ' Hadamard test ', aangezien de laatste wordt gecommuniceerd hoe de voormalige wordt geïmplementeerd.

- ✅ **kunt** woorden op een consistente manier gebruiken in alle Q\#-api's:

  - **Termen**

    - **Assert**: Controleer of een veronderstelling over de status van een doel computer en de qubits-bewaringen mogelijk is door gebruik te maken van niet-fysieke resources. Bewerkingen die gebruikmaken van deze term moeten altijd veilig kunnen worden verwijderd zonder dat dit van invloed is op de functionaliteit van bibliotheken en uitvoer bare Program ma's. Houd er rekening mee dat de beweringen in het algemeen afhankelijk zijn van externe status, zoals de status van een Qubit-REGI ster, de uitvoerings omgeving of dergelijke. Als afhankelijkheid van de externe status is een soort neven effect, moeten beweringen worden weer gegeven als bewerkingen in plaats van functions.

    - **Schatting**: als u een of meer mogelijk herhaalde metingen gebruikt, moet u een klassiek aantal van meet resultaten schatten.

      *Vindt*
      - @"microsoft.quantum.characterization.estimatefrequency"
      - @"microsoft.quantum.characterization.estimateoverlapbetweenstates"

    - **Voorbereiden**: een Quantum bewerking of volg orde van bewerkingen Toep assen op een of meer qubits, aangenomen dat deze wordt gestart met een bepaalde begin status (doorgaans $ \ket{00\cdots 0} $), waardoor de status van die qubits naar een gewenste eind status kan worden gegroeid. Over het algemeen **kan** het optreden op andere statussen dan de opgegeven start status leiden tot een niet-gedefinieerde unitary-trans formatie, maar **moet** nog steeds zorgen dat een bewerking en de adjoint ' annuleren ' worden bewaard en er geen op worden toegepast.

      *Vindt*
      - @"microsoft.quantum.preparation.preparearbitrarystate"
      - @"microsoft.quantum.preparation.prepareuniformsuperposition"

    - **Meting**: een Quantum bewerking of een reeks bewerkingen Toep assen op een of meer qubits. er wordt een back-up van klassieke gegevens weer gegeven.

      *Vindt*
      - @"microsoft.quantum.intrinsic.measure"
      - @"microsoft.quantum.arithmetic.measurefxp"
      - @"microsoft.quantum.arithmetic.measureinteger"

    - **Toep assen**: een Quantum bewerking of reeks bewerkingen Toep assen op een of meer qubits, waardoor de status van die qubits op een samenhangende manier kan worden gewijzigd. Dit woord is de meest algemene term in Q\# Nomenclature, en **mag niet worden** gebruikt wanneer een meer specifieke term direct relevant is.

  - **Zelfstandige naam woorden**:

    - **Fact**: een Booleaanse voor waarde die alleen afhankelijk is van de invoer en niet van de status van een doel computer, de omgeving of de status van de qubits van de machine. In tegens telling tot een bevestiging is een feit alleen gevoelig voor de *waarden* die aan dat feit worden gegeven. Bijvoorbeeld:

      *Vindt*
      - @"microsoft.quantum.diagnostics.equalityfacti": vertegenwoordigt een gelijkheids feit over twee integer-invoer; de gehele getallen die als invoer worden opgegeven, zijn gelijk aan elkaar of ze zijn niet onafhankelijk van een andere programma status.

    - **Opties:** Een UDT met meerdere benoemde items die als optionele argumenten kunnen fungeren voor een functie of bewerking. Bijvoorbeeld:

      *Vindt*
      - De @"microsoft.quantum.machinelearning.trainingoptions" UDT bevat benoemde items voor Learning rate, minibatch-grootte en andere Configureer bare para meters voor ML-training.

  - **Bijvoegingen**:

    - ⛔️ **Nieuw**: deze bijvoeger **mag niet** worden gebruikt, om Verwar ring met het gebruik als een werk woord te voor komen in veel programmeer C++talen C#(bijvoorbeeld:,, Java, type script, Power shell).

  - Voor **zetsels:** In sommige gevallen kunnen preposities worden gebruikt om de rollen van zelfstandige naam woorden en termen in functie-en bewerkings namen verder te dubbel zinnigheid of te verduidelijken. Zorg ervoor dat dit echter spaarzaam en consistent is.

    - **Als:** Hiermee wordt aangegeven dat de invoer en uitvoer van een functie dezelfde informatie vertegenwoordigen, maar dat de uitvoer de gegevens vertegenwoordigt **als** een *X* in plaats van de oorspronkelijke weer gave. Dit is met name gebruikelijk voor functies van type conversie.

      *Vindt*
      - `IntAsDouble(2)` geeft aan dat zowel de invoer (`2`) als de uitvoer (`2.0`) op basis van dezelfde informatie overeenkomen, maar gebruikmaken van verschillende Q\#-gegevens typen.

    - **Van:** Om consistentie te garanderen, mag deze voor positie **niet** worden gebruikt om type conversie functies of een ander geval waar **dat** van toepassing is, aan te geven.

    - ⛔️ **:** deze voor positie **mag niet** worden gebruikt, zodat Verwar ring met het gebruik als een werk woord in veel programmeer talen wordt voor komen.