---
title: Installatie van micro soft Q# chemie Library
description: Meer informatie over het installeren van de micro soft quantum chemie-bibliotheek en het gebruik ervan met het NWChem Computation-chemische platform.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5fe973d24ceffd413cdbd3c543013dcc7ee379c0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869338"
---
# <a name="chemistry-library-installation"></a>Schei-bibliotheek installatie

Het [ **MolecularHydrogen** ](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) -voor beeld maakt gebruik van moleculaire invoer gegevens die hand matig worden geconfigureerd.
Hoewel dit goed is voor kleine voor beelden, vereist Quantum-schei kunde op schaal Hamiltonians met miljoenen of miljarden termen.
Dergelijke Hamiltonians, die worden gegenereerd door schaal bare reken kunde-pakketten, zijn te groot om met de hand te worden geïmporteerd.

De quantum chemie-bibliotheek voor de Quantum Development Kit is ontworpen voor gebruik met reken kundige chemie-pakketten, met name het [**NWChem**](http://www.nwchem-sw.org/) computing computing-platform dat is ontwikkeld door het Environmental wetenschappen LABORATORY (EMSL) op Pacific Noordwest National Laboratory.
Met name het pakket [ **micro soft. Quantum. chemie** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) voorziet in hulpprogram ma's voor het laden van exemplaren van de simulatie problemen die in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)worden weer gegeven, ook ondersteund voor export door recente versies van NWChem.

De Quantum Development Kit chemie-bibliotheek biedt ook een opdracht regel programma, `qdk-chem` voor het converteren van een oude indeling en [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).

In deze sectie wordt beschreven hoe u de Quantum Development Kit kunt gebruiken met NWChem en Broombridge, of met een verouderde indeling en `qdk-chem` .

## <a name="using-the-quantum-development-kit-with-nwchem"></a>De Quantum Development Kit gebruiken met NWChem

Gebruik een van de volgende methoden om aan de slag te gaan met NWChem in combi natie met de Quantum Development Kit:

- Ga aan de slag met bestaande Broombridge-bestanden die zijn meegeleverd met de voor beelden op [IntegralData/yaml](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).
- Gebruik de [opbouw functie voor EMSL-pijlen voor de Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) die een web-front-end is voor NWChem, voor het genereren van nieuwe Broombridge-geformatteerde moleculaire invoer bestanden.  
- Gebruik de [docker-installatie kopie](https://hub.docker.com/r/nwchemorg/nwchem-qc/) van PNNL om NWChem uit te voeren, of
- [Compileer NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) voor uw platform.

Zie [end-to-end met NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) voor meer informatie over het werken met NWChem en chemische modellen om te analyseren met de Quantum werknem Kit chemie-bibliotheek.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Aan de slag met Broombridge-bestanden die worden meegeleverd met de voor beelden

De map [IntegralData/yaml](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) in de Quantum Development Kit samples-opslag bevat Broombridge-indeling gelabelde gegevens bestanden.  

Gebruik bijvoorbeeld het voor beeld van chemie Library, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) om de Hamiltonian te laden vanuit een van Broombridge-bestanden en poort schattingen van Quantum simulatie algorigthms uit te voeren:

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
> Nadat u [Ubuntu 18,04 LTS voor Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)hebt geïnstalleerd, voert u `ubuntu18.04` uit vanaf uw favoriete terminal en volgt u de bovenstaande instructies om NWChem van de bron te installeren.

Wanneer u NWChem hebt gecompileerd vanuit de bron, kunt u het `yaml_driver` script uitvoeren dat is opgegeven met NWChem om snel Broombridge-instanties te maken op basis van NWChem-invoer dekken:

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

Met deze opdracht wordt een nieuw `input.yaml` bestand gemaakt in de Broombridge-indeling in de huidige map.

### <a name="using-nwchem-with-docker"></a>NWChem gebruiken met docker

Vooraf gemaakte installatie kopieën voor het gebruik van NWChem zijn beschikbaar voor meerdere platforms via [docker hub](https://hub.docker.com).
Volg de installatie-instructies voor docker voor uw platform om aan de slag te gaan:

- [Docker voor Ubuntu installeren](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Docker voor macOS installeren](https://docs.docker.com/docker-for-mac/install/)
- [Docker voor Windows 10 installeren](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> Als u docker voor Windows gebruikt, moet u het station met de tijdelijke map (meestal het `C:\` station) met de docker-daemon delen. Raadpleeg de [docker-documentatie](https://docs.docker.com/docker-for-windows/#shared-drives) voor meer informatie.

Zodra u docker hebt geïnstalleerd, kunt u de Power shell-module van de Quantum Development Kit-voor beelden gebruiken om de installatie kopie uit te voeren, of u kunt de installatie kopie hand matig uitvoeren.
Hier vindt u informatie over het gebruik van Power shell. Als u de docker-installatie kopie hand matig wilt gebruiken, raadpleegt u de [documentatie van de installatie kopie](https://hub.docker.com/r/nwchemorg/nwchem-qc/).

#### <a name="running-nwchem-through-powershell-core"></a>NWChem uitvoeren via Power shell core

Als u de NWChem docker-installatie kopie wilt gebruiken met de Quantum Development Kit, bieden we een kleine Power shell-module die het verplaatsen van bestanden in en uit NWChem voor u verzorgt.
Als u de Power shell-kern nog niet hebt geïnstalleerd, kunt u deze cross-platform downloaden vanuit de [Power shell-opslag plaats op github](https://github.com/PowerShell/PowerShell#get-powershell).

> [!NOTE]
> Power shell core wordt ook gebruikt voor enkele voor beelden voor het demonstreren van interoperabiliteit met data Science en Business Analytics-werk stromen.

Zodra u Power shell core hebt geïnstalleerd, importeert u `InvokeNWChem.psm1` de NWChem-opdrachten die beschikbaar zijn in uw huidige sessie:

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

Hiermee wordt de `Convert-NWChemToBroombridge` opdracht beschikbaar gemaakt in uw huidige Power shell-sessie.
Voer het volgende uit om de benodigde installatie kopieën van docker te downloaden en te gebruiken voor het uitvoeren van NWChem-invoer dekken en het vastleggen van uitvoer naar Broombridge:

```powershell
Convert-NWChemToBroombridge ./input.nw
```

Hiermee maakt u een Broombridge-bestand door NWChem uit te voeren op `input.nw` .
De Broombridge-uitvoer heeft standaard dezelfde naam en hetzelfde pad als het invoer deck, waarbij de extensie is `.nw` vervangen door `.yaml` .
Dit kan worden overschreven door gebruik te maken van de `-DestinationPath` para meter voor `Convert-NWChemToBroombridge` .
Meer informatie kan worden verkregen met behulp van de ingebouwde Help-functionaliteit van Power shell:

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```

## <a name="using-the-quantum-development-kit-with-qdk-chem"></a>De Quantum Development Kit gebruiken met`qdk-chem`

Als u wilt installeren `qdk-chem` , kunt u het .net core SDK gebruiken op de opdracht regel:

```dotnetcli
dotnet tool install --global Microsoft.Quantum.Chemistry.Tools
```

Wanneer u hebt geïnstalleerd `qdk-chem` , kunt u de `--help` optie gebruiken om meer informatie te krijgen over de functionaliteit van het `qdk-chem` hulp programma.

Als u wilt converteren naar en van Broombridge, kunt u de `qdk-chem convert` opdracht gebruiken:

```
qdk-chem convert --from fcidump --to broombridge data.fcidump --out data.yml
```

De `qdk-chem convert` opdracht kan ook de gegevens van de standaard invoer accepteren en kan schrijven naar de standaard uitvoer. Dit is vooral nuttig in scripts en voor de integratie met hulpprogram ma's die naar verouderde indelingen exporteren.
Bijvoorbeeld, in Bash:

```bash
cat data.fcidump | qdk-convert --from fcidump --to broombridge - > data.yml
```
