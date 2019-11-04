---
title: Een Hamiltonian laden vanuit het bestand | Microsoft Docs
description: Een Hamiltonian laden vanuit bestands documenten
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.loadhamiltonian
ms.openlocfilehash: 9902e95b09d38323b4b91c29ab897a4f0124b6cd
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184182"
---
## <a name="loading-a-hamiltonian-from-file"></a>Een Hamiltonian laden vanuit een bestand
Voorheen hebben we Hamiltonians gemaakt door afzonderlijke voor waarden toe te voegen. Hoewel dit een kleine voor beeld is, is voor Quantum-schei kunde op schaal Hamiltonians met miljoenen of miljarden voor waarden vereist. Dergelijke Hamiltonians, die zijn gegenereerd door chemie pakketten zoals NWChem, zijn te groot om met de hand te worden geïmporteerd. In dit voor beeld laten we zien hoe een `FermionHamiltonian` exemplaar automatisch kan worden gegenereerd op basis van een molecuul dat wordt vertegenwoordigd door het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge). Ter referentie kan één het gegeven `LithiumHydrideGUI` voor beeld controleren of het `RunSimulation`-voor beeld. Beperkte ondersteuning is ook beschikbaar voor importeren vanuit de indeling die wordt gebruikt door [LIQUi | >](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/).

Laten we eens kijken naar het voor beeld van het stikstof molecuul, dat is opgenomen in de map `IntegralData/YAML` van de opslag plaats voor beelden. De methode voor het laden van het `Broombridge` schema is eenvoudig.

```csharp
// This is the name of the file we want to load
var filename = @"n2_1_00Re_sto3g.nw.out.yaml";
// This is the directory containing the file
var root = @"IntegralData\YAML";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge($@"{root}\{filename}");

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.First()`, which selects the first element of the list.
var problem = broombridge.ProblemDescriptions.First();

// This extracts the `OrbitalIntegralHamiltonian` from Broombridge format,
// then converts it to a fermion Hamiltonian, then to a Jordan-Wigner
// representation.
var orbitalIntegralHamiltonian = problem.OrbitalIntegralHamiltonian;
var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);
var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);
```

Het Broombridge-schema bevat ook suggesties voor de oorspronkelijke status die moet worden voor bereid. De labels, bijvoorbeeld `"|G⟩"` of `"|E1⟩"`, voor deze statussen kunnen worden weer gegeven door het bestand te controleren. Om deze initiële statussen voor te bereiden, wordt de `qSharpData` die wordt gebruikt door de Q # Quantum-algoritmen verkregen op dezelfde manier als de [vorige sectie](xref:microsoft.quantum.chemistry.examples.energyestimate), maar met een extra para meter die de gewenste begin status selecteert. Bijvoorbeeld,
```csharp
// The desired initial state, assuming that a description of it is present in the
// Broombridge schema.
var state = "|E1>";
var wavefunction = problem.Wavefunctions[state].ToIndexing(IndexConvention.UpDown);

// This creates the qSharpData consumable by the Q# chemistry library algorithms.
var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
var qSharpWavefunctionData = wavefunction.ToQSharpFormat();
var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Alle bovenstaande stappen kunnen worden afgekort door gebruik te maken van de volgende gebruiks vriendelijke methoden.
```csharp
// This is the name of the file we want to load
var filename = "...";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge(filename);

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.Single()`, which selects the only element of the list.
var problem = broombridge.ProblemDescriptions.Single();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
// If no state is specified, the Hartree-Fock state is used by default.
var qSharpData = problem.ToQSharpFormat("|E1>");
```

We kunnen ook een Hamiltonian laden vanuit de LIQUi | >-indeling, met een vergelijk bare syntaxis. 

```csharp
// This is the name of the file we want to load
var filename = @"fe2s2_sto3g.dat"; // This is Ferrodoxin.
// This is the directory containing the file
var root = @"IntegralData\Liquid";

// Deserialize the LiQuiD format.
var problem = LiQuiD.Deserialize($@"{root}\{filename}").First();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
var qSharpData = problem.ToQSharpFormat();
```

Door dit proces te volgen vanuit een wille keurig exemplaar van Broombridge of een wille keurige stap, kunnen Quantum algoritmen, zoals de Quantum Phase-schatting, worden uitgevoerd op het opgegeven elektronische structuur probleem.