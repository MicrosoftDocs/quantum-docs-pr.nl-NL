---
title: Q# technieken - Alles in elkaar zetten
description: Loop door een basis Q# programma dat kwantumteleportatie demonstreert.
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030562"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="5f01a-103">Putting It All Together: Teleportatie</span><span class="sxs-lookup"><span data-stu-id="5f01a-103">Putting It All Together: Teleportation</span></span> #
<span data-ttu-id="5f01a-104">Laten we terugkeren naar het voorbeeld van het teleportatiecircuit gedefinieerd in [Quantum Circuits.](xref:microsoft.quantum.concepts.circuits)</span><span class="sxs-lookup"><span data-stu-id="5f01a-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="5f01a-105">We gaan dit gebruiken om de concepten te illustreren die we tot nu toe hebben geleerd.</span><span class="sxs-lookup"><span data-stu-id="5f01a-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="5f01a-106">Een uitleg van quantum teleportatie is hieronder voorzien voor degenen die niet bekend zijn met de theorie, gevolgd door een walkthrough van de code implementatie in Q#.</span><span class="sxs-lookup"><span data-stu-id="5f01a-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="5f01a-107">Quantum Teleportatie: Theorie</span><span class="sxs-lookup"><span data-stu-id="5f01a-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="5f01a-108">Quantum teleportatie is een techniek voor het verzenden van een onbekende kwantumtoestand (die we zullen noemen de '__boodschap__') van een qubit op een locatie naar een qubit op een andere locatie (we zullen verwijzen naar deze qubits als '__hier__' en '__er__', respectievelijk).</span><span class="sxs-lookup"><span data-stu-id="5f01a-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="5f01a-109">We kunnen onze __boodschap__ als een vector vertegenwoordigen met Dirac-notatie:</span><span class="sxs-lookup"><span data-stu-id="5f01a-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="5f01a-110">$$ \ket{\psi} = \alpha\ket{0} +{1} \beta\ket $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="5f01a-111">De status van de __boodschap__ qubit is onbekend voor ons als we niet weten wat de waarden van $\alpha $ en $\beta$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="5f01a-112">Stap 1: Een verstrengelde toestand maken</span><span class="sxs-lookup"><span data-stu-id="5f01a-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="5f01a-113">Om het __bericht__ te sturen moeten we voor de qubit __hier__ te worden verstrikt met de qubit __daar__.</span><span class="sxs-lookup"><span data-stu-id="5f01a-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="5f01a-114">Dit wordt bereikt door het toepassen van een Hadamard poort, gevolgd door een CNOT poort.</span><span class="sxs-lookup"><span data-stu-id="5f01a-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="5f01a-115">Laten we eens kijken naar de wiskunde achter deze poort operaties.</span><span class="sxs-lookup"><span data-stu-id="5f01a-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="5f01a-116">We zullen beginnen met de qubits __hier__ en{0} __daar__ zowel in de $ \ ket $ staat.</span><span class="sxs-lookup"><span data-stu-id="5f01a-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="5f01a-117">Na het verwarren van deze qubits, zijn ze in de staat:</span><span class="sxs-lookup"><span data-stu-id="5f01a-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="5f01a-118">$$ \ket{\phi^+} ={1}\frac{2}{\sqrt{00} }(\ket + \ket{11}) $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="5f01a-119">Stap 2: Het bericht verzenden</span><span class="sxs-lookup"><span data-stu-id="5f01a-119">Step 2: Send the message</span></span>
<span data-ttu-id="5f01a-120">Om het __bericht__ te verzenden passen we eerst een CNOT-poort toe met de __message__ qubit en __hier__ qubit als inputs (het __bericht__ qubit is de controle en de __here__ qubit is het doel qubit, in dit geval).</span><span class="sxs-lookup"><span data-stu-id="5f01a-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="5f01a-121">Deze invoerstatus kan worden geschreven:</span><span class="sxs-lookup"><span data-stu-id="5f01a-121">This input state can be written:</span></span>

<span data-ttu-id="5f01a-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} +{1}\beta\ket)(\frac{1}{\sqrt{2}{00} {11}}(\ket + \ket)) $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="5f01a-123">Dit breidt zich uit naar:</span><span class="sxs-lookup"><span data-stu-id="5f01a-123">This expands to:</span></span>

<span data-ttu-id="5f01a-124">$${2}\ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{000} }\ket +{2}\frac{\alpha}{\sqrt }\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} +{2}\frac{\beta}{\sqrt }\ket{111} $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="5f01a-125">Ter herinnering, de CNOT-poort draait de doelqubit wanneer de controle qubit is 1.</span><span class="sxs-lookup"><span data-stu-id="5f01a-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="5f01a-126">Dus bijvoorbeeld, een input van{000}$\ket $ zal resulteren in geen verandering als de eerste qubit (het besturingselement) is 0.</span><span class="sxs-lookup"><span data-stu-id="5f01a-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="5f01a-127">Neem echter een geval waarbij de eerste qubit 1 is{100}- bijvoorbeeld een invoer van $\ket $.</span><span class="sxs-lookup"><span data-stu-id="5f01a-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="5f01a-128">In dit geval is de{110}uitvoer $\ket $ als de tweede qubit (het doel) wordt omgedraaid door de CNOT-poort.</span><span class="sxs-lookup"><span data-stu-id="5f01a-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="5f01a-129">Laten we nu overwegen onze output zodra de CNOT poort heeft gehandeld op onze input hierboven.</span><span class="sxs-lookup"><span data-stu-id="5f01a-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="5f01a-130">Het resultaat is:</span><span class="sxs-lookup"><span data-stu-id="5f01a-130">The result is:</span></span>

<span data-ttu-id="5f01a-131">$${2}\frac{\alpha}{\sqrt }\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="5f01a-132">De volgende stap om het __bericht__ te verzenden is het toepassen van een Hadamard poort op het __bericht__ qubit (dat is de eerste qubit van elke term).</span><span class="sxs-lookup"><span data-stu-id="5f01a-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="5f01a-133">Ter herinnering, de Hadamard poort doet het volgende:</span><span class="sxs-lookup"><span data-stu-id="5f01a-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="5f01a-134">Invoer</span><span class="sxs-lookup"><span data-stu-id="5f01a-134">Input</span></span> | <span data-ttu-id="5f01a-135">Uitvoer</span><span class="sxs-lookup"><span data-stu-id="5f01a-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="5f01a-136">$\ket{0}$</span><span class="sxs-lookup"><span data-stu-id="5f01a-136">$\ket{0}$</span></span>  | <span data-ttu-id="5f01a-137">$\frac{1}{\sqrt{2}}(\ket{0} {1}+ \ket )$</span><span class="sxs-lookup"><span data-stu-id="5f01a-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="5f01a-138">$\ket{1}$</span><span class="sxs-lookup"><span data-stu-id="5f01a-138">$\ket{1}$</span></span>  | <span data-ttu-id="5f01a-139">$\frac{1}{\sqrt{2}}(\ket{0} {1}- \ket )$</span><span class="sxs-lookup"><span data-stu-id="5f01a-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="5f01a-140">Als we de Hadamard-poort toepassen op de eerste qubit van elke termijn van onze bovenstaande output, krijgen we het volgende resultaat:</span><span class="sxs-lookup"><span data-stu-id="5f01a-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="5f01a-141">{2}$$ \frac{\alpha}{\sqrt }(\frac{1}{\sqrt{2}{0} }(\ket +{00} \ket)\ket{2}{1}{2}{0} {1}{11} {2}{1}{2}{0} {1}{10} {2}{1}+ \frac{\alpha}{\sqrt }(\frac {\sqrt }(\ket + \ket)\ket + ket + \frac{\beta}{\sqrt }(\frac {\sqrt }(\ket -{1}\ket)\ket{2}+ \frac{\beta}{\sqrt }(\frac {\sqrt }(\ket{0} - \ket)\ket{1}{01} $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="5f01a-142">Houd er rekening mee dat{1}elke term{2}twee $\frac {\sqrt }$ factoren heeft.</span><span class="sxs-lookup"><span data-stu-id="5f01a-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="5f01a-143">We kunnen vermenigvuldigen deze uit het geven van het volgende resultaat:</span><span class="sxs-lookup"><span data-stu-id="5f01a-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="5f01a-144">$${2}\frac{\alpha} (\ket{0} {1}+ \ket)\ket{00} +{2}\frac{\alpha}{0} (\ket + \ket)\ket{1}{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket){1}{01} \ket</span><span class="sxs-lookup"><span data-stu-id="5f01a-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="5f01a-145">De $\frac{1}{2}$ factor is gemeenschappelijk voor elke term, zodat we nu kunnen nemen buiten de haakjes:</span><span class="sxs-lookup"><span data-stu-id="5f01a-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="5f01a-146">$${1}{2}\frac \big[\alpha(\ket{0} {1}+ \ket)\ket{00} +{0} \alpha(\ket + \ket)\ket{1}{11} +{0} \beta(\ket -{0} \ket)\ket{01}{1}{10} + \beta(\ket - \ket)\ket{1}\big] $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="5f01a-147">We kunnen dan vermenigvuldigen uit de haakjes voor elke term geven:</span><span class="sxs-lookup"><span data-stu-id="5f01a-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="5f01a-148">$$ \frac{1}{2}\big[\alpha\ket{000} +{100} \alpha\ket{011} + \alpha\ket +{111} \alpha\ket + \beta\ket{001} {101}{010} - \beta\ket{110} + \beta\ket - \beta\ket \big] $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="5f01a-149">Stap 3: Meet het resultaat</span><span class="sxs-lookup"><span data-stu-id="5f01a-149">Step 3: Measure the result</span></span>

<span data-ttu-id="5f01a-150">Als gevolg van __hier__ en __daar__ verstrikt, elke meting op __hier__ zal invloed hebben op de toestand van __daar__.</span><span class="sxs-lookup"><span data-stu-id="5f01a-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="5f01a-151">Als we meten de eerste en tweede qubit __(bericht__ en __hier__) kunnen we leren welke staat __er__ is in, als gevolg van deze eigenschap van verstrengeling.</span><span class="sxs-lookup"><span data-stu-id="5f01a-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="5f01a-152">Als we meten en krijgen een resultaat 00, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat.</span><span class="sxs-lookup"><span data-stu-id="5f01a-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="5f01a-153">Dat is $\alpha\ket{000} +\beta\ket{001}$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="5f01a-154">Dit kan worden aangepast aan{00}$\ket (\alpha\ket{0} {1}+\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="5f01a-155">Daarom als we meten de eerste en tweede qubit te zijn __there__00, weten we dat de{0} derde qubit, er , is in de staat $(\alpha\ket +\beta\ket)$.{1}</span><span class="sxs-lookup"><span data-stu-id="5f01a-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="5f01a-156">Als we meten en krijgen een resultaat 01, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat.</span><span class="sxs-lookup"><span data-stu-id="5f01a-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="5f01a-157">Dat is $\alpha\ket{011} +\beta\ket{010}$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="5f01a-158">Dit kan worden aangepast aan{01}$\ket (\alpha\ket{1} {0}+\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="5f01a-159">Daarom als we meten de eerste en tweede qubit te zijn __there__01, weten we dat de{1} derde qubit, er , is in de staat $(\alpha\ket +\beta\ket)$.{0}</span><span class="sxs-lookup"><span data-stu-id="5f01a-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="5f01a-160">Als we meten en krijgen een resultaat 10, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat.</span><span class="sxs-lookup"><span data-stu-id="5f01a-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="5f01a-161">Dat is $\alpha\ket{100} -\beta\ket{101}$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="5f01a-162">Dit kan worden aangepast aan{10}$\ket (\alpha\ket{0} {1}-\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="5f01a-163">Daarom als we meten de eerste en tweede qubit te zijn __there__10, weten we dat de{0} derde qubit, er , is in de staat $(\alpha\ket -\beta\ket)$.{1}</span><span class="sxs-lookup"><span data-stu-id="5f01a-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="5f01a-164">Als we meten en krijgen een resultaat 11, de superpositie instort, waardoor alleen termen in overeenstemming met dit resultaat.</span><span class="sxs-lookup"><span data-stu-id="5f01a-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="5f01a-165">Dat is $\alpha\ket{111} -\beta\ket{110}$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="5f01a-166">Dit kan worden aangepast aan{11}$\ket (\alpha\ket{1} {0}-\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="5f01a-167">Daarom als we meten de eerste en tweede qubit te zijn __there__11, weten we dat de{1} derde qubit, er , is in de staat $(\alpha\ket -\beta\ket)$.{0}</span><span class="sxs-lookup"><span data-stu-id="5f01a-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="5f01a-168">Stap 4: Interpreteer het resultaat</span><span class="sxs-lookup"><span data-stu-id="5f01a-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="5f01a-169">Ter herinnering, het oorspronkelijke __bericht__ dat we wilden sturen was:</span><span class="sxs-lookup"><span data-stu-id="5f01a-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="5f01a-170">$$ \ket{\psi} = \alpha\ket{0} +{1} \beta\ket $$</span><span class="sxs-lookup"><span data-stu-id="5f01a-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="5f01a-171">We moeten de __qubit in__ deze staat krijgen, zodat de ontvangen toestand degene is die bedoeld was.</span><span class="sxs-lookup"><span data-stu-id="5f01a-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="5f01a-172">Als we gemeten en kreeg een resultaat van 00, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{0} +\beta\ket)$.{1}</span><span class="sxs-lookup"><span data-stu-id="5f01a-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="5f01a-173">Aangezien dit het beoogde __bericht__is, is er geen wijziging nodig.</span><span class="sxs-lookup"><span data-stu-id="5f01a-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="5f01a-174">Als we gemeten en kreeg een resultaat van 01, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{1} +\beta\ket)$.{0}</span><span class="sxs-lookup"><span data-stu-id="5f01a-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="5f01a-175">Dit verschilt van het beoogde __bericht,__ maar het toepassen van een NOT-poort{0} geeft ons{1}de gewenste status $(\alpha\ket +\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="5f01a-176">Als we gemeten en kreeg een resultaat van 10, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{0} -\beta\ket)$.{1}</span><span class="sxs-lookup"><span data-stu-id="5f01a-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="5f01a-177">Dit verschilt van het beoogde __bericht,__ maar het toepassen van een Z-poort{0} geeft ons{1}de gewenste staat $(\alpha\ket +\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="5f01a-178">Als we gemeten en kreeg een resultaat van 11, dan is de derde qubit, __daar__, is in de staat $(\alpha\ket{1} -\beta\ket)$.{0}</span><span class="sxs-lookup"><span data-stu-id="5f01a-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="5f01a-179">Dit verschilt van het beoogde __bericht,__ maar het toepassen van een NOT-poort gevolgd door{0} een Z-poort{1}geeft ons de gewenste staat $(\alpha\ket +\beta\ket)$.</span><span class="sxs-lookup"><span data-stu-id="5f01a-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="5f01a-180">Samenvattend, als we meten en de eerste qubit is 1, een Z-poort wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="5f01a-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="5f01a-181">Als we meten en de tweede qubit is 1, een NOT poort wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="5f01a-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="5f01a-182">Samenvatting</span><span class="sxs-lookup"><span data-stu-id="5f01a-182">Summary</span></span>
<span data-ttu-id="5f01a-183">Hieronder is een tekst-boek quantum circuit dat de teleportatie implementeert.</span><span class="sxs-lookup"><span data-stu-id="5f01a-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="5f01a-184">Als u van links naar rechts gaat, u zien:</span><span class="sxs-lookup"><span data-stu-id="5f01a-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="5f01a-185">Stap 1: Verwaren __hier__ en __daar__ door het toepassen van een Hadamard poort en CNOT poort.</span><span class="sxs-lookup"><span data-stu-id="5f01a-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="5f01a-186">Stap 2: Het verzenden van het __bericht__ met behulp van een CNOT-poort en een Hadamard-poort.</span><span class="sxs-lookup"><span data-stu-id="5f01a-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="5f01a-187">Stap 3: Het nemen van een meting van de eerste en tweede qubits, __bericht__ en __hier__.</span><span class="sxs-lookup"><span data-stu-id="5f01a-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="5f01a-188">Stap 4: Het aanbrengen van een NOT-poort of een Z-poort, afhankelijk van het resultaat van de meting in stap 3.</span><span class="sxs-lookup"><span data-stu-id="5f01a-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

!["Teleport(msg : Qubit, there : Qubit) : Unit"](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="5f01a-190">Quantum Teleportatie: Code</span><span class="sxs-lookup"><span data-stu-id="5f01a-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="5f01a-191">We hebben ons circuit voor kwantumteleportatie:</span><span class="sxs-lookup"><span data-stu-id="5f01a-191">We have our circuit for quantum teleportation:</span></span>

!["Teleport(msg : Qubit, there : Qubit) : Unit"](~/media/teleportation.svg)

<span data-ttu-id="5f01a-193">We kunnen nu elk van de stappen in dit kwantumcircuit vertalen naar Q#.</span><span class="sxs-lookup"><span data-stu-id="5f01a-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="5f01a-194">Stap 0: Definitie</span><span class="sxs-lookup"><span data-stu-id="5f01a-194">Step 0: Definition</span></span>
<span data-ttu-id="5f01a-195">Wanneer we teleportatie uitvoeren, moeten we weten welke __boodschap__ we willen sturen, en waar we het __(daar)__ willen sturen.</span><span class="sxs-lookup"><span data-stu-id="5f01a-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="5f01a-196">Om deze reden beginnen we met het definiëren van een nieuwe `msg` Teleport-bewerking die twee qubits als argumenten krijgt, en: `there`</span><span class="sxs-lookup"><span data-stu-id="5f01a-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="5f01a-197">We moeten ook een `here` qubit toewijzen `using` die we bereiken met een blok:</span><span class="sxs-lookup"><span data-stu-id="5f01a-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="5f01a-198">Stap 1: Een verstrengelde toestand maken</span><span class="sxs-lookup"><span data-stu-id="5f01a-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="5f01a-199">We kunnen dan het verstrengelde `there` paar @"microsoft.quantum.intrinsic.h" tussen @"microsoft.quantum.intrinsic.cnot" `here` en met behulp van de en operaties:</span><span class="sxs-lookup"><span data-stu-id="5f01a-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="5f01a-200">Stap 2: Het bericht verzenden</span><span class="sxs-lookup"><span data-stu-id="5f01a-200">Step 2: Send the message</span></span>
<span data-ttu-id="5f01a-201">Vervolgens gebruiken we de volgende $\operatorname{CNOT}$ en $H$ poorten om ons bericht qubit te verplaatsen:</span><span class="sxs-lookup"><span data-stu-id="5f01a-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="5f01a-202">Stap 3 & 4: Het meten en interpreteren van het resultaat</span><span class="sxs-lookup"><span data-stu-id="5f01a-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="5f01a-203">Tot slot @"microsoft.quantum.intrinsic.m" gebruiken we om de metingen uit te voeren en de `if` nodige poortbewerkingen uit te voeren om de gewenste status te krijgen, zoals aangegeven door verklaringen:</span><span class="sxs-lookup"><span data-stu-id="5f01a-203">Finally, we use @"microsoft.quantum.intrinsic.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a><span data-ttu-id="5f01a-204">Stap 5: Het qubit-register opnieuw opstarten</span><span class="sxs-lookup"><span data-stu-id="5f01a-204">Step 5: Restarting the qubit register</span></span>

<span data-ttu-id="5f01a-205">Aan het einde van elke Q # operatie moeten we de{0}qubits laten in de staat $\ket $.</span><span class="sxs-lookup"><span data-stu-id="5f01a-205">At the end of every Q# operation we need to let the qubits in the state $\ket{0}$.</span></span> <span data-ttu-id="5f01a-206">We kunnen @"microsoft.quantum.intrinsic.reset" gebruiken om alle qubits opnieuw te starten naar de nulstaat en dit zal onze operatie voltooien.</span><span class="sxs-lookup"><span data-stu-id="5f01a-206">We can use @"microsoft.quantum.intrinsic.reset" to restart all the qubits to the zero state and this will finish our operation.</span></span>

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


