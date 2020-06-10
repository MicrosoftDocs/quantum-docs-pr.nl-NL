---
title: 'Micro soft Q #-stijl gids'
description: "Meer informatie over de naamgeving, invoer, documentatie en opmaak conventies voor Q # Program ma's en bibliotheken."
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
ms.openlocfilehash: 948b385948f0b362e7c12500662132883959a798
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630234"
---
# <a name="q-style-guide"></a>Q #-stijl gids #
## <a name="general-conventions"></a>Algemene conventies ##

De conventies die in deze hand leiding worden voorgesteld, zijn bedoeld om Program ma's en bibliotheken die zijn geschreven in Q # gemakkelijker te kunnen lezen en begrijpen.

## <a name="guidance"></a>Hulp

Suggesties voor:

- Negeer nooit een Conventie, tenzij u dit opzettelijk doet om meer Lees bare en begrijpelijke code voor uw gebruikers te bieden.

## <a name="naming-conventions"></a>Naamgevings regels ##

Om de Quantum Development Kit te bieden, streven we naar functie-en bewerkings namen die verquantumt ontwikkel aars om Program ma's te schrijven die gemakkelijk te lezen zijn en die verrassingen minimaliseren.
Een belang rijk deel hiervan is dat wanneer we namen kiezen voor functies, bewerkingen en typen, de *woorden lijst* die programmeurs gebruiken om de Quantum concepten te Express, te bepalen. met onze keuzes kunnen we deze in hun inspanningen helpen om duidelijk te communiceren.
Dit is een verantwoordelijkheid voor ons om ervoor te zorgen dat de namen die we bieden, duidelijkheid geven in plaats van onduidelijkheid.
In deze sectie wordt beschreven hoe we voldoen aan deze verplichting in termen van expliciete richt lijnen die ons helpen bij het beste van de Q #-ontwikkel community.

### <a name="operations-and-functions"></a>Bewerkingen en functies ###

Een van de eerste dingen die een naam moet bepalen, is of een bepaald symbool een functie of een bewerking vertegenwoordigt.
Het verschil tussen functies en bewerkingen is van cruciaal belang om te weten hoe een code blok zich gedraagt.
Om het onderscheid tussen functies en bewerkingen voor gebruikers te communiceren, vertrouwen we op die Q # modellen Quantum bewerkingen door het gebruik van neven effecten.
Dat wil zeggen dat een bewerking iets *doet* .

Daarentegen beschrijven functies de wiskundige relaties tussen gegevens.
De expressie `Sin(PI() / 2.0)` *is* `1.0` en impliceert niets over de status van een programma of de qubits.

Samen vatting, bewerkingen doen zich voor in functies.
In dit onderscheid wordt gesuggereerd dat we bewerkingen als termen en functies als zelfstandig naam woord noemen.

> [!NOTE]
> Wanneer een door de gebruiker gedefinieerd type wordt gedeclareerd, wordt tegelijkertijd een nieuwe functie voor het maken van exemplaren van dat type gedefinieerd.
> Vanuit dat perspectief moeten door de gebruiker gedefinieerde typen worden benoemd als zelfstandig naam woord, zodat zowel het type zelf als de functie-constructor consistente namen hebben.

Als dat het geval is, moet u ervoor zorgen dat de naam van de bewerking begint met de termen die duidelijk aangeven wat het effect van de bewerking is.
Bijvoorbeeld:

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

Een voor beeld van een specifieke bewerking in de duur van het verdient wanneer een bewerking een andere handeling als invoer gebruikt en aanroept.
In dergelijke gevallen is de actie die door de invoer bewerking wordt uitgevoerd niet duidelijk wanneer de buitenste bewerking is gedefinieerd, zodat de juiste term niet onmiddellijk wordt gewist.
We raden u aan de term in te voeren, `Apply` zoals in `ApplyIf` , `ApplyToEach` en `ApplyToFirst` .
Andere woorden kunnen ook nuttig zijn in dit geval, zoals in `IterateThroughCartesianPower` .

| Verb | Verwacht effect |
| ---- | ------ |
| Toepassen | Een bewerking die is opgegeven als invoer, wordt aangeroepen |
| Assert | Een hypo these over het resultaat van een mogelijke quantum meting wordt gecontroleerd door een simulator |
| Schatting | Er wordt een klassieke waarde geretourneerd die een schatting vertegenwoordigt die uit een of meer metingen is getrokken |
| Measure | Er wordt een quantum meting uitgevoerd en het resultaat wordt geretourneerd aan de gebruiker |
| Voorbereiden | Een bepaald REGI ster van qubits wordt geïnitialiseerd in een bepaalde status |
| Voorbeeld | Er wordt een klassieke waarde geretourneerd op wille keurige wijze van distributie |

Voor-functies voor komt u dat het gebruik van woorden wordt voor komen voor veelvoorkomende naam woorden (Zie de richt lijnen voor de onderstaande juiste naam woorden) of bijvoeglijke naam woorden:

- `ConstantArray`
- `Head`
- `LookupFunction`

In nagenoeg alle gevallen raden we u aan om eerdere participles te gebruiken, waar dat nodig is om aan te geven dat een functie naam sterk is verbonden met een actie of een neven effect ergens anders in een Quantum programma.
`ControlledOnInt`Maakt bijvoorbeeld gebruik van de formulier participle van de term ' besturings element ' om aan te geven dat de functie fungeert als een bijvoeger om het argument te wijzigen.
Deze naam heeft een extra voor deel van het afstemmen van de semantiek van de ingebouwde `Controlled` functor, zoals hieronder wordt besproken.
Op dezelfde manier kunnen zelfstandige naam van _agents_ worden gebruikt om functie-en UDT-namen te maken op basis van bewerkings namen, zoals in het geval van de namen van `Encoder` een UDT die sterk is gekoppeld aan `Encode` .

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Termen gebruiken voor bewerkings namen.
- Gebruik naam woorden of bijvoegingen voor functie namen.
- Gebruik zelfstandige naam woorden voor door de gebruiker gedefinieerde typen en kenmerken.
- Gebruik voor alle aanroep bare namen een `CamelCase` sterke voor keur voor `pascalCase` , `snake_case` of `ANGRY_CASE` . Zorg er met name voor dat oproep bare namen beginnen met hoofd letters.
- Gebruik voor alle lokale variabelen een `pascalCase` sterke voor keur voor `CamelCase` , `snake_case` of `ANGRY_CASE` . Zorg er met name voor dat lokale variabelen beginnen met kleine letters.
- Vermijd het gebruik van onderstrepings tekens `_` in functie-en bewerkings namen; wanneer extra hiërarchie niveaus nodig zijn, gebruikt u naam ruimten en aliassen van naam ruimten.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

|   | Naam | Beschrijving |
|---|------|-------------|
| ☑ | `operation ReflectAboutStart` | Het gebruik van een term (' reflectie ') wissen om het effect van de bewerking aan te geven. |
| ☒ | <s>`operation XRotation`</s> | Het gebruik van de woord groep frase suggesties voor de functie, in plaats van de bewerking. |
| ☒ | <s>`operation search_oracle`</s> | Gebruik van de `snake_case` Contravenes Q #-notatie. |
| ☒ | <s>`operation Search_Oracle`</s> | Het gebruik van onderstrepings tekens intern voor de bewerkings naam contravenes Q #-notatie. |
| ☑ | `function StatePreparationOracle` | Als u een woord groep gebruikt, wordt gesuggereerd dat de functie een bewerking retourneert. |
| ☑ | `function EqualityFact` | Het gebruik van zelfstandig naam woord ("feit") wissen om aan te geven dat dit een functie is, terwijl de bijvoeger. |
| ☒ | <s>`function GetRotationAngles`</s> | Bij gebruik van term (' Get ') wordt voorgesteld dat dit een bewerking is. |
| ☑ | `newtype GeneratorTerm` | Het gebruik van de woord groep van een zelfstandig nummer verwijst duidelijk naar het resultaat van het aanroepen van de UDT-constructor. |
| ☒ | <s>`@Attribute() newtype RunOnce()`</s> | Het gebruik van een verbale woord groep adviseert dat de UDT-constructor een bewerking is. |
| ☑ | `@Attribute() newtype Deprecated(Reason : String)` | Gebruik van de woord groep met zelfstandig naam communicatie communiceert het gebruik van het kenmerk. |

***

### <a name="shorthand-and-abbreviations"></a>Steno en afkortingen ###

Het bovenstaande advies ondanks dat er sprake is van een groot aantal vormen van steno met een gemeen schappelijke en pervasive gebruik in de Quantum Computing.
We raden u aan bestaande en algemene steno te gebruiken waar deze zich bevinden, met name voor bewerkingen die intrinsiek zijn voor de werking van een doel machine.
We kiezen bijvoorbeeld de naam `X` in plaats van `ApplyX` en `Rz` in plaats van `RotateAboutZ` .
Bij het gebruik van deze steno moeten de namen van de bewerkingen allemaal hoofd letters zijn (bijvoorbeeld: `MAJ` ).

Bij het Toep assen van deze Conventie is een zorgvuldige toepassing vereist voor een vaak gebruikte acroniemen en initialisms zoals ' QFT ' voor ' Quantum Fourier Transform '.
We suggereren de volgende algemene .NET-conventies voor het gebruik van acroniemen en initialisms in volledige namen, waarbij u moet bepalen dat:

- afkortingen van twee letters en initialisms worden in hoofd letters genoemd (bijvoorbeeld: `BE` voor "big-endian"),
- alle langere acroniemen en initialisms worden genoemd in `CamelCase` (bijvoorbeeld: `Qft` voor "Quantum Fourier Transform")

Een bewerking die de QFT implementeert, kan dus worden aangeroepen `QFT` als steno of als uitgeschreven als `ApplyQft` .

Voor bijzonder gebruikte bewerkingen en functies kan het wenselijk zijn om een steno naam op te geven als _alias_ voor een langer formulier:

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Overweeg vaak geaccepteerde en veelgebruikte steno namen als dat nodig is.
- Gebruik hoofd letters voor Steno.
- Gebruik hoofd letters voor korte (twee letters) acroniemen en initialisms.
- Gebruik `CamelCase` voor meer (drie of meer letter) acroniemen en initialisms.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

|   | Naam | Beschrijving |
|---|------|-------------|
| ☑ | `X` | Goed te begrijpen steno voor ' een $X $ Transformation ' toep assen ' |
| ☑ | `CNOT` | Goed te begrijpen steno voor "Controlled-NOT" |
| ☒ | <s>`Cnot`</s> | Steno mag niet in zijn `CamelCase` . |
| ☑ | `ApplyQft` | Common Initiation "QFT" wordt weer gegeven als onderdeel van een lange formulier naam. |
| ☑ | `QFT` | Common Initiation "QFT" wordt weer gegeven als onderdeel van een steno naam. |



***


### <a name="proper-nouns-in-names"></a>Juiste naam woorden in namen ###

In het geval van een fysieke waarde is het gebruikelijk om dingen te benoemen na de eerste persoon die over hen publiceert. de meeste niet-physicists zijn niet bekend met de namen van iedereen en alle geschiedenis.
Het is te sterk om te voldoen aan de naamgevings conventies van de fysica, waardoor er een aanzienlijke barrière kan worden ingevoerd, omdat gebruikers van andere achtergronden een groot aantal schijnbaar ondoorzichtige namen moeten leren om veelvoorkomende bewerkingen en concepten te kunnen gebruiken.
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
Daarom is het raadzaam om, waar mogelijk, veelvoorkomende algemene naam woorden die een concept beschrijven, in hoge voor keur te worden aangenomen voor de juiste naam woorden die de publicatie geschiedenis van een concept beschrijven.
Een voor beeld hiervan is dat de afzonderlijk beheerde SWAP en de dubbele controle niet worden uitgevoerd, ook wel de Fredkin-en Toffoli-bewerkingen worden genoemd in academische literatuur, maar worden aangeduid met Q #, voornamelijk als `CSWAP` en `CCNOT` .
In beide gevallen bieden de API-documentatie opmerkingen synoniemen op basis van de juiste naam woorden, samen met alle relevante bron vermeldingen.

Deze voor keur is met name belang rijk, omdat het gebruik van de juiste zelfstandige naam woorden altijd nood zakelijk is. Q # volgt de traditie die is ingesteld door veel klassieke talen, bijvoorbeeld, en verwijst naar `Bool` typen in verwijzingen naar Boole-logica, die op zijn beurt wordt genoemd in respect van George Boole.
Enkele Quantum concepten worden op een vergelijk bare manier genoemd, met inbegrip van het `Pauli` type ingebouwd in de Q #-taal.
Door het gebruik van de juiste zelfstandige naam woorden, waarbij dit gebruik niet essentieel is, te minimaliseren, kunnen we de impact verminderen waarbij de juiste zelfstandige naam woorden niet redelijkerwijs worden vermeden.

# <a name="guidance"></a>[Hulp](#tab/guidance) 

Suggesties voor:

- Vermijd het gebruik van de juiste zelfstandige naam woorden in namen.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

***

### <a name="type-conversions"></a>Type conversies ###

Aangezien Q # een sterk en statisch getypte taal is, kan een waarde van één type alleen worden gebruikt als waarde van een ander type met behulp van een expliciete aanroep van een type conversie functie.
Dit is in tegens telling tot talen waarmee waarden typen impliciet kunnen worden gewijzigd (bijvoorbeeld: type promotie) of via casting.
Als gevolg hiervan spelen functies van het type conversie een belang rijke rol bij het ontwikkelen van Q #-bibliotheken en vormen ze een van de vaak voorkomende beslissingen over de naamgeving.
Maar omdat type conversies altijd _deterministisch_zijn, kunnen ze worden geschreven als functies en dus onder de bovenstaande aanbeveling vallen.
In het bijzonder raden we aan dat type conversie functies nooit moeten worden benoemd als woorden (bijvoorbeeld:) of voor voor keuren voor bewerkings `ConvertToX` parameters ( `ToX` ), maar moeten worden benoemd als voor zetsels van bijvoeglijke woord groepen die de bron-en doel typen ( `XAsY` ) aangeven.
Bij het weer geven van matrix typen in functie namen van type conversie, wordt de steno aangeraden `Arr` .
Als buitengewone omstandigheden worden geblokkeerd, raden we aan dat alle type conversie functies worden benoemd met `As` zodat ze snel kunnen worden geïdentificeerd.

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Als een functie een waarde van het type converteert `X` naar een waarde van `Y` het type, gebruikt u de naam `AsY` of `XAsY` .

# <a name="examples"></a>[Voorbeelden](#tab/examples)

|   | Naam | Beschrijving |
|---|------|-------------|
| ☒ | <s>`ToDouble`</s> | De voor positie ' to ' resulteert in een verbale woord groep, wat een bewerking aangeeft en niet een functie. |
| ☒ | <s>`AsDouble`</s> | Het invoer type is niet duidelijk uit de functie naam. |
| ☒ | <s>`PauliArrFromBoolArr`</s> | De invoer-en uitvoer typen worden in de verkeerde volg orde weer gegeven. |
| ☑ | `ResultArrAsBoolArr` | Zowel de invoer typen als de uitvoer typen zijn duidelijk. |

***

### <a name="private-or-internal-names"></a>Privé-of interne namen ###

In veel gevallen is een naam uitsluitend bedoeld voor intern gebruik in een bibliotheek of project en is dit geen gegarandeerd deel van de API die wordt aangeboden door een bibliotheek.
Het is handig om duidelijk aan te geven dat dit het geval is bij het benoemen van functies en bewerkingen, zodat onbedoelde afhankelijkheden op interne code duidelijk worden gemaakt.
Als een bewerking of functie niet bedoeld is voor direct gebruik, maar moet worden gebruikt door een overeenkomende aanroep die door een gedeeltelijke toepassing wordt uitgevoerd, kunt u overwegen een naam te gebruiken die begint met `_` voor de aanroep bare die gedeeltelijk is toegepast.

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Wanneer een functie, bewerking of door de gebruiker gedefinieerd type geen deel uitmaakt van de open bare API voor een Q #-bibliotheek of-programma, moet u ervoor zorgen dat de naam begint met een onderstrepings teken ( `_` ).

# <a name="examples"></a>[Voorbeelden](#tab/examples)

|   | Naam | Beschrijving |
|---|------|-------------|
| ☒ | <s>`ApplyDecomposedOperation_`</s> | Het onderstrepings teken `_` mag niet aan het einde van de naam worden weer gegeven. |
| ☑ | `_ApplyDecomposedOperation` | Het onderstrepings teken `_` aan het begin geeft duidelijk aan dat deze bewerking alleen voor intern gebruik is. |

***

### <a name="variants"></a>Qua ###

Hoewel deze beperking mogelijk niet persistent is in toekomstige versies van Q #, is het altijd zo dat er vaak groepen van gerelateerde bewerkingen of functies zijn die worden onderscheiden door welke functors hun invoer ondersteunen, of op basis van de concrete typen van de argumenten.
Deze groepen kunnen worden onderscheiden met dezelfde hoofd naam, gevolgd door een of twee letters die de variant aangeven.

| Achtervoegsel | Betekenis |
|--------|---------|
| `A` | Verwachte invoer wordt ondersteund`Adjoint` |
| `C` | Verwachte invoer wordt ondersteund`Controlled` |
| `CA` | Verwachte invoer voor ondersteuning `Controlled` en`Adjoint` |
| `I` | Invoer-of invoer waarden zijn van het type`Int` |
| `D` | Invoer-of invoer waarden zijn van het type`Double` |
| `L` | Invoer-of invoer waarden zijn van het type`BigInt` |

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Als een functie of bewerking niet is gerelateerd aan vergelijk bare functies of bewerkingen door de typen en functor-ondersteuning van de invoer, mag u geen achtervoegsel gebruiken.
- Als een functie of bewerking is gerelateerd aan vergelijk bare functies of bewerkingen door de typen en functor-ondersteuning van de invoer, gebruikt u achtervoegsels zoals in de bovenstaande tabel om varianten te onderscheiden.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

***

### <a name="arguments-and-variables"></a>Argumenten en variabelen ###

Een belang rijk doel van de Q #-code voor een functie of bewerking is dat deze eenvoudig kan worden gelezen en begrepen.
Op dezelfde manier moeten de namen van invoer-en type argumenten communiceren hoe een functie of argument wordt gebruikt wanneer dit wordt gegeven.


# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Gebruik voor alle variabele-en invoer namen een `pascalCase` sterke voor keur voor `CamelCase` , `snake_case` of `ANGRY_CASE` .
- De invoer namen moeten een beschrijvende naam hebben. Vermijd waar mogelijk een of twee letter namen.
- Bewerkingen en functies die precies één type argument accepteren, moeten dit type argument aangeven door `T` als de bijbehorende rol duidelijk is.
- Als een functie of bewerking meerdere type argumenten nodig heeft, of als de rol van een enkel type argument niet duidelijk is, overweeg dan het gebruik van een kort gepaard woord met als `T` voor beeld (bijvoorbeeld: `TOutput` ) voor elk type.
- Typ geen type namen in argument-en variabelenamen; deze informatie kan worden verstrekt door uw ontwikkel omgeving.
- Denoteer scalaire typen met hun letterlijke namen ( `flagQubit` ) en matrix typen met een meervoud ( `measResults` ).
  Voor matrices van qubits met name, overweeg om dergelijke typen te identificeren, `Register` waarbij de naam verwijst naar een reeks qubits die op een of andere manier nauw verwant zijn.
- Variabelen die als indexen worden gebruikt in matrices moeten beginnen met `idx` en moeten een enkelvoud zijn (bijvoorbeeld: `things[idxThing]` ).
  In het bijzonder Vermijd het gebruik van variabelen namen met één letter als indices. Overweeg `idx` ten minste te gebruiken.
- Variabelen die worden gebruikt om de lengte van matrices te bewaren, moeten beginnen met `n` en moeten worden gemeervoudt (bijvoorbeeld: `nThings` ).

# <a name="examples"></a>[Voorbeelden](#tab/examples)

***

### <a name="user-defined-type-named-items"></a>Door de gebruiker gedefinieerd type met de naam items ###

Benoemde items in door de gebruiker gedefinieerde typen moeten worden aangeduid als `CamelCase` , zelfs bij invoer naar UDT-constructors.
Dit helpt om de benoemde items duidelijk te scheiden van verwijzingen naar variabelen met een lokaal bereik wanneer u een accessor-notatie (bijvoorbeeld: `callable::Apply` ) of Copy-and-update notatie ( `set arr w/= Data <- newData` ) gebruikt.

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Benoemde items in UDT-constructors moeten worden benoemd als `CamelCase` ; dat wil zeggen dat ze beginnen met een eerste hoofd letter.
- Benoemde items die aan bewerkingen worden omgezet, moeten de naam werk woord fasen hebben.
- Benoemde items die niet naar bewerkingen worden omgezet, moeten een naam hebben als woord groepen.
- Voor UDTs die verloopt, moet een enkel benoemd item `Apply` worden gedefinieerd.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

|   | Codefragment | Beschrijving |
|---|---------|-------------|
| ☑ | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | De naam `Apply` is een `CamelCase` verbale woord groep waarmee wordt voorgesteld dat het benoemd item een bewerking is. |
| ☒ | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | Benoemde items moeten beginnen met een eerste hoofd letter. |
| ☒ | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | Benoemde items die worden omgezet in-functies, moeten worden benoemd als woord groepen, niet als verbale woord groepen. |

***

## <a name="input-conventions"></a>Invoer conventies ##

Wanneer een ontwikkelaar een bewerking of functie aanroept, moeten de verschillende invoer waarden voor die bewerking of functie worden opgegeven in een bepaalde volg orde, waardoor de cognitieve belasting die een ontwikkelaar gemerkt, wordt gebruikt om een bibliotheek te gebruiken.
Met name de taak van het onthouden van invoer orders is vaak een afleiding van de taak bij de hand: het Program meren van een implementatie van een Quantum algoritme.
Hoewel uitgebreide ondersteuning voor IDE dit in grote mate kan beperken, kan een goed ontwerp en de gang bare conventies ook helpen om de cognitieve belasting van een API te minimaliseren.

Waar mogelijk kan het nuttig zijn om het aantal ingevoerde invoer waarden te verminderen dat wordt verwacht door een bewerking of functie, zodat de rol van elke invoer onmiddellijk duidelijker is voor ontwikkel aars die de bewerking of functie aanroepen, en naar ontwikkel aars die code later lezen.
Met name wanneer het niet mogelijk is om het aantal argumenten voor een bewerking of functie te verminderen, is het belang rijk om een consistente volg orde te hebben die het voors pellen van de gebruiker bij de voor spelling van de invoer verkleint.

We raden u aan om de conventies voor invoer volgorde in te stellen die grotendeels afleiden van een deel van de toepassing als generalisatie van currying f (x, y) ≡ f (x) (y).
Het Toep assen van de eerste argumenten zou dus gedeeltelijk van toepassing moeten zijn en die nuttig is voor eigen rechts, wanneer dat redelijk is.
U kunt de volgende volg orde van argumenten gebruiken om dit principe te volgen:

- Klassieke niet-aanroep bare argumenten, zoals hoeken, vectoren van bevoegdheden, enzovoort.
- Aanroep bare argumenten (functies en argumenten).
  Als beide functies en bewerkingen worden uitgevoerd als argumenten, kunt u de bewerkingen na functies plaatsen.
- Verzamelingen die worden uitgevoerd door aanroep bare argumenten op soort gelijke wijze als,, en `Map` `Iter` `Enumerate` `Fold` .
- Qubit argumenten gebruikt als besturings elementen.
- Qubit argumenten die als doelen worden gebruikt.

Houd rekening met een bewerking `ApplyPhaseEstimationIteration` voor het gebruik in de fase-schatting die een hoek en een Oracle afneemt, de hoek door gegeven aan `Rz` een matrix met verschillende schaal factoren en vervolgens de toepassingen van de Oracle beheert.
De invoer wordt op `ApplyPhaseEstimationIteration` de volgende manier gerangschikt:

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
Als een speciaal geval van het minimaliseren van de verrassingen, simuleren sommige functies en bewerkingen het gedrag van de ingebouwde functors `Adjoint` en `Controlled` .
Bijvoorbeeld, `ControlledOnInt<'T>` is van `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` het type, bijvoorbeeld `ControlledOnInt<Qubit[]>(5, _)` de `Controlled` functor, maar op voor waarde dat het controle register de status $ \ket {5} = \ket {101} $ vertegenwoordigt.
Daarom verwacht een ontwikkelaar dat de invoer de `ControlledOnInt` aanroep zou plaatsen die het laatst is getransformeerd en dat de resulterende bewerking de invoer `(Qubit[], 'T)` ---dezelfde volg orde uitvoert, gevolgd door de uitvoer van de `Controlled` functor.

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Gebruik invoer volgorden die consistent zijn met het gebruik van een gedeeltelijke toepassing.
- Gebruik invoer volgorden die consistent zijn met ingebouwde functors.
- Plaats alle klassieke invoer vóór een Quantum invoer.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

***

## <a name="documentation-conventions"></a>Documentatie conventies ##

De Q #-taal maakt het mogelijk om documentatie toe te voegen aan bewerkingen, functies en door de gebruiker gedefinieerde typen door het gebruik van speciaal opgemaakte documentatie opmerkingen.
Deze documentatie opmerkingen worden aangeduid met drievoudige slashes ( `///` ) en zijn kleine [DocFX-geprijsde](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documenten die kunnen worden gebruikt voor het beschrijven van het doel van elke bewerking, functie en door de gebruiker gedefinieerd type, welke invoer elk verwacht, enzovoort.
De compiler die wordt geleverd met de Quantum Development Kit, haalt deze opmerkingen op en gebruikt deze om de typen documentatie op te geven die vergelijkbaar is met die in https://docs.microsoft.com/quantum .
Op dezelfde manier gebruikt de taal server van de Quantum Development Kit deze opmerkingen om gebruikers te helpen bij het aanwijzen van de muis aanwijzer over symbolen in hun Q #-code.
Het gebruik van documentatie opmerkingen kan gebruikers helpen om code te maken met behulp van een nuttige referentie voor informatie die niet eenvoudig kan worden weer gegeven met de andere conventies in dit document.

<div class="nextstepaction">
    [Naslag informatie over de syntaxis van documentatie](xref:microsoft.quantum.guide.filestructure#documentation-comments)
</div>

Als u deze functionaliteit effectief wilt gebruiken om gebruikers te helpen, raden we u aan om een aantal zaken te houden wanneer u documentatie opmerkingen schrijft.

# <a name="guidance"></a>[Hulp](#tab/guidance)

Suggesties voor:

- Elke open bare functie, bewerking en door de gebruiker gedefinieerd type moeten onmiddellijk worden voorafgegaan door een documentatie opmerking.
- Elke documentatie opmerking moet mini maal de volgende secties bevatten:
    - Samenvatting
    - Invoer
    - Uitvoer (indien van toepassing)
- Zorg ervoor dat alle samen vattingen twee zinnen of minder zijn. Als er meer ruimte nodig is, geeft u een `# Description` sectie op die direct volgt `# Summary` met de volledige informatie.
- Als dat niet het geval is, kunt u geen wiskundige formules in samen vattingen gebruiken, omdat niet alle clients TeX-notatie in samen vattingen ondersteunen. Houd er rekening mee dat bij het schrijven van Prose-documenten (bijvoorbeeld TeX of prijs verlaging) het voor keur is dat er langere lijn lengten worden gebruikt.
- Geef alle relevante wiskundige expressies op in de `# Description` sectie.
- Herhaal bij het beschrijven van invoer de typen van elke invoer niet, aangezien deze kunnen worden afgeleid door de compiler en het risico dat inconsistentie wordt geïntroduceerd.
- Geef voor beelden op die van toepassing zijn, elk in hun eigen `# Example` sectie.
- Geef een korte beschrijving van elk voor beeld voordat u code vermeldt.
- Vermeld alle relevante academische publicaties (bijvoorbeeld: papers, procedures, blog berichten en alternatieve implementaties) in een `# References` sectie als een lijst met opsommings tekens van koppelingen.
- Zorg ervoor dat alle bron vermelding-koppelingen, waar mogelijk, permanent en onveranderbare id's (DOIs of genummerde arXiv) zijn.
- Wanneer een bewerking of functie is gerelateerd aan andere bewerkingen of functies van functor varianten, vermeldt u andere varianten als opsommings tekens in de `# See Also` sectie.
- Laat een lege opmerkings regel tussen de secties Level-1 ( `/// #` ), maar laat geen lege regel tussen de secties Level-2 ( `/// ##` ) staan.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

#### <a name=""></a>☑ ####

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

## <a name="formatting-conventions"></a>Opmaak conventies ##

Naast de voor gaande suggesties is het handig om code zo leesbaar mogelijk te maken voor het gebruik van consistente opmaak regels.
Dergelijke opmaak regels worden op een wille keurige manier en in het algemeen op persoonlijke wijze in het gepaareerd.
Het is echter raadzaam een consistente set opmaak conventies binnen een groep mede werkers te onderhouden, met name voor grote Q #-projecten, zoals de Quantum Development Kit zelf.
Deze regels kunnen automatisch worden toegepast met behulp van het opmaak programma dat is geïntegreerd met de compiler Q #.

# <a name="guidance"></a>[Hulp](#tab/guidance) 

Suggesties voor:

- Gebruik vier spaties in plaats van tabs voor portabiliteit.
  Bijvoorbeeld in VS code:
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- Regel terugloop om 79 tekens waar redelijk.
- Gebruik spaties om binaire Opera tors.
- Gebruik spaties aan beide zijden van de dubbele punten die worden gebruikt voor type annotaties.
- Gebruik één spatie na komma's die worden gebruikt in matrix-en tuple-letterlijke waarden (bijvoorbeeld: in ingangen naar functies en bewerkingen).
- Gebruik geen spaties na functie, bewerking of UDT-namen, of na de `@` in-kenmerk declaraties.
- Elke kenmerk declaratie moet op een eigen regel staan.

# <a name="examples"></a>[Voorbeelden](#tab/examples)

|   | Codefragment | Beschrijving |
|---|---------|-------------|
| ☒ | <s>`2+3`</s> | Gebruik spaties om binaire Opera tors. |
| ☒ | <s>`target:Qubit`</s> | Gebruik spaties rondom type aantekening. |
| ☑ | `Example(a, b, c)` | De items in de invoer-tuple zijn op de juiste wijze voor de Lees baarheid. |
| ☒ | <s>`Example (a, b, c)`</s> | Spaties moeten worden onderdrukt na functie-, bewerking-of UDT-namen. |

***

