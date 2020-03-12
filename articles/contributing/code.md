---
title: Code bijdragen aan de micro soft-QDK
description: Meer informatie over het bijdragen van voorbeeld-en bibliotheek code aan de Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
ms.openlocfilehash: edc52dc4434e91258bece28812fd76b66329c6f9
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022459"
---
# <a name="contributing-code"></a>Code bijdragen

Naast het melden van problemen en het verbeteren van documentatie, kan bijdragen aan code in de Quantum Development Kit een zeer directe manier zijn om uw collega's in de Quantum-programmeer community te helpen.
Door code te leveren, kunt u problemen oplossen, nieuwe voor beelden bieden, bestaande bibliotheken eenvoudiger te gebruiken of zelfs volledig nieuwe functies toevoegen.

In deze hand leiding wordt een overzicht gegeven van wat er wordt gezocht wanneer we pull-aanvragen bekijken om uw bijdrage te helpen het meest geschikt te maken.

## <a name="what-we-look-for"></a>Wat we zoeken

Een ideale code bijdrage bouwt voort op de bestaande werkzaamheden in een Quantum Development Kit-opslag plaats om problemen op te lossen, bestaande functies uit te breiden of nieuwe functies toe te voegen die binnen het bereik van een opslag plaats vallen.
Wanneer we een code bijdrage accepteren, wordt het een deel van de Quantum Development Kit zelf, zodat nieuwe functies worden vrijgegeven, onderhouden en ontwikkeld op dezelfde manier als de rest van de Quantum Development Kit.
Het is dus handig wanneer de functionaliteit die door een bijdrage wordt toegevoegd, goed is getest en is gedocumenteerd.

### <a name="unit-tests"></a>Eenheids tests

De Q #-functies,-bewerkingen en door de gebruiker gedefinieerde typen waaruit bibliotheken bestaan, zoals de Canon, worden automatisch getest als onderdeel van de ontwikkeling van de [**micro soft/QuantumLibraries-** ](https://github.com/Microsoft/QuantumLibraries/) opslag plaats.
Wanneer er een nieuwe pull-aanvraag wordt geopend, bijvoorbeeld de configuratie van [Azure-pijp lijnen](https://azure.microsoft.com/services/devops/pipelines/) , wordt gecontroleerd of de wijzigingen in de pull-aanvraag geen invloed hebben op de bestaande functionaliteit waarvan de Quantum-programmeer Community afhankelijk is.

Met de meest recente Q #-versie wordt de eenheids test gedefinieerd met behulp van het kenmerk `@Test("QuantumSimulator")`. Het argument kan "QuantumSimulator", "ToffoliSimulator", "TraceSimulator" of een volledig gekwalificeerde naam zijn die het uitvoerings doel opgeeft. Verschillende kenmerken die verschillende uitvoerings doelen definiëren, kunnen worden gekoppeld aan dezelfde aanroepable. Sommige van onze tests maken nog steeds gebruik van het afgeschafte [micro soft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) -pakket dat alle Q #-functies en-bewerkingen bevat die eindigen op `Test` naar het [xUnit](https://xunit.github.io/) -Framework. Dit pakket is niet meer nodig om de eenheids tests te definiëren. 

De volgende functie wordt gebruikt om ervoor te zorgen dat de functies <xref:microsoft.quantum.canon.fst> en <xref:microsoft.quantum.canon.snd> beide de juiste uitvoer in een representatief voor beeld retour neren.
Als de uitvoer van `Fst` of `Snd` onjuist is, wordt de instructie `fail` gebruikt om te zorgen dat de test mislukt.

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

Complexere voor waarden kunnen worden gecontroleerd met behulp van de technieken in het [gedeelte testen](xref:microsoft.quantum.libraries.diagnostics) van de hand leiding standaard bibliotheken.
Zo controleert de volgende test of `H(q); X(q); H(q);` zoals aangeroepen door <xref:microsoft.quantum.canon.applywith> hetzelfde is als `Z(q)`.

```Q#
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

Bij het toevoegen van nieuwe functies is het een goed idee om ook nieuwe tests toe te voegen, zodat u zeker weet dat uw bijdrage de bedoeling is.
Dit helpt de rest van de community om uw functie te onderhouden en te ontwikkelen, met name om andere ontwikkel aars te helpen weten dat ze op uw functie kunnen vertrouwen.

> [!NOTE]
> Dit werkt op de andere manier.
> Als er sprake is van een bestaande functie waarvoor bepaalde tests ontbreken, helpt we bij het toevoegen van test dekking een uitstekende bijdrage aan de community.

Lokale tests kunnen worden uitgevoerd met behulp van Visual Studio test Explorer of de `dotnet test` opdracht, zodat u uw bijdrage kunt controleren voordat u een pull-aanvraag opent.

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->


## <a name="when-well-reject-a-pull-request"></a>Wanneer we een pull-aanvraag afwijzen

Soms wordt de pull-aanvraag voor een bijdrage geweigerd.
Als dit het geval is, betekent dit niet dat het defect is, omdat er een aantal redenen zijn waarom we een bepaalde bijdrage mogelijk niet kunnen accepteren.
Mogelijk is een bijdrage aan de Quantum-programmeer Community heel goed, maar de Quantum Development Kit-opslag plaatsen zijn niet de juiste plaats om deze te ontwikkelen.
In dergelijke gevallen raden wij u ten zeerste aan om uw eigen opslag plaats---deel van de sterkte van de Quantum Development Kit te maken, waarmee u eenvoudig uw eigen bibliotheken kunt maken en distribueren met GitHub en NuGet.org, op dezelfde manier als we de Canon en chemie distribueren Bibliotheken vandaag.

Op andere momenten kunnen we een goede bijdrage afwijzen, omdat we nog niet klaar zijn om deze te onderhouden en te ontwikkelen.
Het kan lastig zijn om alles te doen, dus we plannen welke functies u het beste kunt gebruiken als een route kaart.
Dit kan een andere situatie zijn waarbij het loslaten van een functie als een bibliotheek van derden een hoop idee kan maken.
Het is ook mogelijk om uw hulp te vragen bij het wijzigen van een functie zodat deze beter past in onze route kaart, zodat we het beste werk kunnen doen.

We vragen u ook om wijzigingen in een pull-aanvraag als er meer documentatie of eenheids tests nodig zijn om ons te helpen hun gebruik te maken, of als de stijl van de rest van de Q #-bibliotheken zo veel verschilt dat het voor gebruikers moeilijker wordt om uw functie te vinden.
In deze gevallen proberen we een aantal adviezen te geven over wat er kan worden toegevoegd of gewijzigd om uw bijdrage voor ons gemakkelijker te maken.

Ten slotte kunnen we geen bijdragen accepteren die schade aanrichten aan de quantum computer Community, zoals beschreven in de [micro soft open source-gedrags code](https://opensource.microsoft.com/codeofconduct/).
We willen er zeker van zijn dat de bijdragen van toepassing zijn op de volledige quantum computer-Community, zowel in de huidige fantastische diversiteit als in de toekomst, naarmate deze nog steeds groter wordt.
Bedankt voor uw hulp bij het realiseren van dit doel.

## <a name="next-steps"></a>Volgende stappen

Hartelijk dank dat u de Quantum Development Kit een fantastische resource wilt maken voor de hele Quantum-programmeer community.
Ga voor meer informatie naar de volgende hand leiding over Q # style.

> [!div class="nextstepaction"]
> [Meer informatie over Q # Style-richt lijnen](xref:microsoft.quantum.contributing.style)

Afhankelijk van wat voor soort code u bijdraagt, zijn er mogelijk extra zaken die u kunnen helpen om uw bijdrage zo goed mogelijk voor de community te laten doen.

> [!div class="nextstepaction"]
> [Meer informatie over bijdragende voor beelden](xref:microsoft.quantum.contributing.samples)
