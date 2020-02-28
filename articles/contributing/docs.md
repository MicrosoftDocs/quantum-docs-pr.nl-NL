---
title: Documentatie over micro soft QDK
description: Meer informatie over het bijdragen van conceptuele of API-inhoud aan de micro soft Quantum documentation set.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
ms.openlocfilehash: d244a7841b4093031d6225230a6cbefb22cc6a39
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904890"
---
# <a name="improving-documentation"></a>Documentatie verbeteren #

De documentatie voor de Quantum Development Kit gaat over verschillende formulieren, waardoor de informatie gemakkelijk beschikbaar is voor Quantum ontwikkelaars.

Aan de hand van de beginselen van [documenten als code](https://www.writethedocs.org/guide/docs-as-code/)is alle Quantum Development Kit-documentatie ingedeeld als code en wordt beheerd met behulp van Git op dezelfde manier als de bron code die wordt gebruikt om de Quantum Development Kit te bouwen.
In het algemeen is de code-documentatie voor het terugzetten van verschillende vormen van [prijs verlaging](https://daringfireball.net/projects/markdown/), een taal voor het schrijven van RTF-tekst in een onbewerkte tekst indeling die eenvoudig te gebruiken is op de opdracht regel, in ide's en met broncode beheer.
We gaan de [MathJax](https://www.mathjax.org/) -bibliotheek op dezelfde manier gebruiken voor het opmaken van wiskunde in documentatie met behulp van de latex-taal, zoals hieronder beschreven.


Dit betekent dat elke vorm van documentatie enigszins in de details kan verschillen:

- De **conceptuele documentatie** bestaat uit een set artikelen die worden gepubliceerd op https://docs.microsoft.com/quantumen die alles beschrijft uit de basis beginselen van Quantum Computing tot de technische specificaties voor Interchange-indelingen. Deze artikelen worden geschreven in [DocFXe prijs verlaging (dfm)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), een afkortings variant die wordt gebruikt voor het maken van uitgebreide documentatie sets.
- De **API-verwijzing** is een set pagina's voor elke Q #-functie,-bewerking en door de gebruiker gedefinieerd type, gepubliceerd op https://docs.microsoft.com/qsharp/api/. Deze pagina's documenteren de invoer en bewerkingen van elke aanroep, samen met voor beelden en koppelingen naar meer informatie. De API-verwijzing wordt automatisch geëxtraheerd uit kleine DFM-documenten in Q #-bron code als onderdeel van elke release.
- De **Leesmij-bestanden<!---->. MD** die zijn opgenomen in elk voor beeld en Kata beschrijven hoe u dit voor beeld of Kata gebruikt, wat het dekt en hoe het werkt met de rest van de Quantum Development Kit. Deze bestanden worden geschreven met behulp van github geringte [prijs verlaging (GFM)](https://github.github.com/gfm/), een licht gewicht alternatief voor dfm dat populair is voor het rechtstreeks koppelen van documentatie aan code opslagplaatsen.

## <a name="contributing-to-the-conceptual-documentation"></a>Bijdragen aan de conceptuele documentatie ##

Voor een verbetering van de conceptuele of leesmij-documentatie, begint met een pull-aanvraag op [**MicrosoftDocs/Quantum-docs-PR**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**micro soft/Quantum**](https://github.com/Microsoft/Quantum)of [**micro soft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas), zoals van toepassing.
Hieronder vindt u meer informatie over pull-aanvragen. er is nu een paar dingen die u in aanmerking kunt nemen bij het verbeteren van de documentatie:

- Lezers worden door de Quantum Development Kit-documentatie van een breed scala aan achtergronden geleverd. Iedereen van hoge school studenten die meer willen weten over een nieuwe en interessante tenurede faculteit bij het uitvoeren van het gebruik van Quantum Computing, moeten in staat zijn om de documentatie te lezen. Als dat mogelijk is, neemt u geen uitgebreide kennis op over het deel van uw lezers, aangezien ze alleen kunnen worden gestart. Het is handig als u duidelijke en toegankelijke beschrijvingen kunt opgeven, of als u koppelingen naar andere bronnen kunt opgeven voor meer informatie.
- Het is niet mogelijk om documentatie sets op te stellen als boeken of documenten, in die lezers die in de ' middle ' lijken te komen. Zoek machines maken bijvoorbeeld mogelijk geen suggesties voor de index of ze hebben mogelijk een koppeling verzonden door een vriend om hen te helpen. Probeer uw lezer te helpen door altijd een duidelijke context te geven, samen met koppelingen waar dat van toepassing is.
- Sommige lezers vinden de meest nuttige samen vattingen en definities, terwijl andere lezers het meest geschikt zijn voor het extrapoleren van concrete voor beelden. Door zowel het algemene als het specifieke voor beeld te bieden, kunnen beide lezers optimaal profiteren van Quantum programmering.
- Met name als u de code die wordt gedocumenteerd ook hebt geschreven, zijn de dingen mogelijk duidelijk voor uw lezers. Er is geen unieke beste manier om Program ma's aan te bieden, dus het is niet mogelijk om te zien welke ontwerp patronen u hebt gevonden en wat u het nuttigst vindt om uw ideeën in code uit te drukken. Het is duidelijk om te zien hoe een lezer het gebruik van uw code kan verwachten door deze context te gebruiken.
- Veel leden van de Quantum-programmeer Community zijn academische onderzoekers en worden voornamelijk door middel van citaten voor hun bijdragen aan de Community herkend. U kunt niet alleen lezers helpen om aanvullende materialen te vinden, maar ook om academische uitvoer, zoals papers, besprekingen, blog berichten en software tools te vermelden, kunnen academische mede werkers helpen om de beste werkzaamheden te blijven uitvoeren om de community te verbeteren.
- De Quantum-programmeer Community is een brede en veelzijdige community. Het gebruik van geslachte promaakte in voor beelden van derden (bijvoorbeeld: "als een gebruiker..., hij...) kan worden gebruikt om uit te sluiten in plaats van op te nemen. Het Cognizant van de namen van mensen in citaten en koppelingen, en van de juiste insluiting van niet-ASCII-tekens, kan de diversiteit van de Community opleveren door de leden van de Gemeenschap te laten zien. Evenzo worden veel woorden in de Engelse taal vaak op een hatefule manier gebruikt, zodat het gebruik ervan in technische documentatie kan leiden tot beschadiging van zowel individuele lezers als de community.

## <a name="contributing-to-the-api-references"></a>Bijdragen aan de API-verwijzingen ##

Om een verbetering van de API-verwijzingen bij te dragen, is het handig om een pull-aanvraag rechtstreeks te openen in de code die wordt gedocumenteerd.
Elke functie, bewerking of door de gebruiker gedefinieerd type ondersteunt een documentatie opmerking (aangeduid met `///` in plaats van `//`).
Wanneer we elke release van de Quantum Development Kit compileren, worden deze opmerkingen gebruikt voor het genereren van de API-verwijzing op https://docs.microsoft.com/qsharp/api/, met inbegrip van gegevens over de invoer van en uitvoer van elke aanroep bare, de veronderstellingen die elk aanroepbaar zijn, en voor beelden van het gebruik ervan.

> [!IMPORTANT]
> Zorg ervoor dat u de gegenereerde API-documentatie niet hand matig bewerkt, omdat deze bestanden worden overschreven door elke nieuwe release.
> We stellen uw bijdrage aan de community op prijs en willen er zeker van zijn dat uw wijzigingen blijven bijdragen aan de release van gebruikers na de release.

Neem bijvoorbeeld de functie `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.
Een documentatie opmerking moet een gebruiker helpen informatie te lezen over het interpreteren van `bits` en `oracle` en waarvoor de functie is.
Elk van deze verschillende informatie kan worden verstrekt aan de sectie Q # van een speciaal benoemde prijs opgave in de documentatie opmerking.
Voor het voor beeld van `ControlledOnBitString`kunnen we een van de volgende zaken schrijven:

```qsharp
 /// # Summary
 /// Returns a unitary operation that applies an oracle on the target register if the 
 /// control register state corresponds to a specified bit mask.
 ///
 /// # Description
 /// The output of this function is an operation that can be represented by a
 /// unitary transformation $U$ such that
 /// \begin{align}
 ///     U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes
 ///     \begin{cases}
 ///         V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\
 ///         \ket{\psi} & \textrm{otherwise}
 ///     \end{cases},
 /// \end{align}
 /// where $V$ is a unitary transformation that represents the action of the
 /// `oracle` operation.
 ///
 /// # Input
 /// ## bits
 /// The bit string to control the given unitary operation on.
 /// ## oracle
 /// The unitary operation to be applied on the target register.
 ///
 /// # Output
 /// A unitary operation that applies `oracle` on the target register if the control 
 /// register state corresponds to the bit mask `bits`.
 ///
 /// # Remarks
 /// The length of `bits` and `controlRegister` must be equal.
 ///
 /// Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function
 /// is an operation that performs the following steps:
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits`;
 /// * apply `Controlled oracle` to the control and target registers;
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits` again to return the control register to the original state.
 ///
 /// The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.
 ///
 /// # Example
 /// The following code snippets are equivalent:
 /// ```qsharp
 /// (ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
 /// ```
 /// and
 /// ```qsharp
 /// within {
 ///     ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
 /// } apply {
 ///     Controlled oracle(controlRegister, targetRegister);
 /// }
 /// ```
 ///
 /// The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:
 /// ```qsharp
 /// using (register = Qubit[2]) {
 ///     ApplyToEach(H, register);
 ///     (ControlledOnBitString([false], Z))(register[0..0], register[1]);
 /// }
 /// ```
 function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
 {
     return ControlledOnBitStringImpl(bits, oracle, _, _);
 }
```
U kunt de gerenderde versie van de bovenstaande code bekijken in de [API-documentatie voor de functie `ControlledOnBitString`](xref:microsoft.quantum.canon.controlledonbitstring).

Naast de algemene procedures voor het schrijven van documentatie, in het schrijven van API-documentatie opmerkingen, is het handig om een aantal zaken in acht te nemen:

- De indeling van elke documentatie opmerking moet overeenkomen met wat de Q #-compiler verwacht dat uw documentatie correct wordt weer gegeven. Sommige secties, zoals `/// # Remarks` toestaan voor vrije-vorm inhoud, terwijl secties zoals `/// # See Also` sectie meer beperkend zijn.
- Een lezer kan uw API-documentatie lezen op de belangrijkste API-referentie site, op basis van de samen vatting van elke naam ruimte of zelfs vanuit de IDE door het gebruik van de aanwijs informatie te gebruiken. Als u er zeker van wilt zijn dat `/// # Summary` niet langer is dan een zin, kunt u met uw lezer snel zien of ze verder moeten worden gelezen of ergens anders moeten kijken en kunt u helpen bij het snel scannen van naam ruimte overzichten.
- Het is mogelijk dat uw documentatie veel langer is dan de code zelf, maar dat is wel goed. Zelfs een klein stukje code kan onverwachte gevolgen hebben voor gebruikers die niet weten in welke context de code zich bevindt. Door concrete voor beelden te bieden en duidelijke uitleg te geven, kunt u gebruikers helpen het beste gebruik te maken van de code die voor hen van toepassing is.

<!-- ## LaTeX Formatting ##

**TODO** -->
