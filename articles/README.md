# <a name="articles"></a>Artikelen

In deze Directory vindt u de artikelen voor de documentatie van de Quantum Development Kit. Deze map bevat:

- **Artikelen directory's**: bevatten de artikelen voor elke sectie van de documentatie. In deze directory's vindt u de volgende inhoud:
  
  - Elke directory bevat een `toc.yml` bestand om de inhoud van de map weer te geven in de hoofd inhouds opgave (TOC).
  - Verkort artikelen die de documentatie bevatten. Deze artikelen moeten voldoen aan de richt lijnen van de [hand leiding Microsoft docs contributor](https://docs.microsoft.com/en-us/contribute/).
  - Submappen van artikelen. Deze submappen moeten ook een eigen `toc.yml` bestand bevatten.

> :p encil: Hoewel het mogelijk is om de `*.md` bestanden rechtstreeks in het bovenliggende `TOC.yml` bestand te plaatsen, zodat ze alleen kunnen worden genoteerd, worden ze alleen naar de huidige map gerefereerd `toc.yml` .

- **Hoofd `TOC.yml` bestand van inhouds opgave (TOC)**: in dit bestand worden de secties van de inhouds opgave van de website weer gegeven samen met de verwijzing naar het hoofd `toc.yml` bestand van de map van elke sectie.
- **`index.yml`** YAML met de configuratie van de landings pagina van de documentatie.
- **`\media`**: Een directory voor het opslaan van alle installatie kopieën die in de documentatie worden gebruikt. Het bevat een `\media\src` submap om de bron bestanden van de installatie kopieën op te slaan.
- **Licentie bestanden**: bestanden met geldige licenties
- **Technische bestanden**: bestanden met macro's en meta gegevens.

## <a name="guidelines"></a>Richtlijnen

Enkele algemene richt lijnen over de organisatie van deze directory voor inzenders:

- Elke directory of submap moet een eigen bestand bevatten waarin alle `toc.yml` artikelen van hetzelfde niveau of de `toc.yml` bestanden van de onderliggende mappen worden genoemd.
- De organisatie van de directory's van de opslag plaats moet zo dicht mogelijk zijn bij de organisatie van de inhouds opgave van de documentatie website.
- Alle installatie kopieën moeten worden opgeslagen in `articles\media` en niet in de map artikelen.
- De titels van de artikelen, de namen in de inhouds opgave en de *UID* van de meta gegevens moeten zo dicht mogelijk naast elkaar staan en duidelijk de h1-kop van het document voor de korting.

## <a name="adding-images"></a>Installatie kopieën toevoegen

Om ervoor te zorgen dat de afbeeldingen goed worden weer gegeven in de donkere modus, moet u transparanten vermijden.
- Voor `*.jpg` bestanden hoeft u niets te doen omdat de bestands indeling geen transparante elementen ondersteunt.
- Voor `*.png` bestanden moet u een witte achtergrond toevoegen of de waarde van het Alfa kanaal wijzigen in 100. De eenvoudigste manier om dit te doen in Windows is door het bestand te openen in Paint en opslaan, het oorspronkelijke bestand te overschrijven.
- Voor `*.svg` bestanden moet u een witte rechthoek toevoegen aan de laagste laag. U kunt dit doen met Inkscape:
  - Open het `*.svg`-bestand.
  - Selecteer het gereedschap vier Kante maker en teken een witte rechthoek boven op de oorspronkelijke afbeelding.
  - Selecteer het hulp programma ' objecten selecteren en transformeren ' door te klikken op de donkere pijl of op F1 te drukken.
  - Terwijl de rechthoek is geselecteerd, klikt u in het werkbalk element onder selectie naar onder (End).
  - Pas de rechthoek aan met de muis of de pijl toetsen.
