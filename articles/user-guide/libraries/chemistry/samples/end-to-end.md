---
title: Voor beeld van een NWChem Quantum-programma
description: Door een NWChem-invoer deck te gebruiken, loopt u een voor beeld van het ophalen van poort aantallen voor de simulatie van de quantum chemie.
author: cgranade
ms.author: chgranad
ms.date: 10/23/2018
ms.topic: sample
uid: microsoft.quantum.chemistry.examples.endtoend
no-loc:
- Q#
- $$v
ms.openlocfilehash: e0ec7dcbdccbab5c81177a4223c71fd3f2ce57d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847764"
---
# <a name="end-to-end-with-nwchem"></a><span data-ttu-id="c1b53-103">End-to-end met NWChem</span><span class="sxs-lookup"><span data-stu-id="c1b53-103">End-to-end with NWChem</span></span> #

<span data-ttu-id="c1b53-104">In dit artikel vindt u een voor beeld van het ophalen van poort aantallen voor de simulatie van quantum chemie, beginnend bij een [NWChem](http://www.nwchem-sw.org/index.php/Main_Page) -invoer deck.</span><span class="sxs-lookup"><span data-stu-id="c1b53-104">In this article, you will walk through an example of getting gate counts for quantum chemistry simulation, starting from an [NWChem](http://www.nwchem-sw.org/index.php/Main_Page) input deck.</span></span>
<span data-ttu-id="c1b53-105">Controleer voordat u doorgaat met dit voor beeld of u docker hebt geïnstalleerd volgens de installatie- [en validatie handleiding](xref:microsoft.quantum.chemistry.concepts.installation).</span><span class="sxs-lookup"><span data-stu-id="c1b53-105">Before proceeding with this example, make sure that you've installed Docker, following the [installation and validation guide](xref:microsoft.quantum.chemistry.concepts.installation).</span></span>

<span data-ttu-id="c1b53-106">Voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="c1b53-106">For more information:</span></span>
- [<span data-ttu-id="c1b53-107">Structuur van NWChem-invoer dekken</span><span class="sxs-lookup"><span data-stu-id="c1b53-107">Structure of NWChem input decks</span></span>](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [<span data-ttu-id="c1b53-108">Invoer deck-opdrachten voor gebruik met de Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="c1b53-108">Input deck commands for use with the Quantum Development Kit</span></span>](https://github.com/nwchemgit/nwchem/tree/main/contrib/quasar)
- [<span data-ttu-id="c1b53-109">De schei-bibliotheek en de afhankelijkheden worden geïnstalleerd</span><span class="sxs-lookup"><span data-stu-id="c1b53-109">Installing the chemistry library and dependencies</span></span>](xref:microsoft.quantum.chemistry.concepts.installation)
- [<span data-ttu-id="c1b53-110">Resources tellen</span><span class="sxs-lookup"><span data-stu-id="c1b53-110">Resource counting</span></span>](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> <span data-ttu-id="c1b53-111">Voor dit voor beeld moet Windows Power shell core worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c1b53-111">This example requires Windows PowerShell Core to run.</span></span>
> <span data-ttu-id="c1b53-112">Down load Power shell core voor Windows, macOS of Linux op https://github.com/PowerShell/PowerShell .</span><span class="sxs-lookup"><span data-stu-id="c1b53-112">Download PowerShell Core for Windows, macOS, or Linux at https://github.com/PowerShell/PowerShell.</span></span>

## <a name="importing-required-powershell-modules"></a><span data-ttu-id="c1b53-113">Vereiste Power shell-modules importeren</span><span class="sxs-lookup"><span data-stu-id="c1b53-113">Importing Required PowerShell Modules</span></span> ##

<span data-ttu-id="c1b53-114">Als u dit nog niet hebt gedaan, kloont u de [micro soft/Quantum-opslag plaats](https://github.com/Microsoft/Quantum)met voor beelden en hulpprogram ma's voor het werken met de Quantum Development Kit:</span><span class="sxs-lookup"><span data-stu-id="c1b53-114">If you haven't already done so, clone the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum), which contains samples and utilities for working with the Quantum Development Kit:</span></span>

```powershell
git clone https://github.com/Microsoft/Quantum
```

<span data-ttu-id="c1b53-115">Zodra u bent gekloond `Microsoft/Quantum` , voert u `cd` de volgende opdracht uit in de `utilities/` map en importeert u de Power shell-module voor het werken met docker en NWChem:</span><span class="sxs-lookup"><span data-stu-id="c1b53-115">Once you've cloned `Microsoft/Quantum`, perform `cd` into the `utilities/` folder and import the PowerShell module for working with Docker and NWChem:</span></span>

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> <span data-ttu-id="c1b53-116">Windows voor komt standaard dat er scripts of modules worden uitgevoerd als beveiligings maatregel.</span><span class="sxs-lookup"><span data-stu-id="c1b53-116">By default, Windows prevents the running of any scripts or modules as a security measure.</span></span>
> <span data-ttu-id="c1b53-117">Als u modules wilt toestaan die `Invoke-NWChem.psm1` worden uitgevoerd in Windows, moet u het beleid mogelijk wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c1b53-117">To allow modules such as `Invoke-NWChem.psm1` to run on Windows, you may need to change the policy.</span></span>
> <span data-ttu-id="c1b53-118">U doet dit door de opdracht uit te voeren `Set-ExecutionPolicy` :</span><span class="sxs-lookup"><span data-stu-id="c1b53-118">To do so, run the `Set-ExecutionPolicy` command:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> <span data-ttu-id="c1b53-119">Het beleid wordt hersteld wanneer u Power shell afsluit.</span><span class="sxs-lookup"><span data-stu-id="c1b53-119">The policy will revert when you exit PowerShell.</span></span>
> <span data-ttu-id="c1b53-120">Als u het beleid wilt opslaan, gebruikt u een andere waarde voor `-Scope` :</span><span class="sxs-lookup"><span data-stu-id="c1b53-120">If you would like to save the policy, use a different value for `-Scope`:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

<span data-ttu-id="c1b53-121">U hebt nu de `Convert-NWChemToBroombridge` volgende opdracht:</span><span class="sxs-lookup"><span data-stu-id="c1b53-121">You should now have the `Convert-NWChemToBroombridge` command available:</span></span>

```powershell
Get-Command -Module InvokeNWChem
```

<span data-ttu-id="c1b53-122">Vervolgens importeren we de `Get-GateCount` opdracht die is opgenomen in het **GetGateCount** -voor beeld.</span><span class="sxs-lookup"><span data-stu-id="c1b53-122">Next, we'll import the `Get-GateCount` command provided with the **GetGateCount** sample.</span></span>
<span data-ttu-id="c1b53-123">Zie de instructies van het voor [beeld](https://github.com/Microsoft/Quantum/tree/main/samples/chemistry/GetGateCount)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c1b53-123">For full details, see the [instructions provided with the sample](https://github.com/Microsoft/Quantum/tree/main/samples/chemistry/GetGateCount).</span></span>
<span data-ttu-id="c1b53-124">Voer vervolgens de volgende handelingen uit en vervang deze door `<runtime>` `win10-x64` of, `osx-x64` `linux-x64` afhankelijk van uw besturings systeem:</span><span class="sxs-lookup"><span data-stu-id="c1b53-124">Next, run the following, substituting `<runtime>` with either `win10-x64`, `osx-x64`, or `linux-x64`, depending on your operating system:</span></span>

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

<span data-ttu-id="c1b53-125">U hebt nu de `Get-GateCount` volgende opdracht:</span><span class="sxs-lookup"><span data-stu-id="c1b53-125">You should now have the `Get-GateCount` command available:</span></span>

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a><span data-ttu-id="c1b53-126">Invoer dekken</span><span class="sxs-lookup"><span data-stu-id="c1b53-126">Input Decks</span></span> ##

<span data-ttu-id="c1b53-127">Het NWChem-pakket neemt een tekst bestand met de naam een _invoer deck_ op waarmee een Quantum oplossings probleem wordt aangegeven dat moet worden opgelost, samen met andere para meters, zoals geheugen toewijzings instellingen.</span><span class="sxs-lookup"><span data-stu-id="c1b53-127">The NWChem package takes a text file called an _input deck_ which specifies a quantum chemistry problem to be solved, along with other parameters such as memory allocation settings.</span></span>
<span data-ttu-id="c1b53-128">In dit voor beeld gebruiken we een van de vooraf gemaakte invoer dekken die worden geleverd met NWChem.</span><span class="sxs-lookup"><span data-stu-id="c1b53-128">For this example, we'll use one of the pre-made input decks that comes with NWChem.</span></span>
<span data-ttu-id="c1b53-129">Kloon eerst de [opslag plaats nwchemgit/NWChem](https://github.com/nwchemgit/nwchem):</span><span class="sxs-lookup"><span data-stu-id="c1b53-129">First, clone the [nwchemgit/nwchem repository](https://github.com/nwchemgit/nwchem):</span></span>

> [!NOTE]
> <span data-ttu-id="c1b53-130">Omdat dit een zeer grote opslag plaats is, kunnen we een beschik bare kloon van de band breedte en schijf ruimte besparen met behulp van het `--depth 1` argument.</span><span class="sxs-lookup"><span data-stu-id="c1b53-130">Since this is a very large repository, we can do a shallow clone to save some bandwidth and disk space, using the `--depth 1` argument.</span></span>
> <span data-ttu-id="c1b53-131">Dit is echter optioneel.</span><span class="sxs-lookup"><span data-stu-id="c1b53-131">This is optional, however.</span></span>
> <span data-ttu-id="c1b53-132">Klonen werkt gewoon zonder `--depth 1` .</span><span class="sxs-lookup"><span data-stu-id="c1b53-132">Cloning will work just fine without `--depth 1`.</span></span>

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

<span data-ttu-id="c1b53-133">De `nwchemgit/nwchem` opslag plaats wordt geleverd met diverse invoer dekken die zijn bedoeld voor gebruik met de Quantum Development Kit, die wordt weer gegeven in de [ `QA/chem_library_tests` map](https://github.com/nwchemgit/nwchem/tree/main/QA/chem_library_tests).</span><span class="sxs-lookup"><span data-stu-id="c1b53-133">The `nwchemgit/nwchem` repository comes with a variety of input decks intended for use with the Quantum Development Kit, listed under the [`QA/chem_library_tests` folder](https://github.com/nwchemgit/nwchem/tree/main/QA/chem_library_tests).</span></span>
<span data-ttu-id="c1b53-134">In dit voor beeld gebruiken we het `H4` invoer deck:</span><span class="sxs-lookup"><span data-stu-id="c1b53-134">For this example, we'll use the `H4` input deck:</span></span>

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

<span data-ttu-id="c1b53-135">Het betrokken molecuul is een systeem van 4 waterstof atomen dat is gerangschikt in een bepaalde geometrie die afhankelijk is van één hoek, de para meter `alpha` zoals aangegeven in de naam `h4_sto6g_alpha.nw` van het dek.</span><span class="sxs-lookup"><span data-stu-id="c1b53-135">The molecule in question is a system of 4 hydrogen atoms that are arranged in a certain geometry that depends on one angle, the parameter `alpha` as indicated in the name `h4_sto6g_alpha.nw` of the deck.</span></span> <span data-ttu-id="c1b53-136">H4 is een bekend [molecuul referentie](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) punt voor reken kundige schei kunde sinds de jaren zeventig.</span><span class="sxs-lookup"><span data-stu-id="c1b53-136">H4 is a known [molecular benchmark](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) for computational chemistry since the 1970s.</span></span> <span data-ttu-id="c1b53-137">De para meter `sto6g` is indicatief dat de-dek een representatie implementeert met betrekking tot een Slater Orbital, met name een vertegenwoordiging met betrekking tot een [Waarschuwingsd-aardgas set](https://en.wikipedia.org/wiki/STO-nG_basis_sets) met 6 Gaussiaans basis functies.</span><span class="sxs-lookup"><span data-stu-id="c1b53-137">The parameter `sto6g` is indicative that the deck implements a representation with respect to a Slater-type orbital, specifically, a representation with respect to an [STO-nG basis set](https://en.wikipedia.org/wiki/STO-nG_basis_sets) with 6 Gaussian basis functions.</span></span> <span data-ttu-id="c1b53-138">Deze invoer deck bevat ook verschillende instructies voor de NWChem tensor-inrichtings Engine (TCE) waarmee NWChem de benodigde informatie voor samen werking met de Quantum Development Kit kunt produceren:</span><span class="sxs-lookup"><span data-stu-id="c1b53-138">This input deck furthermore contains several instructions to the NWChem Tensor Contraction Engine (TCE) that direct NWChem to produce the information needed for interoperating with the Quantum Development Kit:</span></span>

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a><span data-ttu-id="c1b53-139">Produceren en gebruiken van Broombridge-uitvoer van NWChem</span><span class="sxs-lookup"><span data-stu-id="c1b53-139">Producing and Consuming Broombridge Output from NWChem</span></span> ##

<span data-ttu-id="c1b53-140">U hebt nu alles wat u nodig hebt om Broombridge-documenten te maken en te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c1b53-140">You now have everything you need to produce and consume Broombridge documents.</span></span>
<span data-ttu-id="c1b53-141">Als u NWChem wilt uitvoeren en een Broombridge-document wilt maken voor het `h4_sto6g_0.000.nw` invoer deck, voert u de `Convert-NWChemToBroombridge` volgende handelingen uit:</span><span class="sxs-lookup"><span data-stu-id="c1b53-141">To run NWChem and produce a Broombridge document for the `h4_sto6g_0.000.nw` input deck, run `Convert-NWChemToBroombridge`:</span></span>

> [!NOTE]
> <span data-ttu-id="c1b53-142">De eerste keer dat u deze opdracht uitvoert, wordt de installatie kopie door docker `nwchemorg/nwchem-qc` voor u gedownload.</span><span class="sxs-lookup"><span data-stu-id="c1b53-142">The first time you run this command, Docker will download the `nwchemorg/nwchem-qc` image for you.</span></span>
> <span data-ttu-id="c1b53-143">Dit kan even duren, afhankelijk van de verbindings snelheid, waardoor u mogelijk een kopje koffie krijgt.</span><span class="sxs-lookup"><span data-stu-id="c1b53-143">This may take a little while, depending on your connection speed, possibly providing an opportunity to get a cup of coffee.</span></span>

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

<span data-ttu-id="c1b53-144">Er wordt een Broombridge-document gemaakt `h4_sto6g_0.000.yaml` met de naam die u kunt gebruiken met `Get-GateCount` :</span><span class="sxs-lookup"><span data-stu-id="c1b53-144">This will produce a Broombridge document called `h4_sto6g_0.000.yaml` that you can use with `Get-GateCount`:</span></span>

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

<span data-ttu-id="c1b53-145">U ziet nu de console-uitvoer die de resource schatting bevat, zoals T-aantal, rotaties aantal, CNOT aantal enzovoort. voor verschillende Quantum simulatie methoden:</span><span class="sxs-lookup"><span data-stu-id="c1b53-145">You should now see console output which contains resource estimation such as T-count, rotations count, CNOT count, etc. for various quantum simulation methods:</span></span>

```powershell 
IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Trotter
TCount              : 0
RotationsCount      : 92
CNOTCount           : 520
ElapsedMilliseconds : 327

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Qubitization
TCount              : 438
RotationsCount      : 516
CNOTCount           : 2150
ElapsedMilliseconds : 528

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Optimized Qubitization
TCount              : 3540
RotationsCount      : 18
CNOTCount           : 7932
ElapsedMilliseconds : 721
```

<span data-ttu-id="c1b53-146">U kunt op de volgende manieren te werk gaan:</span><span class="sxs-lookup"><span data-stu-id="c1b53-146">There are many things to go do from here:</span></span> 
- <span data-ttu-id="c1b53-147">Probeer verschillende vooraf gedefinieerde invoer dekken, bijvoorbeeld door de para meter `alpha` in te variëren in `h4_sto6g_alpha.nw`</span><span class="sxs-lookup"><span data-stu-id="c1b53-147">Try out different predefined input decks, e.g., by varying the parameter `alpha` in `h4_sto6g_alpha.nw`,</span></span> 
- <span data-ttu-id="c1b53-148">Wijzig de dekken door de NWChem-dekken rechtstreeks te bewerken, bijvoorbeeld om modellen te verkennen `STO-nG` voor verschillende keuzes van n,</span><span class="sxs-lookup"><span data-stu-id="c1b53-148">Try modifying the decks by editing the NWChem decks directly, e.g., exploring `STO-nG` models for various choices of n,</span></span> 
- <span data-ttu-id="c1b53-149">Probeer andere vooraf gedefinieerde NWChem-invoer dekken die beschikbaar zijn op `nwchem/qa/chem_library_tests` ,</span><span class="sxs-lookup"><span data-stu-id="c1b53-149">Try other predefined NWChem input decks that are available at `nwchem/qa/chem_library_tests`,</span></span>
- <span data-ttu-id="c1b53-150">Probeer een reeks vooraf gedefinieerde Broombridge YAML-benchmarks die zijn gegenereerd op basis van NWChem en die beschikbaar zijn als onderdeel van de [micro soft/Quantum-opslag plaats](https://github.com/Microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML).</span><span class="sxs-lookup"><span data-stu-id="c1b53-150">Try out a suite of predefined Broombridge YAML benchmarks that were generated from NWChem and are available as part of the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML).</span></span> <span data-ttu-id="c1b53-151">Deze benchmarks zijn onder andere:</span><span class="sxs-lookup"><span data-stu-id="c1b53-151">These benchmarks include:</span></span> 
    - <span data-ttu-id="c1b53-152">kleine moleculen zoals moleculaire water stof (H2), beryllium (as), lithium hydride (LiH),</span><span class="sxs-lookup"><span data-stu-id="c1b53-152">small molecules such as molecular hydrogen (H2), Beryllium (Be), Lithium hydride (LiH),</span></span>
    - <span data-ttu-id="c1b53-153">grotere moleculen, zoals ozon (O3), bèta-carotene, cytosine en nog veel meer.</span><span class="sxs-lookup"><span data-stu-id="c1b53-153">larger molecules such as ozone (O3), beta-carotene, cytosine, and many more.</span></span> 
- <span data-ttu-id="c1b53-154">Probeer de grafische front-end [EMSL-pijlen](https://arrows.emsl.pnnl.gov/api/qsharp_chem) uit die een interface aan de Microsoft Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="c1b53-154">Try out the graphical front-end [EMSL Arrows](https://arrows.emsl.pnnl.gov/api/qsharp_chem) that features an interface to the Microsoft Quantum Development Kit.</span></span> 


## <a name="producing-broombridge-output-from-emsl-arrows"></a><span data-ttu-id="c1b53-155">Broombridge-uitvoer genereren op basis van EMSL-pijlen</span><span class="sxs-lookup"><span data-stu-id="c1b53-155">Producing Broombridge Output from EMSL Arrows</span></span> ##

<span data-ttu-id="c1b53-156">Als u aan de slag wilt met webgebaseerde front end EMSL-pijlen, navigeert u [hier](https://arrows.emsl.pnnl.gov/api/qsharp_chem)in een browser.</span><span class="sxs-lookup"><span data-stu-id="c1b53-156">To get started with web-based front end EMSL Arrows, navigate a browser [here](https://arrows.emsl.pnnl.gov/api/qsharp_chem).</span></span> 

> [!NOTE]
> <span data-ttu-id="c1b53-157">Voor het uitvoeren van EMSL-pijlen in een webbrowser moet Java script worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c1b53-157">Running EMSL Arrows in a web browser requires JavaScript to be enabled.</span></span> <span data-ttu-id="c1b53-158">Raadpleeg deze [instructies](https://www.enable-javascript.com/) voor het inschakelen van Java script in uw browser.</span><span class="sxs-lookup"><span data-stu-id="c1b53-158">Please refer to these [instructions](https://www.enable-javascript.com/) on how to enable JavaScript in your browser.</span></span> 

<span data-ttu-id="c1b53-159">Voer eerst een molecuul in in het query-vak met de tekst ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span><span class="sxs-lookup"><span data-stu-id="c1b53-159">First, enter a molecule in the query box that says ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span></span> 

<span data-ttu-id="c1b53-160">U kunt een groot aantal moleculen invoeren op basis van hun colloquial-naam, zoals "cafeïne" in plaats van "1, 3, 7-Trimethylxanthine".</span><span class="sxs-lookup"><span data-stu-id="c1b53-160">You can enter many molecules by their colloquial name, such as "caffeine" instead of "1,3,7-Trimethylxanthine".</span></span> 

<span data-ttu-id="c1b53-161">Klik vervolgens op de knop met de tekst ``theory{qsharp_chem}`` .</span><span class="sxs-lookup"><span data-stu-id="c1b53-161">Next, click the button that says ``theory{qsharp_chem}``.</span></span> <span data-ttu-id="c1b53-162">Hiermee wordt het query-vak verder gevuld met een instructie waarmee wordt aangegeven dat de uitvoer in de Broombridge YAML-indeling moet worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="c1b53-162">This will populate the query box further with an instruction that will tell the run to export output in the Broombridge YAML format.</span></span> 

<span data-ttu-id="c1b53-163">Klok nu in ``Run Arrows`` .</span><span class="sxs-lookup"><span data-stu-id="c1b53-163">Now, clock on ``Run Arrows``.</span></span> <span data-ttu-id="c1b53-164">Afhankelijk van de grootte van de invoer kan dit enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="c1b53-164">Depending on the size of the input, this might take a while.</span></span> <span data-ttu-id="c1b53-165">Als het specifieke model al eerder is berekend, kan het echter zeer snel worden uitgevoerd, omdat het alleen in een zoek actie in een Data Base is.</span><span class="sxs-lookup"><span data-stu-id="c1b53-165">Or, in case the particular model has already been computed before, it can be done extremely fast as it will only amount to a lookup in a database.</span></span> <span data-ttu-id="c1b53-166">In beide gevallen gaat u naar een nieuwe pagina die een verdwaald bevat met informatie over de specifieke uitvoering van NWChem voor het dek dat is opgegeven door uw invoer.</span><span class="sxs-lookup"><span data-stu-id="c1b53-166">In either case, you will be taken to a new page that contains a plethora of information about the particular run of NWChem against the deck specified by your input.</span></span> 

<span data-ttu-id="c1b53-167">U kunt het Broombridge YAML-bestand downloaden en opslaan in de sectie die begint met de volgende header:</span><span class="sxs-lookup"><span data-stu-id="c1b53-167">You can download and save the Broombridge YAML file from the section that starts with the following header:</span></span> 
```powershell
+==================================================+
||              Molecular Calculation             ||
+==================================================+

Id     = 48443

NWOutput = Link to NWChem Output (download)

Datafiles:
qsharp_chem.yaml-2018-10-23-14:37:42 (download)
...
```

<span data-ttu-id="c1b53-168">Klik op aan ``download`` , waarmee een lokale kopie wordt opgeslagen met een unieke bestands naam, zoals ``qsharp_chem48443.yaml`` (de specifieke naam voor elke uitvoering verschilt).</span><span class="sxs-lookup"><span data-stu-id="c1b53-168">Click on ``download``, which saves a local copy with a unique file name such as ``qsharp_chem48443.yaml`` (the particular name will be different for each run).</span></span> <span data-ttu-id="c1b53-169">U kunt dit bestand vervolgens net zo verder verwerken als hierboven, bijvoorbeeld met</span><span class="sxs-lookup"><span data-stu-id="c1b53-169">You can then further process this file as above, e.g., with</span></span> 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
<span data-ttu-id="c1b53-170">om het aantal resources op te halen.</span><span class="sxs-lookup"><span data-stu-id="c1b53-170">to get resource counts.</span></span> 

<span data-ttu-id="c1b53-171">U kunt gebruikmaken van de 3D-moleculen Builder die toegankelijk is via het ``Arrows Entry - 3D Builder`` tabblad op de start pagina van de EMSL-pijlen.</span><span class="sxs-lookup"><span data-stu-id="c1b53-171">You might enjoy the 3D molecule builder that can be accessed from the ``Arrows Entry - 3D Builder`` tab on the EMSL Arrows start page.</span></span> <span data-ttu-id="c1b53-172">Als u op de [JSMol](http://wiki.jmol.org/index.php/JSmol) 3D-afbeelding van het weer gegeven molecuul klikt, kunt u deze bewerken.</span><span class="sxs-lookup"><span data-stu-id="c1b53-172">Clicking the [JSMol](http://wiki.jmol.org/index.php/JSmol) 3D picture of the shown molecule will let you allow to edit it.</span></span> <span data-ttu-id="c1b53-173">U kunt atomen verplaatsen. Sleep atomen uit elkaar zodat de intermoleculaire afstanden veranderen, atomen toevoegen/verwijderen, enzovoort. Voor elk van deze opties kunt u, nadat u hebt toegevoegd ``theory{qsharp_chem}`` in het query-vak, een exemplaar van het BROOMBRIDGE YAML-schema genereren en het vervolgens verder verkennen met behulp van de quantum chemie-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="c1b53-173">You can move atoms around, drag atoms apart so that their inter-molecular distances change, add/remove atoms, etc. For each of these choices, once you added ``theory{qsharp_chem}`` in the query box, you can then generate an instance of the Broombridge YAML schema and further explore it using the Quantum Chemistry Library.</span></span> 
