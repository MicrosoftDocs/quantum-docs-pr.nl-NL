---
title: Voor beeld van een NWChem Quantum-programma
description: Door een NWChem-invoer deck te gebruiken, loopt u een voor beeld van het ophalen van poort aantallen voor de simulatie van de quantum chemie.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/23/2018
uid: microsoft.quantum.chemistry.examples.endtoend
ms.openlocfilehash: 7605676e05ee352e47791657eeaafceef5dbb493
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022498"
---
# <a name="end-to-end-with-nwchem"></a>End-to-end met NWChem #

In dit artikel vindt u een voor beeld van het ophalen van poort aantallen voor de simulatie van quantum chemie, beginnend bij een [NWChem](http://www.nwchem-sw.org/index.php/Main_Page) -invoer deck.
Controleer voordat u doorgaat met dit voor beeld of u docker hebt geïnstalleerd volgens de installatie- [en validatie handleiding](xref:microsoft.quantum.chemistry.concepts.installation).

Voor meer informatie:
- [Structuur van NWChem-invoer dekken](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [Invoer deck-opdrachten voor gebruik met de Quantum Development Kit](https://github.com/nwchemgit/nwchem/tree/master/contrib/quasar)
- [De schei-bibliotheek en de afhankelijkheden worden geïnstalleerd](xref:microsoft.quantum.chemistry.concepts.installation)
- [Resources tellen](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> Voor dit voor beeld moet Windows Power shell core worden uitgevoerd.
> Down load Power shell core voor Windows, macOS of Linux op https://github.com/PowerShell/PowerShell.

## <a name="importing-required-powershell-modules"></a>Vereiste Power shell-modules importeren ##

Als u dit nog niet hebt gedaan, kloont u de [micro soft/Quantum-opslag plaats](https://github.com/Microsoft/Quantum)met voor beelden en hulpprogram ma's voor het werken met de Quantum Development Kit:

```powershell
git clone https://github.com/Microsoft/Quantum
```

Nadat u `Microsoft/Quantum`hebt gekloond, voert u `cd` uit in de map `utilities/` en importeert u de Power shell-module voor het werken met docker en NWChem:

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> Standaard wordt voor komen dat scripts of modules worden uitgevoerd als beveiligings maatregel.
> Als u wilt toestaan dat modules zoals `Invoke-NWChem.psm1` worden uitgevoerd in Windows, moet u het uitvoerings beleid mogelijk wijzigen.
> U doet dit door de `Set-ExecutionPolicy` opdracht uit te voeren:
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> Het uitvoerings beleid wordt dan teruggezet wanneer u Power shell afsluit.
> Als u het uitvoerings beleid wilt opslaan, gebruikt u een andere waarde voor `-Scope`:
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

U hebt nu de `Convert-NWChemToBroombridge`-opdracht beschikbaar:

```powershell
Get-Command -Module InvokeNWChem
```

Vervolgens importeren we de `Get-GateCount`-opdracht die is opgenomen in het **GetGateCount** -voor beeld.
Zie de instructies van het voor [beeld](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount)voor meer informatie.
Voer vervolgens de volgende handelingen uit en vervang `<runtime>` door `win10-x64`, `osx-x64`of `linux-x64`, afhankelijk van uw besturings systeem:

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

U hebt nu de `Get-GateCount`-opdracht beschikbaar:

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a>Invoer dekken ##

Het NWChem-pakket neemt een tekst bestand met de naam een _invoer deck_ op waarmee een Quantum oplossings probleem wordt aangegeven dat moet worden opgelost, samen met andere para meters, zoals geheugen toewijzings instellingen.
In dit voor beeld gebruiken we een van de vooraf gemaakte invoer dekken die worden geleverd met NWChem.
Kloon eerst de [opslag plaats nwchemgit/NWChem](https://github.com/nwchemgit/nwchem):

> [!NOTE]
> Omdat dit een zeer grote opslag plaats is, kunnen we een beschik bare kloon van de band breedte en schijf ruimte besparen met behulp van het argument `--depth 1`.
> Dit is echter optioneel.
> Klonen werkt alleen zonder `--depth 1`.

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

De `nwchemgit/nwchem`-opslag plaats wordt geleverd met diverse invoer dekken die zijn bedoeld voor gebruik met de Quantum Development Kit, die wordt weer gegeven in de [map`QA/chem_library_tests`](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests).
In dit voor beeld gebruiken we het `H4`-invoer deck:

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

Het betrokken molecuul is een systeem van 4 waterstof atomen dat is gerangschikt in een bepaalde geometrie die afhankelijk is van één hoek, de para meter `alpha` zoals aangegeven in de naam `h4_sto6g_alpha.nw` van het dek. H4 is een bekend [molecuul referentie](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) punt voor reken kundige schei kunde sinds de jaren zeventig. De para meter `sto6g` is indicatief dat het deck een representatie implementeert met betrekking tot een Slater Orbital, met name een vertegenwoordiging met betrekking tot een [waarschuwingsd-aardgas set](https://en.wikipedia.org/wiki/STO-nG_basis_sets) met 6 Gaussiaans basis functies. Deze invoer deck bevat ook verschillende instructies voor de NWChem tensor-inrichtings Engine (TCE) waarmee NWChem de benodigde informatie voor samen werking met de Quantum Development Kit kunt produceren:

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a>Produceren en gebruiken van Broombridge-uitvoer van NWChem ##

U hebt nu alles wat u nodig hebt om Broombridge-documenten te maken en te gebruiken.
Als u NWChem wilt uitvoeren en een Broombridge-document wilt maken voor het `h4_sto6g_0.000.nw`-invoer deck, voert u `Convert-NWChemToBroombridge`uit:

> [!NOTE]
> De eerste keer dat u deze opdracht uitvoert, zal docker de `nwchemorg/nwchem-qc`-installatie kopie voor u downloaden.
> Dit kan even duren, afhankelijk van de verbindings snelheid, waardoor u mogelijk een kopje koffie krijgt.

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

Hiermee wordt een Broombridge-document gemaakt met de naam `h4_sto6g_0.000.yaml` die u met `Get-GateCount`kunt gebruiken:

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

U ziet nu de console-uitvoer die de resource schatting bevat, zoals T-aantal, rotaties aantal, CNOT aantal enzovoort. voor verschillende Quantum simulatie methoden:

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

U kunt op de volgende manieren te werk gaan: 
- Probeer verschillende vooraf gedefinieerde invoer dekken, bijvoorbeeld door de para meter `alpha` in `h4_sto6g_alpha.nw`te variëren. 
- Wijzig de dekken door de NWChem-dekken rechtstreeks te bewerken, bijvoorbeeld om `STO-nG` modellen te verkennen voor verschillende keuzes van n, 
- Probeer andere vooraf gedefinieerde NWChem-invoer dekken die beschikbaar zijn op `nwchem/qa/chem_library_tests`,
- Probeer een reeks vooraf gedefinieerde Broombridge YAML-benchmarks die zijn gegenereerd op basis van NWChem en die beschikbaar zijn als onderdeel van de [micro soft/Quantum-opslag plaats](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML). Deze benchmarks zijn onder andere: 
    - kleine moleculen zoals moleculaire water stof (H2), beryllium (as), lithium hydride (LiH),
    - grotere moleculen, zoals ozon (O3), bèta-carotene, cytosine en nog veel meer. 
- Probeer de grafische front-end [EMSL-pijlen](https://arrows.emsl.pnnl.gov/api/qsharp_chem) uit die een interface aan de Microsoft Quantum Development Kit. 


## <a name="producing-broombridge-output-from-emsl-arrows"></a>Broombridge-uitvoer genereren op basis van EMSL-pijlen ##

Als u aan de slag wilt met webgebaseerde front end EMSL-pijlen, navigeert u [hier](https://arrows.emsl.pnnl.gov/api/qsharp_chem)in een browser. 

> [!NOTE]
> Voor het uitvoeren van EMSL-pijlen in een webbrowser moet Java script worden ingeschakeld. Raadpleeg deze [instructies](https://www.enable-javascript.com/) voor het inschakelen van Java script in uw browser. 

Voer eerst een molecuul in in het query-vak met de tekst ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.`` 

U kunt een groot aantal moleculen invoeren op basis van hun colloquial-naam, zoals "cafeïne" in plaats van "1, 3, 7-Trimethylxanthine". 

Klik vervolgens op de knop met de tekst ``theory{qsharp_chem}``. Hiermee wordt het query-vak verder gevuld met een instructie waarmee wordt aangegeven dat de uitvoer in de Broombridge YAML-indeling moet worden geëxporteerd. 

Klok nu in ``Run Arrows``. Afhankelijk van de grootte van de invoer kan dit enige tijd duren. Als het specifieke model al eerder is berekend, kan het echter zeer snel worden uitgevoerd, omdat het alleen in een zoek actie in een Data Base is. In beide gevallen gaat u naar een nieuwe pagina die een verdwaald bevat met informatie over de specifieke uitvoering van NWChem voor het dek dat is opgegeven door uw invoer. 

U kunt het Broombridge YAML-bestand downloaden en opslaan in de sectie die begint met de volgende header: 
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

Klik op ``download``, waarmee een lokale kopie wordt opgeslagen met een unieke bestands naam, zoals ``qsharp_chem48443.yaml`` (de betreffende naam verschilt voor elke uitvoering). U kunt dit bestand vervolgens net zo verder verwerken als hierboven, bijvoorbeeld met 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
om het aantal resources op te halen. 

U kunt gebruikmaken van de 3D-molecuul Builder die toegankelijk is via het tabblad ``Arrows Entry - 3D Builder`` op de start pagina EMSL Arrows. Als u op de [JSMol](http://wiki.jmol.org/index.php/JSmol) 3D-afbeelding van het weer gegeven molecuul klikt, kunt u deze bewerken. U kunt atomen verplaatsen. Sleep atomen uit elkaar zodat de intermoleculaire afstanden veranderen, atomen toevoegen/verwijderen, enzovoort. Voor elk van deze keuzes kunt u, nadat u ``theory{qsharp_chem}`` hebt toegevoegd in het query venster, een exemplaar van het Broombridge YAML-schema genereren en het vervolgens verder verkennen met behulp van de quantum chemie-bibliotheek. 
