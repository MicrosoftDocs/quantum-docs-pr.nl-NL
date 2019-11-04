---
title: Schei kunde-bibliotheek installatie en-validatie | Microsoft Docs
description: Schei kunde van de bibliotheek installatie en validatie
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: fd43c783fa82c7219e143a57759919606fdd197f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184199"
---
# <a name="chemistry-library-installation-and-validation"></a>Schei kunde van de bibliotheek installatie en validatie

De Quantum Development Kit biedt ondersteuning voor quantum chemie-toepassingen via het NuGet-pakket van [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) .
Net als bij andere NuGet-pakketten is het eenvoudig om de Library chemie toe te voegen aan uw project.

**Visual Studio 2019:** Als u Visual Studio 2019 gebruikt, kunt u de quantum chemie-pakketten toevoegen met behulp van de NuGet-pakket Manager.
Als u pakket beheer wilt openen, klikt u met de rechter muisknop op het project waaraan u de bibliotheek voor schei kunde wilt toevoegen en selecteert u ' NuGet-pakketten beheren... ', zoals in de onderstaande scherm afbeelding.

![](~/media/vs2017-nuget-manage-packages.png)

Zoek op het tabblad Bladeren naar de pakket naam ' micro soft. Quantum. chemie '.

> [!NOTE]
> Zorg ervoor dat u ' include Prerelease ' opgeeft.

![](~/media/vs2017-nuget-package-search.png)

Hiermee worden de pakketten weer geven die kunnen worden gedownload.
Klik op ' micro soft. Quantum. chemie ' in het linkerdeel venster, selecteer de nieuwste voorlopige versie in het rechterdeel venster en klik op installeren:

![](~/media/vs2017-nuget-select-chem.png)

Zie de [gebruikers interface voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-ui)voor meer informatie.

U kunt ook de Package Manager-console gebruiken om de quantum chemie-bibliotheek toe te voegen aan uw project met een opdracht regel interface.

![](~/media/vs2017-nuget-console-menu.png)

Voer de volgende handelingen uit vanuit de Package Manager-console:

```
Install-Package Microsoft.Quantum.Chemistry
```

Zie de [console handleiding voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-console)voor meer informatie.

**Opdracht regel of Visual Studio code:** Met de opdracht regel zelf of vanuit Visual Studio code kunt u de `dotnet` opdracht gebruiken om de NuGet-pakket verwijzing toe te voegen aan uw project:

```bash
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a>De installatie controleren 

Net als de rest van de Quantum Development Kit wordt de quantum chemie-bibliotheek geleverd met een aantal volledig gedocumenteerde voor beelden om snel aan de slag te kunnen.
Als u de installatie met behulp van deze voor beelden wilt testen, kloont u de [opslag plaats](https://github.com/Microsoft/Quantum)voor de belangrijkste voor beelden en voert u een van de voor beelden  Als u bijvoorbeeld het [`MolecularHydrogen`](https://github.com/Microsoft/Quantum/tree/master/Chemistry/MolecularHydrogen) -voor beeld wilt uitvoeren:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Chemistry/MolecularHydrogen
dotnet run
```

Controleren of de quantum chemie-bibliotheek is geïnstalleerd met behulp van micro soft Visual Studio na het klonen van de opslag plaats:
    1. Open de oplossing ChemistrySamples. SLN in de map schei kunde.  
    2. Selecteer voor beelden/1. Eenvoudige moleculen/MolecularHydrogen als het opstart project.
    3. Druk op F5 om de demo van de molecuul waterstof Quantum-fase schatting uit te voeren.

Zie [schattingen voor het energie niveau verkrijgen](xref:microsoft.quantum.chemistry.examples.energyestimate) voor meer informatie over het schatten van de waarden van energie niveaus.   


## <a name="using-the-quantum-development-kit-with-nwchem"></a>De Quantum Development Kit gebruiken met NWChem ##

Het MolecularHydrogen-voor beeld maakt gebruik van moleculaire invoer gegevens die hand matig worden geconfigureerd.  Hoewel dit een kleine voor beeld is, is voor Quantum-schei kunde op schaal Hamiltonians met miljoenen of miljarden voor waarden vereist. Dergelijke Hamiltonians, die zijn gegenereerd door schaal bare reken kunde-pakketten, zijn te groot om hand matig te importeren. 

De quantum chemie-bibliotheek voor de Quantum Development Kit is ontworpen om goed te werken met reken kundige chemie-pakketten, met name het [**NWChem**](http://www.nwchem-sw.org/) computing computing-platform dat is ontwikkeld door het Environmental wetenschappen Laboratory ( EMSL) op het nationale laboratorium van Pacific Noordwest.
Met name het `Microsoft.Quantum.Chemistry`-pakket biedt hulpprogram ma's voor het laden van exemplaren van de simulatie problemen die in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)worden weer gegeven, ook ondersteund voor export door recente versies van NWChem.

Als u NWChem wilt gebruiken in combi natie met de Quantum Development Kit, wordt een van de volgende methoden voorgesteld:
- Ga aan de slag met bestaande Broombridge-bestanden die zijn meegeleverd met de voor beelden op [IntegralData/yaml](https://github.com/Microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML).
- Gebruik de [opbouw functie voor EMSL-pijlen voor de Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) die een web-front-end is voor NWChem, voor het genereren van nieuwe Broombridge-geformatteerde moleculaire invoer bestanden.  
- Gebruik de [docker-installatie kopie](https://hub.docker.com/r/nwchemorg/nwchem-qc/) van PNNL om NWChem uit te voeren, of
- [Compileer NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) voor uw platform.

Zie [end-to-end met NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) voor meer informatie over het werken met NWChem en chemische modellen om te analyseren met de Quantum werknem Kit chemie-bibliotheek.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Aan de slag met Broombridge-bestanden die worden meegeleverd met de voor beelden
De map [IntegralData/yaml](https://github.com/Microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML) in de Quantum Development Kit samples-opslag bevat Broombridge-indeling gelabelde gegevens bestanden.  

Gebruik bijvoorbeeld het voor beeld van chemie Library, [GetGateCount](https://github.com/Microsoft/Quantum/tree/master/Chemistry/GetGateCount) om de Hamiltonian te laden vanuit een van Broombridge-bestanden en poort schattingen van Quantum simulatie algorigthms uit te voeren:

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

Zie [een Hamiltonian laden uit het bestand](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) voor meer informatie over het invoeren van moleculen die worden weer gegeven door het Broombridge-schema.  

Zie [resource tellingen ophalen](xref:microsoft.quantum.chemistry.examples.resourcecounts) voor meer informatie over het schatten van resources.  

### <a name="getting-started-using-the-emsl-arrows-builder"></a>Aan de slag met de opbouw functie voor EMSL-pijlen

EMSL Arrows is een hulp programma dat gebruikmaakt van NWChem en chemische reken databases voor het genereren van molecuul gegevens.  Met [EMSL Arrow Builder voor de Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) kunt u uw model invoeren met meerdere moleculaire model bouwers en het Broombridge gegevensbestand genereren dat door de Quantum Development Kit moet worden gebruikt.  

Klik op de pagina EMSL op het tabblad [' instuctions '] en volg de instructies voor [' eenvoudige voor beelden '] om Broombridge-bestanden te genereren.  Probeer vervolgens [' GetGateCount '] uit te voeren om de Quantum resource schattingen voor deze moleculen weer te geven.

### <a name="installing-nwchem-from-source"></a>NWChem installeren vanuit de bron

Volledige instructies voor het installeren van NWChem vanaf de bron [zijn afkomstig van PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).

> [!TIP]
> Als u NWChem van Windows 10 wilt gebruiken, is het Windows-subsysteem voor Linux een uitstekende optie.
> Nadat u [Ubuntu 18,04 LTS voor Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)hebt geïnstalleerd, voert u `ubuntu18.04` uit vanuit uw favoriete terminal en volgt u de bovenstaande instructies om NWChem van de bron te installeren.

Wanneer u NWChem hebt gecompileerd vanuit de bron, kunt u het `yaml_driver` script uitvoeren dat is opgegeven met NWChem om snel Broombridge-instanties te maken op basis van NWChem-invoer dekken:

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

Met deze opdracht wordt een nieuw `input.yaml`-bestand gemaakt in de Broombridge-indeling in de huidige map.

### <a name="using-nwchem-with-docker"></a>NWChem gebruiken met docker

Vooraf gemaakte installatie kopieën voor het gebruik van NWChem zijn beschikbaar voor meerdere platforms via [docker hub](https://hub.docker.com).
Volg de installatie-instructies voor docker voor uw platform om aan de slag te gaan:

- [Docker voor Ubuntu installeren](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Docker voor macOS installeren](https://docs.docker.com/docker-for-mac/install/)
- [Docker voor Windows 10 installeren](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> Als u docker voor Windows gebruikt, moet u het station met de tijdelijke map delen (dit is meestal het `C:\` station) met de docker-daemon. Raadpleeg de [docker-documentatie](https://docs.docker.com/docker-for-windows/#shared-drives) voor meer informatie.

Zodra u docker hebt geïnstalleerd, kunt u de Power shell-module van de Quantum Development Kit-voor beelden gebruiken om de installatie kopie uit te voeren, of u kunt de installatie kopie hand matig uitvoeren.
Hier vindt u informatie over het gebruik van Power shell. Als u de docker-installatie kopie hand matig wilt gebruiken, raadpleegt u de [documentatie van de installatie kopie](https://hub.docker.com/r/nwchemorg/nwchem-qc/).

#### <a name="running-nwchem-through-powershell-core"></a>NWChem uitvoeren via Power shell core

Als u de NWChem docker-installatie kopie wilt gebruiken met de Quantum Development Kit, bieden we een kleine Power shell-module die het verplaatsen van bestanden in en uit NWChem voor u verzorgt.
Als u de Power shell-kern nog niet hebt geïnstalleerd, kunt u deze cross-platform downloaden vanuit de [Power shell-opslag plaats op github](https://github.com/PowerShell/PowerShell#get-powershell).

> [!NOTE]
> Power shell core wordt ook gebruikt voor enkele voor beelden voor het demonstreren van interoperabiliteit met data Science en Business Analytics-werk stromen.

Zodra u Power shell core hebt geïnstalleerd, importeert u `InvokeNWChem.psm1` om NWChem-opdrachten beschikbaar te maken in uw huidige sessie:

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

Hiermee wordt de `Convert-NWChemToBroombridge`-opdracht beschikbaar gemaakt in uw huidige Power shell-sessie.
Voer het volgende uit om de benodigde installatie kopieën van docker te downloaden en te gebruiken voor het uitvoeren van NWChem-invoer dekken en het vastleggen van uitvoer naar Broombridge:

```powershell
Convert-NWChemToBroombridge ./input.nw
```

Hiermee maakt u een Broombridge-bestand door NWChem uit te voeren op `input.nw`.
De Broombridge-uitvoer heeft standaard dezelfde naam en hetzelfde pad als het invoer deck, waarbij de uitbrei ding `.nw` door `.yaml`is vervangen.
Dit kan worden overschreven door gebruik te maken van de para meter `-DestinationPath` om `Convert-NWChemToBroombridge`.
Meer informatie kan worden verkregen met behulp van de ingebouwde Help-functionaliteit van Power shell:

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```


