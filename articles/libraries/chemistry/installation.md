---
title: 'Micro soft Q # library-installatie en-validatie'
description: Meer informatie over het installeren van de micro soft quantum chemie-bibliotheek en het gebruik ervan met het NWChem Computation-chemische platform.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: 48bf7bc980e238e622053f5c2bdd09604c572596
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907355"
---
# <a name="chemistry-library-installation-and-validation"></a><span data-ttu-id="146d5-103">Schei kunde van de bibliotheek installatie en validatie</span><span class="sxs-lookup"><span data-stu-id="146d5-103">Chemistry Library Installation and Validation</span></span>

<span data-ttu-id="146d5-104">De Quantum Development Kit biedt ondersteuning voor quantum chemie-toepassingen via het NuGet-pakket van [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="146d5-104">The Quantum Development Kit provides support for quantum chemistry applications through the [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) NuGet package.</span></span>
<span data-ttu-id="146d5-105">Net als bij andere NuGet-pakketten is het eenvoudig om de Library chemie toe te voegen aan uw project.</span><span class="sxs-lookup"><span data-stu-id="146d5-105">As with other NuGet packages, it's straightforward to add the chemistry library to your project.</span></span>

<span data-ttu-id="146d5-106">**Visual Studio 2019:** Als u Visual Studio 2019 gebruikt, kunt u de quantum chemie-pakketten toevoegen met behulp van de NuGet-pakket Manager.</span><span class="sxs-lookup"><span data-stu-id="146d5-106">**Visual Studio 2019:** If you are using Visual Studio 2019, you can add the quantum chemistry packages by using the NuGet Package Manager.</span></span>
<span data-ttu-id="146d5-107">Als u pakket beheer wilt openen, klikt u met de rechter muisknop op het project waaraan u de bibliotheek voor schei kunde wilt toevoegen en selecteert u ' NuGet-pakketten beheren... ', zoals in de onderstaande scherm afbeelding.</span><span class="sxs-lookup"><span data-stu-id="146d5-107">To open the Package Manager, right-click on the project you'd like to add the chemistry library to and select "Manage NuGet Packages...," as in the screenshot below.</span></span>

![NuGet Package Manager gebruiken in Visual Studio 2019](~/media/vs2017-nuget-manage-packages.png)

<span data-ttu-id="146d5-109">Zoek op het tabblad Bladeren naar de pakket naam ' micro soft. Quantum. chemie '.</span><span class="sxs-lookup"><span data-stu-id="146d5-109">From the Browse tab, search for the package name "Microsoft.Quantum.Chemistry."</span></span>

> [!NOTE]
> <span data-ttu-id="146d5-110">Zorg ervoor dat u ' include Prerelease ' opgeeft.</span><span class="sxs-lookup"><span data-stu-id="146d5-110">Make sure to tick "Include prerelease."</span></span>

![Selectie vakje voor voorlopige versie toevoegen](~/media/vs2017-nuget-package-search.png)

<span data-ttu-id="146d5-112">Hiermee worden de pakketten weer geven die kunnen worden gedownload.</span><span class="sxs-lookup"><span data-stu-id="146d5-112">This will list the packages available for download.</span></span>
<span data-ttu-id="146d5-113">Klik op ' micro soft. Quantum. chemie ' in het linkerdeel venster, selecteer de nieuwste voorlopige versie in het rechterdeel venster en klik op installeren:</span><span class="sxs-lookup"><span data-stu-id="146d5-113">Click on the "Microsoft.Quantum.Chemistry on the left-hand pane, select the latest pre-release version on the right-hand pane, and click "Install":</span></span>

![Installeer het nieuwste pakket micro soft. Quantum. chemie](~/media/vs2017-nuget-select-chem.png)

<span data-ttu-id="146d5-115">Zie de [gebruikers interface voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-ui)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="146d5-115">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="146d5-116">U kunt ook de Package Manager-console gebruiken om de quantum chemie-bibliotheek toe te voegen aan uw project met een opdracht regel interface.</span><span class="sxs-lookup"><span data-stu-id="146d5-116">Alternatively, you can use the Package Manager Console to add the quantum chemistry library to your project with a command line interface.</span></span>

![De Package Manager-console gebruiken vanaf de opdracht regel](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="146d5-118">Voer de volgende handelingen uit vanuit de Package Manager-console:</span><span class="sxs-lookup"><span data-stu-id="146d5-118">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Chemistry
```

<span data-ttu-id="146d5-119">Zie de [console handleiding voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-console)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="146d5-119">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="146d5-120">**Opdracht regel of Visual Studio code:** Met de opdracht regel zelf of vanuit Visual Studio code kunt u de `dotnet` opdracht gebruiken om de NuGet-pakket verwijzing toe te voegen aan uw project:</span><span class="sxs-lookup"><span data-stu-id="146d5-120">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a><span data-ttu-id="146d5-121">De installatie controleren</span><span class="sxs-lookup"><span data-stu-id="146d5-121">Verifying Your Installation</span></span> 

<span data-ttu-id="146d5-122">Net als de rest van de Quantum Development Kit wordt de quantum chemie-bibliotheek geleverd met een aantal volledig gedocumenteerde voor beelden om snel aan de slag te kunnen.</span><span class="sxs-lookup"><span data-stu-id="146d5-122">Like the rest of the Quantum Development Kit, the quantum chemistry library comes with a number of fully documented samples to help you get up and running quickly.</span></span>
<span data-ttu-id="146d5-123">Als u de installatie met behulp van deze voor beelden wilt testen, kloont u de [opslag plaats](https://github.com/Microsoft/Quantum)voor de belangrijkste voor beelden en voert u een van de voor beelden</span><span class="sxs-lookup"><span data-stu-id="146d5-123">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum), then run one of the samples.</span></span>  <span data-ttu-id="146d5-124">Als u bijvoorbeeld het [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) -voor beeld wilt uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="146d5-124">For example, to run the [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

<span data-ttu-id="146d5-125">Controleren of de quantum chemie-bibliotheek is geïnstalleerd met behulp van micro soft Visual Studio na het klonen van de opslag plaats:</span><span class="sxs-lookup"><span data-stu-id="146d5-125">To verify the installation of the quantum chemistry library using Microsoft Visual Studio after cloning the repository:</span></span>
    1. <span data-ttu-id="146d5-126">Open de oplossing ChemistrySamples. SLN in de map schei kunde.</span><span class="sxs-lookup"><span data-stu-id="146d5-126">Open the ChemistrySamples.sln solution in the Chemistry folder.</span></span>  
    2. <span data-ttu-id="146d5-127">Selecteer voor beelden/1.</span><span class="sxs-lookup"><span data-stu-id="146d5-127">Select Samples/1.</span></span> <span data-ttu-id="146d5-128">Eenvoudige moleculen/MolecularHydrogen als het opstart project.</span><span class="sxs-lookup"><span data-stu-id="146d5-128">Simple Molecules/MolecularHydrogen as the StartUp project.</span></span>
    3. <span data-ttu-id="146d5-129">Druk op F5 om de demo van de molecuul waterstof Quantum-fase schatting uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="146d5-129">Press F5 to run the molecular Hydrogen quantum phase estimation demo.</span></span>

<span data-ttu-id="146d5-130">Zie [schattingen voor het energie niveau verkrijgen](xref:microsoft.quantum.chemistry.examples.energyestimate) voor meer informatie over het schatten van de waarden van energie niveaus.</span><span class="sxs-lookup"><span data-stu-id="146d5-130">See [Obtaining energy level estimates](xref:microsoft.quantum.chemistry.examples.energyestimate) for more information on estimating the values of energy levels.</span></span>   


## <a name="using-the-quantum-development-kit-with-nwchem"></a><span data-ttu-id="146d5-131">De Quantum Development Kit gebruiken met NWChem</span><span class="sxs-lookup"><span data-stu-id="146d5-131">Using the Quantum Development Kit with NWChem</span></span> ##

<span data-ttu-id="146d5-132">Het MolecularHydrogen-voor beeld maakt gebruik van moleculaire invoer gegevens die hand matig worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="146d5-132">The MolecularHydrogen sample uses molecular input data that is manually configured.</span></span>  <span data-ttu-id="146d5-133">Hoewel dit een kleine voor beeld is, is voor Quantum-schei kunde op schaal Hamiltonians met miljoenen of miljarden voor waarden vereist.</span><span class="sxs-lookup"><span data-stu-id="146d5-133">While this is fine for small examples, quantum chemistry at scale require Hamiltonians with millions or billions of terms.</span></span> <span data-ttu-id="146d5-134">Dergelijke Hamiltonians, die zijn gegenereerd door schaal bare reken kunde-pakketten, zijn te groot om hand matig te importeren.</span><span class="sxs-lookup"><span data-stu-id="146d5-134">Such Hamiltonians, generated by scalable computational chemistry packages are too large to import by hand.</span></span> 

<span data-ttu-id="146d5-135">De quantum chemie-bibliotheek voor de Quantum Development Kit is ontworpen voor gebruik met reken kundige chemie-pakketten, met name het [**NWChem**](http://www.nwchem-sw.org/) computing computing-platform dat is ontwikkeld door het Environmental wetenschappen LABORATORY (EMSL) op Pacific Noordwest National Laboratory.</span><span class="sxs-lookup"><span data-stu-id="146d5-135">The quantum chemistry library for the Quantum Development Kit is designed to work well with computational chemistry packages, most notably the [**NWChem**](http://www.nwchem-sw.org/) computational chemistry platform developed by the Environmental Molecular Sciences Laboratory (EMSL) at Pacific Northwest National Laboratory.</span></span>
<span data-ttu-id="146d5-136">Met name het `Microsoft.Quantum.Chemistry`-pakket biedt hulpprogram ma's voor het laden van exemplaren van de simulatie problemen die in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)worden weer gegeven, ook ondersteund voor export door recente versies van NWChem.</span><span class="sxs-lookup"><span data-stu-id="146d5-136">In particular, the `Microsoft.Quantum.Chemistry` package provides tools for loading instances of quantum chemistry simulation problems represented in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), also supported for export by recent versions of NWChem.</span></span>

<span data-ttu-id="146d5-137">Als u NWChem wilt gebruiken in combi natie met de Quantum Development Kit, wordt een van de volgende methoden voorgesteld:</span><span class="sxs-lookup"><span data-stu-id="146d5-137">To get up and running using NWChem together with the Quantum Development Kit, we suggest one of the following methods:</span></span>
- <span data-ttu-id="146d5-138">Ga aan de slag met bestaande Broombridge-bestanden die zijn meegeleverd met de voor beelden op [IntegralData/yaml](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span><span class="sxs-lookup"><span data-stu-id="146d5-138">Get started using existing Broombridge files provided with the samples at [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span>
- <span data-ttu-id="146d5-139">Gebruik de [opbouw functie voor EMSL-pijlen voor de Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) die een web-front-end is voor NWChem, voor het genereren van nieuwe Broombridge-geformatteerde moleculaire invoer bestanden.</span><span class="sxs-lookup"><span data-stu-id="146d5-139">Use the [EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) which is a web-based frontend to NWChem, to generate new Broombridge-formated molecular input files.</span></span>  
- <span data-ttu-id="146d5-140">Gebruik de [docker-installatie kopie](https://hub.docker.com/r/nwchemorg/nwchem-qc/) van PNNL om NWChem uit te voeren, of</span><span class="sxs-lookup"><span data-stu-id="146d5-140">Use the [Docker image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) provided by PNNL to run NWChem, or</span></span>
- <span data-ttu-id="146d5-141">[Compileer NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) voor uw platform.</span><span class="sxs-lookup"><span data-stu-id="146d5-141">[Compile NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) for your platform.</span></span>

<span data-ttu-id="146d5-142">Zie [end-to-end met NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) voor meer informatie over het werken met NWChem en chemische modellen om te analyseren met de Quantum werknem Kit chemie-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="146d5-142">See [End-to-end with NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) for more information on how to work with NWChem to chemical models to analyze with the Quantum Developmen Kit chemistry library.</span></span>

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a><span data-ttu-id="146d5-143">Aan de slag met Broombridge-bestanden die worden meegeleverd met de voor beelden</span><span class="sxs-lookup"><span data-stu-id="146d5-143">Getting started using Broombridge files provided with the samples</span></span>

<span data-ttu-id="146d5-144">De map [IntegralData/yaml](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) in de Quantum Development Kit samples-opslag bevat Broombridge-indeling gelabelde gegevens bestanden.</span><span class="sxs-lookup"><span data-stu-id="146d5-144">The [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) folder in the Quantum Development Kit Samples repository contains Broombridge-formated molecule data files.</span></span>  

<span data-ttu-id="146d5-145">Gebruik bijvoorbeeld het voor beeld van chemie Library, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) om de Hamiltonian te laden vanuit een van Broombridge-bestanden en poort schattingen van Quantum simulatie algorigthms uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="146d5-145">As a simple example, use the chemistry library sample, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) to load the Hamiltonian from one of Broombridge files and perform gate estimates of quantum simulation algorigthms:</span></span>

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

<span data-ttu-id="146d5-146">Zie [een Hamiltonian laden uit het bestand](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) voor meer informatie over het invoeren van moleculen die worden weer gegeven door het Broombridge-schema.</span><span class="sxs-lookup"><span data-stu-id="146d5-146">See [Loading a Hamiltonian from file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) for more information on how to input molecules represented by the Broombridge schema.</span></span>  

<span data-ttu-id="146d5-147">Zie [resource tellingen ophalen](xref:microsoft.quantum.chemistry.examples.resourcecounts) voor meer informatie over het schatten van resources.</span><span class="sxs-lookup"><span data-stu-id="146d5-147">See [Obtaining resource counts](xref:microsoft.quantum.chemistry.examples.resourcecounts) for more information on resource estimation.</span></span>  

### <a name="getting-started-using-the-emsl-arrows-builder"></a><span data-ttu-id="146d5-148">Aan de slag met de opbouw functie voor EMSL-pijlen</span><span class="sxs-lookup"><span data-stu-id="146d5-148">Getting started using the EMSL Arrows Builder</span></span>

<span data-ttu-id="146d5-149">EMSL Arrows is een hulp programma dat gebruikmaakt van NWChem en chemische reken databases voor het genereren van molecuul gegevens.</span><span class="sxs-lookup"><span data-stu-id="146d5-149">EMSL Arrows is a tool that uses NWChem and chemical computational databases to generate molecule data.</span></span>  <span data-ttu-id="146d5-150">Met [EMSL Arrow Builder voor de Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) kunt u uw model invoeren met meerdere moleculaire model bouwers en het Broombridge gegevensbestand genereren dat door de Quantum Development Kit moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="146d5-150">[EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) allows you to enter your model using multiple molecular model builders and generate the Broombridge datafile to be used by the Quantum Development Kit.</span></span>  

<span data-ttu-id="146d5-151">Klik op de pagina EMSL op het tabblad [' instuctions '] en volg de instructies voor [' eenvoudige voor beelden '] om Broombridge-bestanden te genereren.</span><span class="sxs-lookup"><span data-stu-id="146d5-151">From the EMSL page, click on the ['Instuctions'] tab, and follow the ['Simple Examples'] instructions to generate Broombridge files.</span></span>  <span data-ttu-id="146d5-152">Probeer vervolgens [' GetGateCount '] uit te voeren om de Quantum resource schattingen voor deze moleculen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="146d5-152">Then try running the ['GetGateCount'] to see the quantum resource estimates for these molecules.</span></span>

### <a name="installing-nwchem-from-source"></a><span data-ttu-id="146d5-153">NWChem installeren vanuit de bron</span><span class="sxs-lookup"><span data-stu-id="146d5-153">Installing NWChem from Source</span></span>

<span data-ttu-id="146d5-154">Volledige instructies voor het installeren van NWChem vanaf de bron [zijn afkomstig van PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span><span class="sxs-lookup"><span data-stu-id="146d5-154">Full instructions on how to install NWChem from source [are provided by PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span></span>

> [!TIP]
> <span data-ttu-id="146d5-155">Als u NWChem van Windows 10 wilt gebruiken, is het Windows-subsysteem voor Linux een uitstekende optie.</span><span class="sxs-lookup"><span data-stu-id="146d5-155">If you wish to use NWChem from Windows 10, the Windows Subsystem for Linux is a great option.</span></span>
> <span data-ttu-id="146d5-156">Nadat u [Ubuntu 18,04 LTS voor Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)hebt geïnstalleerd, voert u `ubuntu18.04` uit vanuit uw favoriete terminal en volgt u de bovenstaande instructies om NWChem van de bron te installeren.</span><span class="sxs-lookup"><span data-stu-id="146d5-156">Once you have installed [Ubuntu 18.04 LTS for Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), run `ubuntu18.04` from your favorite terminal and follow the instructions above to install NWChem from source.</span></span>

<span data-ttu-id="146d5-157">Wanneer u NWChem hebt gecompileerd vanuit de bron, kunt u het `yaml_driver` script uitvoeren dat is opgegeven met NWChem om snel Broombridge-instanties te maken op basis van NWChem-invoer dekken:</span><span class="sxs-lookup"><span data-stu-id="146d5-157">Once you have compiled NWChem from source, you can run the `yaml_driver` script provided with NWChem to quickly produce Broombridge instances from NWChem input decks:</span></span>

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

<span data-ttu-id="146d5-158">Met deze opdracht wordt een nieuw `input.yaml`-bestand gemaakt in de Broombridge-indeling in de huidige map.</span><span class="sxs-lookup"><span data-stu-id="146d5-158">This command will create a new `input.yaml` file in the Broombridge format within your current directory.</span></span>

### <a name="using-nwchem-with-docker"></a><span data-ttu-id="146d5-159">NWChem gebruiken met docker</span><span class="sxs-lookup"><span data-stu-id="146d5-159">Using NWChem with Docker</span></span>

<span data-ttu-id="146d5-160">Vooraf gemaakte installatie kopieën voor het gebruik van NWChem zijn beschikbaar voor meerdere platforms via [docker hub](https://hub.docker.com).</span><span class="sxs-lookup"><span data-stu-id="146d5-160">Pre-built images for using NWChem are available cross-platform via [Docker Hub](https://hub.docker.com).</span></span>
<span data-ttu-id="146d5-161">Volg de installatie-instructies voor docker voor uw platform om aan de slag te gaan:</span><span class="sxs-lookup"><span data-stu-id="146d5-161">To get started, follow the Docker installation instructions for your platform:</span></span>

- [<span data-ttu-id="146d5-162">Docker voor Ubuntu installeren</span><span class="sxs-lookup"><span data-stu-id="146d5-162">Install Docker for Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [<span data-ttu-id="146d5-163">Docker voor macOS installeren</span><span class="sxs-lookup"><span data-stu-id="146d5-163">Install Docker for macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)
- [<span data-ttu-id="146d5-164">Docker voor Windows 10 installeren</span><span class="sxs-lookup"><span data-stu-id="146d5-164">Install Docker for Windows 10</span></span>](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> <span data-ttu-id="146d5-165">Als u docker voor Windows gebruikt, moet u het station met de tijdelijke map delen (dit is meestal het `C:\` station) met de docker-daemon.</span><span class="sxs-lookup"><span data-stu-id="146d5-165">If you are using Docker for Windows, you will need to share the drive containing your temporary directory (usually this is the `C:\` drive) with the Docker daemon.</span></span> <span data-ttu-id="146d5-166">Raadpleeg de [docker-documentatie](https://docs.docker.com/docker-for-windows/#shared-drives) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="146d5-166">See the [Docker documentation](https://docs.docker.com/docker-for-windows/#shared-drives) for more details.</span></span>

<span data-ttu-id="146d5-167">Zodra u docker hebt geïnstalleerd, kunt u de Power shell-module van de Quantum Development Kit-voor beelden gebruiken om de installatie kopie uit te voeren, of u kunt de installatie kopie hand matig uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="146d5-167">Once you have Docker installed, you can either use the PowerShell module provided with the Quantum Development Kit samples to run the image, or you can run the image manually.</span></span>
<span data-ttu-id="146d5-168">Hier vindt u informatie over het gebruik van Power shell. Als u de docker-installatie kopie hand matig wilt gebruiken, raadpleegt u de [documentatie van de installatie kopie](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span><span class="sxs-lookup"><span data-stu-id="146d5-168">We detail using PowerShell here; if you would like to use the Docker image manually, please see the [documentation provided with the image](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span></span>

#### <a name="running-nwchem-through-powershell-core"></a><span data-ttu-id="146d5-169">NWChem uitvoeren via Power shell core</span><span class="sxs-lookup"><span data-stu-id="146d5-169">Running NWChem through PowerShell Core</span></span>

<span data-ttu-id="146d5-170">Als u de NWChem docker-installatie kopie wilt gebruiken met de Quantum Development Kit, bieden we een kleine Power shell-module die het verplaatsen van bestanden in en uit NWChem voor u verzorgt.</span><span class="sxs-lookup"><span data-stu-id="146d5-170">To use the NWChem Docker image with the Quantum Development Kit, we provide a small PowerShell module that handles moving files in and out of NWChem for you.</span></span>
<span data-ttu-id="146d5-171">Als u de Power shell-kern nog niet hebt geïnstalleerd, kunt u deze cross-platform downloaden vanuit de [Power shell-opslag plaats op github](https://github.com/PowerShell/PowerShell#get-powershell).</span><span class="sxs-lookup"><span data-stu-id="146d5-171">If you don't already have PowerShell Core installed, you can download it cross-platform from the [PowerShell repository on GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span></span>

> [!NOTE]
> <span data-ttu-id="146d5-172">Power shell core wordt ook gebruikt voor enkele voor beelden voor het demonstreren van interoperabiliteit met data Science en Business Analytics-werk stromen.</span><span class="sxs-lookup"><span data-stu-id="146d5-172">PowerShell Core is also used for some samples to demonstrate interoperability with data science and business analytics workflows.</span></span>

<span data-ttu-id="146d5-173">Zodra u Power shell core hebt geïnstalleerd, importeert u `InvokeNWChem.psm1` om NWChem-opdrachten beschikbaar te maken in uw huidige sessie:</span><span class="sxs-lookup"><span data-stu-id="146d5-173">Once you have PowerShell Core installed, import `InvokeNWChem.psm1` to make NWChem commands available in your current session:</span></span>

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

<span data-ttu-id="146d5-174">Hiermee wordt de `Convert-NWChemToBroombridge`-opdracht beschikbaar gemaakt in uw huidige Power shell-sessie.</span><span class="sxs-lookup"><span data-stu-id="146d5-174">This will make the `Convert-NWChemToBroombridge` command available in your current PowerShell session.</span></span>
<span data-ttu-id="146d5-175">Voer het volgende uit om de benodigde installatie kopieën van docker te downloaden en te gebruiken voor het uitvoeren van NWChem-invoer dekken en het vastleggen van uitvoer naar Broombridge:</span><span class="sxs-lookup"><span data-stu-id="146d5-175">To download any needed images from Docker and use them to run NWChem input decks and capture output to Broombridge, run the following:</span></span>

```powershell
Convert-NWChemToBroombridge ./input.nw
```

<span data-ttu-id="146d5-176">Hiermee maakt u een Broombridge-bestand door NWChem uit te voeren op `input.nw`.</span><span class="sxs-lookup"><span data-stu-id="146d5-176">This will create a Broombridge file by running NWChem on `input.nw`.</span></span>
<span data-ttu-id="146d5-177">De Broombridge-uitvoer heeft standaard dezelfde naam en hetzelfde pad als het invoer deck, waarbij de uitbrei ding `.nw` door `.yaml`is vervangen.</span><span class="sxs-lookup"><span data-stu-id="146d5-177">By default, the Broombridge output will have the same name and path as the input deck, with the `.nw` extension replaced by `.yaml`.</span></span>
<span data-ttu-id="146d5-178">Dit kan worden overschreven door gebruik te maken van de para meter `-DestinationPath` om `Convert-NWChemToBroombridge`.</span><span class="sxs-lookup"><span data-stu-id="146d5-178">This can be overridden by using the `-DestinationPath` parameter to `Convert-NWChemToBroombridge`.</span></span>
<span data-ttu-id="146d5-179">Meer informatie kan worden verkregen met behulp van de ingebouwde Help-functionaliteit van Power shell:</span><span class="sxs-lookup"><span data-stu-id="146d5-179">More information can be obtained by using PowerShell's built-in help functionality:</span></span>

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
