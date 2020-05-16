---
title: Kwantumcircuits
description: Meer informatie over het visueel weer geven van eenvoudige en complexe Quantum bewerkingen met Quantum circuit diagrammen.
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 43f14d67db76dabda34bf881ccbfae0bfd1784ff
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426616"
---
# <a name="quantum-circuits"></a><span data-ttu-id="0a183-103">Quantum circuits</span><span class="sxs-lookup"><span data-stu-id="0a183-103">Quantum Circuits</span></span>
<span data-ttu-id="0a183-104">Denk eens na over een ogen blik dat de unitary-trans formatie $ \Text{CNOT} _ {01} (H\otimes 1) $.</span><span class="sxs-lookup"><span data-stu-id="0a183-104">Consider for a moment the unitary transformation $\text{ CNOT}_{01}(H\otimes 1)$.</span></span>
<span data-ttu-id="0a183-105">Deze poort reeks is van fundamenteel belang voor Quantum Computing omdat hiermee een maximally Entangled-status van twee Qubit wordt gemaakt:</span><span class="sxs-lookup"><span data-stu-id="0a183-105">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="0a183-106">$ $ \mathrm{CNOT}_ {01} (H\otimes 1) \ket {00} = \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right), $ $</span><span class="sxs-lookup"><span data-stu-id="0a183-106">$$\mathrm{CNOT}_{01}(H\otimes 1)\ket{00} = \frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right),$$</span></span>

<span data-ttu-id="0a183-107">Bewerkingen met deze of meer complexiteit zijn alomtegenwoordige in Quantum-algoritmen en Quantum fout correctie, zodat het een uitstekende goed keuring vormt voor de visualisatie die een *Quantum diagram*wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="0a183-107">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram*.</span></span>
<span data-ttu-id="0a183-108">Het circuit diagram voor het voorbereiden van de Quantum status van deze maximally Entangled is:</span><span class="sxs-lookup"><span data-stu-id="0a183-108">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-109">![Circuit diagram voor een maximally Entangled-status van twee Qubit](~/media/1.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-109">![Circuit diagram for a maximally entangled two-qubit state](~/media/1.svg)</span></span>

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="0a183-110">Conventies van Quantum circuit diagram</span><span class="sxs-lookup"><span data-stu-id="0a183-110">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="0a183-111">Deze visuele taal voor Quantum bewerkingen kan beter digestible zijn dan het schrijven van de equivalente matrix wanneer u de conventies voor het uitdrukken van een Quantum circuit begrijpt.</span><span class="sxs-lookup"><span data-stu-id="0a183-111">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="0a183-112">Deze conventies worden hieronder besproken.</span><span class="sxs-lookup"><span data-stu-id="0a183-112">We review these conventions below.</span></span>

<span data-ttu-id="0a183-113">In een circuit diagram geeft elke ononderbroken lijn een Qubit of meer in het algemeen een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="0a183-113">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="0a183-114">Per Conventie is de bovenste regel Qubit REGI ster $0 $ en de rest wordt opeenvolgend gelabeld.</span><span class="sxs-lookup"><span data-stu-id="0a183-114">By convention, the top line is qubit register $0$ and the remainder are labeled sequentially.</span></span> <span data-ttu-id="0a183-115">Het bovenstaande voor beeld wordt weer gegeven als een actie op twee qubits (of gelijkwaardige twee registers die uit één Qubit bestaan).</span><span class="sxs-lookup"><span data-stu-id="0a183-115">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="0a183-116">Poorten die aan een of meer Qubit-registers fungeren, worden aangeduid als een doos.</span><span class="sxs-lookup"><span data-stu-id="0a183-116">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="0a183-117">Bijvoorbeeld het symbool</span><span class="sxs-lookup"><span data-stu-id="0a183-117">For example, the symbol</span></span>

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-118">![Symbool voor een Hadamard-bewerking die fungeert als een single-Qubit-REGI ster](~/media/2.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-118">![Symbol for a Hadamard operation acting on a single-qubit register](~/media/2.svg)</span></span>

<span data-ttu-id="0a183-119">is een [Hadamard](xref:microsoft.quantum.intrinsic.h) -bewerking die fungeert als een single-Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="0a183-119">is a [Hadamard](xref:microsoft.quantum.intrinsic.h) operation acting on a single-qubit register.</span></span>

<span data-ttu-id="0a183-120">Quantum-Gates worden in chronologische volg orde gerangschikt met de meest linkse poort als de poort die voor het eerst op de qubits is toegepast.</span><span class="sxs-lookup"><span data-stu-id="0a183-120">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="0a183-121">Met andere woorden, als u de draden bijhoudt als het gaat om de Quantum status, halen de draden de Quantum status door elk van de poorten in het diagram van links naar rechts.</span><span class="sxs-lookup"><span data-stu-id="0a183-121">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="0a183-122">Dat wil zeggen</span><span class="sxs-lookup"><span data-stu-id="0a183-122">That is to say</span></span> 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-123">![Diagram van Quantum-Gates dat links-naar-rechts wordt toegepast](~/media/3.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-123">![Diagram of quantum gates being applied left-to-right](~/media/3.svg)</span></span>

<span data-ttu-id="0a183-124">is de unitary matrix $CBA $.</span><span class="sxs-lookup"><span data-stu-id="0a183-124">is the unitary matrix $CBA$.</span></span>
<span data-ttu-id="0a183-125">Matrix vermenigvuldiging voldoet aan de tegenovergestelde Conventie: de meest rechtse matrix wordt eerst toegepast.</span><span class="sxs-lookup"><span data-stu-id="0a183-125">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="0a183-126">In Quantum-circuit diagrammen wordt echter de meest linkse poort toegepast eerst.</span><span class="sxs-lookup"><span data-stu-id="0a183-126">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="0a183-127">Dit verschil kan in de loop van Verwar ring zijn, dus het is belang rijk dat u weet dat dit aanzienlijk verschil is tussen de lineaire algebraic notatie en Quantum circuit diagrammen.</span><span class="sxs-lookup"><span data-stu-id="0a183-127">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="0a183-128">Invoer en uitvoer van Quantum circuits</span><span class="sxs-lookup"><span data-stu-id="0a183-128">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="0a183-129">Alle voor gaande voor beelden hebben precies hetzelfde aantal bedradingen (qubits) in een Quantum poort gezien als het aantal draden van de Quantum poort.</span><span class="sxs-lookup"><span data-stu-id="0a183-129">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="0a183-130">Het kan eerst redelijk zijn dat quantum circuits meer of minder uitvoer hebben dan invoer in het algemeen.</span><span class="sxs-lookup"><span data-stu-id="0a183-130">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="0a183-131">Dit is echter onmogelijk, omdat alle Quantum bewerkingen, het opslaan van metingen, unitary en dus omkeerbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="0a183-131">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="0a183-132">Als ze niet hetzelfde aantal uitvoer hebben als invoer, zouden ze niet omkeerbaar zouden zijn en dus niet unitary. Dit is een tegen strijdigheid.</span><span class="sxs-lookup"><span data-stu-id="0a183-132">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="0a183-133">Daarom moet elk vak dat in een circuit diagram wordt getekend, exact hetzelfde aantal draden hebben als het wordt afgesloten.</span><span class="sxs-lookup"><span data-stu-id="0a183-133">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="0a183-134">Multi-Qubit circuit diagrammen volgen vergelijk bare conventies voor enkelvoudige Qubit.</span><span class="sxs-lookup"><span data-stu-id="0a183-134">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="0a183-135">Een voor beeld hiervan is dat we een unitary-bewerking met twee Qubit definiëren $B $ (H S\otimes X) $ en het circuit gelijk geven aan</span><span class="sxs-lookup"><span data-stu-id="0a183-135">As a clarifying example, we can define a two-qubit unitary operation $B$ to be $(H S\otimes X)$ and express the circuit equivalently as</span></span>

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-136">![Circuit diagram van een unitary-bewerking met twee Qubit](~/media/4.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-136">![Circuit diagram of a two-qubit unitary operation](~/media/4.svg)</span></span>

<span data-ttu-id="0a183-137">We kunnen ook $B $ weer geven als een actie voor een enkele twee Qubit-registratie in plaats van 2 1-Qubit registreert, afhankelijk van de context waarin het circuit wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0a183-137">We can also view $B$ as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="0a183-138">Misschien is de meest nuttige eigenschap van dergelijke abstracte circuit diagrammen dat ze gecompliceerde Quantum algoritmen op een hoog niveau mogen worden beschreven, zonder dat ze hoeven te compileren op basis poorten.</span><span class="sxs-lookup"><span data-stu-id="0a183-138">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="0a183-139">Dit betekent dat u een Intuition voor de gegevens stroom kunt verkrijgen voor een grote Quantum algoritme zonder dat u alle details hoeft te begrijpen van de manier waarop elk van de subroutines binnen het algoritme werkt.</span><span class="sxs-lookup"><span data-stu-id="0a183-139">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="0a183-140">Bewaakte poorten</span><span class="sxs-lookup"><span data-stu-id="0a183-140">Controlled gates</span></span>
<span data-ttu-id="0a183-141">De andere constructie die is ingebouwd in multi-Qubit Quantum circuit diagrammen is Control.</span><span class="sxs-lookup"><span data-stu-id="0a183-141">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="0a183-142">De actie van een Quantum die is geïsoleerd als poort, heeft $ \Lambda (G) $, waarbij de waarde van één Qubit de toepassing van $G $, kan worden geïnterpreteerd door het volgende voor beeld van een product status invoer $ \Lambda (G) (\alpha \ket {0} + \beta \ket {1} ) \ket{\psi} = \alpha \ket {0} \ket{\psi} + \beta \ket {1} G\ket {\ psi} $ te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0a183-142">The action of a quantum singly controlled gate, denoted $\Lambda(G)$, where a single qubit's value controls the application of $G$, can be understood by looking at the following example of a product state input $\Lambda(G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket{\psi}$.</span></span>
<span data-ttu-id="0a183-143">Dat wil zeggen dat de bewaakte Gate $G $ toepast op het REGI ster met $ \psi $ als en alleen als het besturings element Qubit de waarde $1 $ heeft.</span><span class="sxs-lookup"><span data-stu-id="0a183-143">That is to say, the controlled gate applies $G$ to the register containing $\psi$ if and only if the control qubit takes the value $1$.</span></span>
<span data-ttu-id="0a183-144">Over het algemeen beschrijven we dergelijke beheerde bewerkingen in circuit diagrammen als</span><span class="sxs-lookup"><span data-stu-id="0a183-144">In general, we describe such controlled operations in circuit diagrams as</span></span>

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-145">![Circuit diagram van een poort die afzonderlijk wordt gecontroleerd](~/media/5.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-145">![Circuit diagram of a singly controlled gate](~/media/5.svg)</span></span>

<span data-ttu-id="0a183-146">Hier geeft de zwarte cirkel de Quantum bit aan waarop de poort wordt gecontroleerd en een verticale bedrading de unitary die wordt toegepast wanneer het besturings element Qubit de waarde $1 $ heeft.</span><span class="sxs-lookup"><span data-stu-id="0a183-146">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value $1$.</span></span>
<span data-ttu-id="0a183-147">Voor de speciale gevallen waarin $G = X $ en $G = Z $, introduceren we de volgende notatie om de bewaakte versie van de poorten te beschrijven (Houd er rekening mee dat de Controlled-X-Gate de [$CNOT $ Gate](xref:microsoft.quantum.intrinsic.cnot)) is:</span><span class="sxs-lookup"><span data-stu-id="0a183-147">For the special cases where $G=X$ and $G=Z$ we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [$CNOT$ gate](xref:microsoft.quantum.intrinsic.cnot)):</span></span>

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-148">![Circuit diagram voor speciale gevallen van gecontroleerde poorten](~/media/6.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-148">![Circuit diagram for special cases of controlled gates](~/media/6.svg)</span></span>

<span data-ttu-id="0a183-149">Q # biedt methoden voor het automatisch genereren van de bewaakte versie van een bewerking, waardoor de programmeur van de hand om deze bewerkingen te hoeven coderen.</span><span class="sxs-lookup"><span data-stu-id="0a183-149">Q# provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="0a183-150">Hieronder ziet u een voor beeld van dit:</span><span class="sxs-lookup"><span data-stu-id="0a183-150">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a><span data-ttu-id="0a183-151">Meet operator</span><span class="sxs-lookup"><span data-stu-id="0a183-151">Measurement operator</span></span>
<span data-ttu-id="0a183-152">De resterende bewerking voor het visualiseren van circuit diagrammen is meting.</span><span class="sxs-lookup"><span data-stu-id="0a183-152">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="0a183-153">Meting neemt een Qubit-REGI ster, meet dit en voert het resultaat uit als klassieke informatie.</span><span class="sxs-lookup"><span data-stu-id="0a183-153">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="0a183-154">Een meting bewerking wordt aangeduid met een meter symbool en gaat altijd als invoer een Qubit-REGI ster (aangeduid met een ononderbroken lijn) en voert klassieke informatie uit (aangeduid met een dubbele lijn).</span><span class="sxs-lookup"><span data-stu-id="0a183-154">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="0a183-155">Met name een dergelijk subcircuit ziet er als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="0a183-155">Specifically, such a subcircuit looks like:</span></span>

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-156">![Symbool dat een meting bewerking vertegenwoordigt](~/media/7.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-156">![Symbol representing a measurement operation](~/media/7.svg)</span></span>

<span data-ttu-id="0a183-157">Q # implementeert een [meet operator](xref:microsoft.quantum.intrinsic.measure) voor dit doel.</span><span class="sxs-lookup"><span data-stu-id="0a183-157">Q# implements a [Measure operator](xref:microsoft.quantum.intrinsic.measure) for this purpose.</span></span>
<span data-ttu-id="0a183-158">Zie de [sectie over metingen](xref:microsoft.quantum.libraries.standard.prelude#measurements) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0a183-158">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="0a183-159">Op dezelfde manier wordt het subcircuit</span><span class="sxs-lookup"><span data-stu-id="0a183-159">Similarly, the subcircuit</span></span>

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="0a183-160">![Circuit diagram dat een bewaakte bewerking vertegenwoordigt](~/media/8.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-160">![Circuit diagram representing a controlled operation](~/media/8.svg)</span></span>

<span data-ttu-id="0a183-161">geeft een klassieke, gecontroleerde poort, waarbij $G $ wordt toegepast op de waarde van het klassieke besturings element bit $1 $.</span><span class="sxs-lookup"><span data-stu-id="0a183-161">gives a classically controlled gate, where $G$ is applied conditioned on the classical control bit being value $1$.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="0a183-162">Circuit diagram teleportatie</span><span class="sxs-lookup"><span data-stu-id="0a183-162">Teleportation circuit diagram</span></span>
<span data-ttu-id="0a183-163">Quantum-teleportie is misschien het beste Quantum algoritme voor het illustreren van deze onderdelen.</span><span class="sxs-lookup"><span data-stu-id="0a183-163">Quantum teleportation is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="0a183-164">U kunt aan de slag met de bijbehorende Quantum [Kata](xref:microsoft.quantum.overview.katas) Quantum teleportal is een methode voor het verplaatsen van gegevens binnen een quantum computer (of zelfs tussen quantum computers in een Quantum netwerk) met behulp van entanglement en meting.</span><span class="sxs-lookup"><span data-stu-id="0a183-164">You can learn hands-on with the corresponding [Quantum Kata](xref:microsoft.quantum.overview.katas) Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="0a183-165">Het is interessant om een Quantum status te verplaatsen, de waarde in een bepaalde Qubit te zeggen van een Qubit naar een andere, zonder dat u weet wat de waarde van de Qubit is.</span><span class="sxs-lookup"><span data-stu-id="0a183-165">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="0a183-166">Dit is nodig om het protocol te laten werken volgens de wetten van Quantum-garages.</span><span class="sxs-lookup"><span data-stu-id="0a183-166">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="0a183-167">Het Quantum teleportal-circuit wordt hieronder gegeven. We bieden ook een geannoteerde versie van het circuit om te laten zien hoe het Quantum circuit kan worden gelezen.</span><span class="sxs-lookup"><span data-stu-id="0a183-167">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<!--- ![](.\media\tp2.svg){ width=50% } --->
<span data-ttu-id="0a183-168">![Quantum teleportisatie-circuit](~/media/tp2.svg)</span><span class="sxs-lookup"><span data-stu-id="0a183-168">![Quantum teleportation circuit](~/media/tp2.svg)</span></span>
