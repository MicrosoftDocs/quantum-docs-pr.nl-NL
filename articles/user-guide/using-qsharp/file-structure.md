---
title: 'Q # bestands structuur'
description: 'Hierin worden de structuur en syntaxis van een Q #-bestand beschreven.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: cbee92c6d7e765237a7a42532dd7012b51421708
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430965"
---
# <a name="q-file-structure"></a>Q # bestands structuur

Elke Q #-bewerking,-functie en een door de gebruiker gedefinieerd type worden binnen een naam ruimte gedefinieerd.

Een Q #-bestand bestaat uit een reeks *naam ruimte declaraties*.
Elke naam ruimte declaratie bevat declaraties voor door de gebruiker gedefinieerde typen, bewerkingen en functies.
Een naam ruimte declaratie kan elk wille keurig aantal van elk type declaratie en in een wille keurige volg orde bevatten.
Volg deze koppelingen voor meer informatie over het declareren van door de [gebruiker gedefinieerde typen](xref:microsoft.quantum.guide.types#user-defined-types), [bewerkingen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)en [functies](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) binnen een naam ruimte.

De enige tekst die buiten een naam ruimte declaratie kan worden weer gegeven, is opmerkingen.
In het bijzonder worden documentatie opmerkingen (meer details hieronder) voor een naam ruimte voorafgaat aan de declaratie.

## <a name="namespace-declarations"></a>Naam ruimte declaraties

Een Q #-bestand heeft normaal gesp roken precies één naam ruimte declaratie, maar kan geen hebben (en mag niet leeg zijn of alleen opmerkingen bevatten) of kan meerdere naam ruimten bevatten.
Naam ruimte declaraties mogen niet worden genest.

Dezelfde naam ruimte kan worden gedeclareerd in meerdere Q #-bestanden die samen worden gecompileerd, zolang er geen type, bewerking of functie declaraties met dezelfde naam zijn.
Het is met name ongeldig om hetzelfde type in dezelfde naam ruimte in meerdere bestanden te definiëren, zelfs als de declaraties identiek zijn.

Een naam ruimte declaratie bestaat uit het tref woord `namespace` , gevolgd door de naam van de naam ruimte, een open accolade `{` , de declaraties in de naam ruimte en een sluitings accolade `}` .
Naam ruimte namen volgen het .NET-patroon van een reeks van een of meer juridische symbolen, gescheiden door punten `.` .
`MyQuantumStuff`En `Microsoft.Quantum.Intrinsic` zijn bijvoorbeeld geldige naam ruimte namen.
Per Conventie worden de symbolen in de naam van een naam ruimte gekapitaliseerd, maar dit is niet vereist.

Verwijzingen naar typen of callables die verder in een bestand worden aangegeven, worden op de juiste wijze opgelost. het is niet nodig om een verwijzing naar het type, de bewerking of de functie te gebruiken.

## <a name="open-directives"></a>Open instructies

Binnen een naam ruimte blok `open` kan de instructie worden gebruikt voor het importeren van alle typen en callables die zijn gedeclareerd in een bepaalde naam ruimte en deze te raadplegen op basis van de niet-gekwalificeerde naam.
Een dergelijke `open` richt lijn bestaat uit het `open` tref woord, gevolgd door de naam ruimte die moet worden geopend en een punt komma als scheidings tekens.

> [!NOTE] 
> Alle `open` instructies moeten voor alle `function` , `operation` of `newtype` declaraties in het naam ruimte blok worden weer gegeven.

Een korte naam voor de naam ruimte kan eventueel worden gedefinieerd, zodat alle elementen van die naam ruimte kunnen (en moeten) worden gekwalificeerd door de gedefinieerde korte naam. Als u bijvoorbeeld de volgende naam ruimte declaratie en open instructies hebt opgegeven,

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

Als voor een bewerking die we declareren een bewerking wordt gebruikt `Op` `Microsoft.Quantum.Intrinsic` , wordt deze aangeroepen door eenvoudigweg te gebruiken `Op` .
Als we echter een bepaalde functie willen aanroepen `Fn` vanuit `Microsoft.Quantum.Math` , moeten we deze aanroepen met `Math.Fn` .

De `open` instructie is van toepassing op het volledige naam ruimte blok binnen een bestand.
Als we een extra naam ruimte in hetzelfde Q #-bestand als hierboven hadden gedefinieerd `NS` , hebben alle bewerkingen/functies/typen die zijn gedefinieerd in de tweede naam ruimte, geen toegang tot niets van `Microsoft.Quantum.Intrinsic` of `Microsoft.Quantum.Math` , tenzij we de open instructies daarin hebben herhaald. 

Er moet naar een type of aanroepbaar worden gedefinieerd in een andere naam ruimte die *niet* in de huidige naam ruimte wordt geopend, met de volledig gekwalificeerde naam.
Bijvoorbeeld: er `Op` moet naar een bewerking met de naam van de `X.Y` naam ruimte worden verwezen met de volledig gekwalificeerde naam `X.Y.Op` , tenzij de `X.Y` naam ruimte eerder in het huidige blok is geopend. Zoals eerder vermeld, `X` is het niet mogelijk om te verwijzen naar de bewerking, zelfs als de naam ruimte is geopend `Y.Op` .
Als er een korte naam `Z` voor `X.Y` is gedefinieerd in die naam ruimte en het bestand, `Op` moet worden aangeduid als `Z.Op` . 

Het is doorgaans beter om een naam ruimte op te neemen met behulp van een `open` instructie.
Het gebruik van een volledig gekwalificeerde naam is vereist als twee naam ruimten constructies met dezelfde naam definiëren. voor de huidige bron worden constructies van beide gebruikt.

Q # volgt dezelfde regels als voor naam als andere .NET-talen.
Q # biedt echter geen ondersteuning voor relatieve verwijzingen naar naam ruimten.
Als de naam ruimte is `a.b` geopend, wordt een verwijzing naar een bewerking met de naam `c.d` *niet* omgezet naar een bewerking met een volledige naam `a.b.c.d` .

## <a name="formatting"></a>Opmaak

De meeste Q #-instructies en de instructies eindigen met een punt komma, `;` .
Instructies en declaraties, zoals `for` en `operation` die eindigen op een instructie blok (zie hieronder), vereisen geen afsluitende punt komma.
Elke instructie bevat een beschrijving van de vraag of de afsluit punt komma is vereist.

Instructies, zoals expressies, declaraties en instructies, kunnen worden verdeeld over meerdere regels.
Meerdere instructies op één regel moeten worden vermeden.

## <a name="statement-blocks"></a>Instructie blokken

Q #-instructies worden gegroepeerd in instructie blokken.
Een instructie blok begint met het openen `{` en eindigen met een afsluiting `}` .

Een overzichts blok dat is inge sloten in een ander blok, wordt beschouwd als een subblok van het container blok; contains-en sub-blokken worden ook outer-en Inner-blokken genoemd.

## <a name="comments"></a>Opmerkingen

Opmerkingen beginnen met twee slashes `//` en door gaan tot het einde van de regel.
Een opmerking kan ergens in een Q #-bron bestand worden weer gegeven.

## <a name="documentation-comments"></a>Documentatie opmerkingen

Opmerkingen die beginnen met drie slashes, `///` worden speciaal door de compiler behandeld wanneer ze direct vóór een naam ruimte, bewerking, specialisatie, functie of type definitie worden weer gegeven.
In dat geval wordt de inhoud ervan als documentatie voor het gedefinieerde aanroepende of door de gebruiker gedefinieerde type beschouwd, net als bij andere .NET-talen.

Binnen `///` opmerkingen wordt tekst die als onderdeel van de API-documentatie moet worden weer gegeven, opgemaakt als een [prijs](https://daringfireball.net/projects/markdown/syntax)opgave, waarbij verschillende delen van de documentatie worden aangegeven door een speciaal benoemde koptekst.
Als uitbrei ding om te kunnen worden genoteerd, kunnen kruis verwijzingen naar bewerkingen, functies en door de gebruiker gedefinieerde typen in Q # worden opgenomen met behulp `@"<ref target>"` van de, waar `<ref target>` wordt vervangen door de volledig gekwalificeerde naam van het code object waarnaar wordt verwezen.
Een documentatie-engine kan eventueel ook extra kortings uitbreidingen ondersteunen.

Bijvoorbeeld:

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

De volgende namen worden herkend als documentatie opmerkings koppen.

- **Samen vatting**: een korte samen vatting van het gedrag van een functie of bewerking, of van het doel van een type. De eerste alinea van de samen vatting wordt gebruikt voor het aanwijzen van informatie. Dit moet tekst zonder opmaak zijn.
- **Beschrijving**: een beschrijving van het gedrag van een functie of bewerking, of van het doel van een type. De samen vatting en beschrijving worden samengevoegd om het gegenereerde documentatie bestand te vormen voor de functie, bewerking of het type.
  De beschrijving mag in-line-symbolen en-vergelijkingen in LaTeX-indeling bevatten.
- **Invoer**: een beschrijving van de invoer-tuple voor een bewerking of functie.
  Kan aanvullende subsecties van de korting bevatten die elk afzonderlijk element van de invoer-tuple aangeven.
- **Output**: een beschrijving van de tuple die wordt geretourneerd door een bewerking of functie.
- **Type parameters**: een lege sectie die één extra subsectie bevat voor elke algemene type parameter.
- **Voor beeld**: een kort voor beeld van het gebruik van de bewerking, functie of het type.
- **Opmerkingen**: diverse Prose die een aspect van de bewerking, functie of type beschrijven.
- **Zie ook**: een lijst met volledig gekwalificeerde namen die betrekking hebben op gerelateerde functies, bewerkingen of door de gebruiker gedefinieerde typen.
- **Verwijzingen**: een lijst met verwijzingen en bron vermeldingen voor het item dat wordt gedocumenteerd.

## <a name="whats-next"></a>Hoe nu verder?
Meer informatie over [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions) in Q #.