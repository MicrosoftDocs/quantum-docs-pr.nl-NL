---
title: Hamiltonian Dynamics simuleren
description: Meer informatie over het gebruik van Trotter-Suzuki-formules en qubitization voor het werken met Hamiltonian-simulaties.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
ms.openlocfilehash: e3ce76f5ddcca497adb519eece959c9dd5dec92f
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904635"
---
# <a name="simulating-hamiltonian-dynamics"></a>Hamiltonian Dynamics simuleren

Zodra de Hamiltonian is uitgedrukt als som van elementaire Opera Tors, kan de dynamiek vervolgens worden gecompileerd in fundamentele poort bewerkingen met behulp van een host van bekende technieken.
Drie efficiënte benaderingen zijn Trotter: Suzuki formules, lineaire combi Naties van unitaries en qubitization.
Deze drie benaderingen worden hieronder beschreven en geven concrete Q # voor beelden van hoe u deze methoden implementeert met behulp van de Hamiltonian simulatie bibliotheek.


## <a name="trottersuzuki-formulas"></a>Trotter – Suzuki formules
Het idee achter Trotter – Suzuki formules is eenvoudig: de Hamiltonian als som van het eenvoudig simuleren van Hamiltonians en de totale evolutie te benaderen als een reeks van deze eenvoudigere evoluties.
U kunt met name $H = \ sum_ {j = 1} ^ m H_j $ de Hamiltonian zijn.
Then $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \ prod_ {j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $. dat wil zeggen dat, als $t \ll $1, de fout in deze benadering verwaarloosbaar is.
Als $e ^ {-i H t} $ een normale exponentiële waarde was, zou de fout in deze benadering niet worden $O (m ^ 2 t ^ 2) $: de waarde is nul.
Deze fout treedt op omdat $e ^ {-iHt} $ een operator exponentiële is. als gevolg hiervan is er een fout opgetreden bij het gebruik van deze formule als gevolg van het feit dat de $H _j $-voor waarden niet werken (*dat wil zeggen*$H _J H_k \ne H_k H_j $ in het algemeen).

Als $t $ groot is, kunnen er nog steeds Trotter-Suzuki formules worden gebruikt om de dynamiek nauw keurig te simuleren door deze op te splitsen in een reeks korte fases.
Laat $r $ het aantal stappen dat wordt uitgevoerd in de tijd evolutie.
Vervolgens hebben we dat $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \left (\ prod_ {j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r), $ $, wat impliceert dat als $r $ wordt geschaald als $m ^ 2 t ^ 2/\ Epsilon $, de fout kan worden gemaakt Maxi maal $ \epsilon $ voor $ \epsilon > 0 $.

Nauw keurigere benaderingen kunnen worden gemaakt door een reeks operator exponentiëlen te maken, zodat de fout voorwaarden worden geannuleerd.
De eenvoudigste van deze formule, de symmetrische Trotter formule of Strang splitsen, heeft de notatie $ $ U_1 (t) = \ prod_ {j = 1} ^ m e ^ {-iH_j t/2} \ prod_ {j = m} ^ 1 e ^ {-iH_j t} = e ^ {-iHt} + O (m ^ 3 t ^ 3), $ $ die minder dan $ \epsilon $ kan worden gemaakt voor $ \epsilon > 0 $ door $r $ te schalen als $m ^ {3/2} t ^ {3/2}/\sqrt {\ Epsilon} $.

Zelfs Trotter formules met een hogere volg orde kunnen worden samengesteld op basis van $U _1 $.
Het eenvoudigste is de volgende formule in de vierde volg orde, oorspronkelijk geïntroduceerd door Suzuki: $ $ U_2 (t) = U_1 ^ 2 (s_1t) U_1 ([1-4s_1] t) U_1 ^ 2 (s_1 t) = e ^ {-iHt} + O (m ^ 5T ^ 5), $ $ waar $s _1 = (4-4 ^ {1/3}) ^{-1}$.
In het algemeen kunnen wille keurige formules met een hoge volg orde worden geconstrueerd. de kosten voor het gebruik van complexere integrators zijn echter vaak zwaarder dan de voor delen van de meeste praktische problemen.

Om de bovenstaande strategieën te laten werken, moeten we een methode hebben voor het simuleren van een brede klasse van $e ^ {-iH_j t} $.
De eenvoudigste familie van Hamiltonians en weliswaar het handigst, die we hier kunnen gebruiken, zijn Pauli Opera tors.
Pauli-Opera tors kunnen gemakkelijk worden gesimuleerd, omdat ze kunnen worden gediagonaalt met behulp van Clifford-bewerkingen (die standaard Gates zijn in Quantum Computing).
Nadat de eigenvalues zijn gediagonaalt, kunnen ze worden gevonden door de pariteit van de qubits waarop ze handelen te berekenen.

Bijvoorbeeld: $ $ e ^ {-iX\otimes X t} = (H\otimes H) e ^ {-iZ\otimes Z t} (H\otimes H), $ $ waarbij $ $ e ^ {-i Z \otimes Z t} = \begin{bmatrix} e ^ {-IT} & 0 & 0 & 0 \\\
        0 & e ^ {i t} & 0 & 0 \\\
        0 & 0 & e ^ {IT} & 0 \\\
        0 & 0 & 0 & e ^ {-it} \end{bmatrix}.
$ $ Hier $e ^ {-iHt} \ket{00} = e ^ {it} \ket{00}$ en $e ^ {-iHt} \ket{01} = e ^ {-it} \ket{01}$, die rechtstreeks kan worden gezien als gevolg van het feit dat de pariteit van $0 $ $0 $ is, terwijl de pariteit van de bit teken reeks $1 $ $1 $ is.

Exponentiële waarde van Pauli-Opera tors kunnen rechtstreeks in Q # worden geïmplementeerd met behulp van de <xref:microsoft.quantum.intrinsic.exp> bewerking:
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies 𝑒^{- 𝑖 𝑋⊗𝑋 𝑡} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

Voor Fermionic Hamiltonians wijst de [Jordanië – Wigner](xref:microsoft.quantum.chemistry.concepts.jordanwigner) de Hamiltonian handig toe aan een som van Pauli-Opera tors.
Dit betekent dat de bovenstaande aanpak eenvoudig kan worden aangepast aan het simuleren van de schei kunde.
In plaats van hand matig te herhalen over alle Pauli-voor waarden in de Wigner-vertegenwoordiging, hieronder volgt een eenvoudig voor beeld van hoe u een dergelijke simulatie binnen de schei kunde uitvoert.
Ons begin punt is een [Jordanië – Wigner-code ring](xref:microsoft.quantum.chemistry.concepts.jordanwigner) van de Fermionic Hamiltonian, uitgedrukt in code als een exemplaar van de klasse `JordanWignerEncoding`.

```csharp
    // This example uses the following namespaces:
    // using Microsoft.Quantum.Chemistry.OrbitalIntegrals;
    // using Microsoft.Quantum.Chemistry.Fermion;
    // using Microsoft.Quantum.Chemistry.Pauli;
    // using Microsoft.Quantum.Chemistry.QSharpFormat;

    // We create an instance of the `FermionHamiltonian` objecclasst to store the terms.
    var hamiltonian = new OrbitalIntegralHamiltonian(new[] 
    {
        new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123),
        new OrbitalIntegral(new[] { 0, 1 }, 0.456)
    }).ToFermionHamiltonian(IndexConvention.UpDown);

    // We convert this fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = hamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);

    // We now convert this representation into a format consumable by Q#.
    var qSharpData = jordanWignerEncoding.ToQSharpFormat();
```

Deze indeling van de Wigner-representatie die kan worden gebruikt door de Q #-simulatie algoritmen is een door de gebruiker gedefinieerd type `JordanWignerEncodingData`.
Binnen Q # wordt deze indeling door gegeven aan een gebruiks vriendelijke functie `TrotterStepOracle` die een operator met geschatte tijd schommelt met behulp van de Trotter-Suzuki integrator, naast de andere para meters die vereist zijn voor de uitvoering ervan.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single time-step.
using(qubits = Qubit[nQubits]){

    // Apply single step of time-evolution
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

Belang rijk: deze implementatie past een aantal optimalisaties toe die worden besproken in de [simulatie van de elektronische structuur Hamiltonians met behulp van quantum computers](https://arxiv.org/abs/1001.3855) en [verbeteren Quantum algoritmen voor quantum chemie](https://arxiv.org/abs/1403.1539) om het aantal vereiste draaiingen voor één Qubit te beperken, en om simulatie fouten te verminderen.

## <a name="qubitization"></a>Qubitization

Qubitization is een alternatieve aanpak voor simulatie waarbij ideeën van Quantum worden gebruikt om de Quantum dynamiek te simuleren.
Hoewel qubitization meer qubits dan Trotter formules vereist, biedt de methode een optimale schaal aanpassing met de ontwikkelings tijd en de fout tolerantie.
Daarom is het een aanbevolen methode geworden voor het simuleren van Hamiltonian Dynamics in het algemeen en voor het oplossen van het probleem met de elektronische structuur.

Op hoog niveau voert qubitization de volgende stappen uit.
Laat eerst $H = \ sum_j h_j H_j $ voor unitary en Hermitian $H _J $ en $h _j \ge $0.
Door een paar reflecties uit te voeren, implementeert qubitization een operator die gelijk is aan $ $W = e ^ {\pm i \cos ^{-1}(H/| H | _1)}, $ $ waarbij $ | H | _1 = \ sum_j | h_j | $.
De volgende stap omvat het transformeren van de eigenvalues van de Walk-operator van $e ^ {i\pm \cos ^{-1}(E_k/| h | _1)} $, waarbij $E _k $ de eigenvalues van $H $ is $e ^ {-iE_k t} $.
Dit kan worden bereikt met behulp van diverse Quantum-waarden transformatie methoden, waaronder [Quantum signaal verwerking](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).

Als er echter alleen statische hoeveel heden gewenst zijn (zoals de grond energie van de Hamiltonian), is het voldoende om de fase- [schatting](xref:microsoft.quantum.libraries.characterization) rechtstreeks toe te passen op $W $ om de grond energie van het resultaat te schatten door de cosinus van het resultaat te nemen.
Dit is belang rijk omdat de Spectral-trans formatie klassiek kan worden uitgevoerd in plaats van een Quantum waarde transformatie methode te gebruiken.

Op een meer gedetailleerd niveau vereist de implementatie van qubitization twee subroutines die de interfaces bieden voor de Hamiltonian.
In tegens telling tot Trotter-Suzuki-methoden zijn deze subroutines Quantum niet klassiek en is de implementatie nood zakelijk om logarithmically meer qubits te gebruiken dan nodig is voor een op Trotter gebaseerde simulatie.

De eerste Quantum subroutine die qubitization gebruikt, heet $ \operatorname{Select} $ en is toegezegd om \begin{Equation} \operatorname{Select} \ket{j} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{Equation} te leveren waarbij elke $H _j $ wordt aangenomen dat het gaat om Hermitian en unitary.
Hoewel dit waarschijnlijk beperkend lijkt, herinnert u zich dat Pauli-Opera tors Hermitian en unitary zijn, en dat toepassingen zoals de simulatie van quantum chemie natuurlijk in dit kader vallen.
De $ \operatorname{Select} $-bewerking, mogelijk verrassend, is eigenlijk een reflectie bewerking.
Dit kan worden gezien uit het feit dat $ \operatorname{Select} ^ 2 \ Ket {j} \ket{\psi} = \ket{j} \ket{\psi} $ sinds elke $H _j $ unitary en Hermitian is en dus eigenvalues $ \pm $1.

De tweede subroutine heet $ \operatorname{Prepare} $.
Hoewel de Select-bewerking een manier biedt om de Hamiltonian-voor waarden op een samenhangende wijze te benaderen $H _j $ de subroutine voor bereiding de methode heeft om toegang te krijgen tot de coëfficiënten $h _j $, \begin{Equation} \operatorname{Prepare}\ket{0} = \ sum_j \sqrt{\frac{h_j} {| H | _1}} \ket{j}.
\end{Equation} ziet u vervolgens met behulp van een geteste gestuurde Phase-Gate dat $ $ \Lambda\ket{0}^ {\otimes n} = \begin{cases} \-\ket{x} & \Text{if} x = 0 \\\
        \ket{x} & \Text{otherwise} \end{cases}.
$$

De $ \operatorname{Prepare} $-bewerking wordt niet rechtstreeks in qubitization gebruikt, maar wordt in plaats daarvan gebruikt voor het implementeren van een reflectie over de status die $ \operatorname{Prepare} $ $ $ \begin{align} R &amp; = 1-2 \ operatornaam {Prepare} \ket{0}\bra{0} \operatorname{Prepare} ^{-1} \\\\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare} ^{-1}.
\end{align} $ $

De Walk-operator, $W $, kan worden uitgedrukt in termen van $ \operatorname{Select} $ en $R $-bewerkingen als $ $ W = \operatorname{Select} R, $ $. Dit kan worden gezien als een operator die equivalent is (Maxi maal een isometry) kan worden geïmplementeerd om te $e ^ {\pm i \cos ^{-1}(H/| h | _1)} $.

Deze subroutines kunnen eenvoudig worden ingesteld in Q #.
Denk bijvoorbeeld aan de eenvoudige Qubit-transversale Ising Hamiltonian waarbij $H = X_1 + X_2 + Z_1 Z_2 $.
In dit geval wordt Q # code waarmee de $ \operatorname{Select} $-bewerking zou worden geïmplementeerd, aangeroepen door <xref:microsoft.quantum.canon.multiplexoperations>, terwijl de $ \operatorname{Prepare} $-bewerking kan worden geïmplementeerd met behulp van <xref:microsoft.quantum.preparation.preparearbitrarystate>.
Een voor beeld van het simuleren van het Hubbard model kan worden gevonden als een [Q #](https://github.com/microsoft/Quantum/tree/master/samples/simulation/hubbard)-voor beeld.

Het hand matig opgeven van deze stappen voor wille keurige schei problemen zou veel moeite vergen, wat wordt voor komen met behulp van de Library chemie.
Op dezelfde manier als het simulatie algoritme Trotter-Suzuki wordt de `JordanWignerEncodingData` door gegeven aan de functie voor gemak `QubitizationOracle` die de Walk-operator retourneert, naast de andere para meters die vereist zijn voor de uitvoering ervan.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/oneNorm`, where oneNorm is the sum of absolute values of all probabilities in state prepared by `Prepare`.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  QubitizationOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single step of the quantum walk.
using(qubits = Qubit[nQubits]){

    // Apply single step of quantum walk.
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

Het is belang rijk dat de implementatie <xref:microsoft.quantum.chemistry.jordanwigner.qubitizationoracle> van toepassing is op een wille keurige Hamiltonians die is opgegeven als een lineaire combi natie van Pauli-teken reeksen.
Een versie die is geoptimaliseerd voor chemie-simulaties, wordt aangeroepen met behulp van <xref:microsoft.quantum.chemistry.jordanwigner.optimizedqubitizationoracle>.
Deze versie is geoptimaliseerd om het aantal T-poorten te minimaliseren met behulp van technieken die worden beschreven in de [code ring van elektronische spectra in Quantum circuits met lineaire-T-complexiteit](https://arxiv.org/abs/1805.03662).
