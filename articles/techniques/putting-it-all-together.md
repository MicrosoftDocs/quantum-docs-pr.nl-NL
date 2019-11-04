---
title: 'Q # technieken: alles op elkaar plaatsen | Microsoft Docs'
description: 'Q # technieken: alles samen zetten'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: f65b3e260f98a7a90da13b62edd6cc63d200f5af
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183264"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="1b024-103">Alles combi neren: teleportie</span><span class="sxs-lookup"><span data-stu-id="1b024-103">Putting it All Together: Teleportation</span></span> #
<span data-ttu-id="1b024-104">We gaan terug naar het voor beeld van het telepoorts circuit dat is gedefinieerd in [Quantum circuits](xref:microsoft.quantum.concepts.circuits).</span><span class="sxs-lookup"><span data-stu-id="1b024-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="1b024-105">We gaan deze gebruiken om de concepten te illustreren die we tot nu toe hebben geleerd.</span><span class="sxs-lookup"><span data-stu-id="1b024-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="1b024-106">Hieronder vindt u een uitleg van Quantum teleportie voor degenen die niet bekend zijn met de theorie, gevolgd door een overzicht van de code-implementatie in Q #.</span><span class="sxs-lookup"><span data-stu-id="1b024-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="1b024-107">Quantum-teleportie: theorie</span><span class="sxs-lookup"><span data-stu-id="1b024-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="1b024-108">Quantum teleportal is een techniek voor het verzenden van een onbekende Quantum status (waarnaar we verwijzen als '__bericht__') van een Qubit op een locatie naar een Qubit op een andere locatie (deze worden naar deze qubits verwezen als '__hier__' en '__daar__', respectievelijk).</span><span class="sxs-lookup"><span data-stu-id="1b024-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="1b024-109">We kunnen ons __bericht__ als een vector weer geven met behulp van de Dirac-notatie:</span><span class="sxs-lookup"><span data-stu-id="1b024-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="1b024-110">$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="1b024-111">De status van het __bericht__ Qubit is niet bekend bij ons, omdat we niet weten wat de waarden van $ \alpha $ en $ \beta $ zijn.</span><span class="sxs-lookup"><span data-stu-id="1b024-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="1b024-112">Stap 1: een Entangled-status maken</span><span class="sxs-lookup"><span data-stu-id="1b024-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="1b024-113">Als u het __bericht__ wilt verzenden, moet u __hier__ de Qubit Entangled met __de Qubit.__</span><span class="sxs-lookup"><span data-stu-id="1b024-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="1b024-114">Dit wordt bereikt door een Hadamard-poort toe te passen, gevolgd door een CNOT-poort.</span><span class="sxs-lookup"><span data-stu-id="1b024-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="1b024-115">Laten we eens kijken naar de wiskundige formules achter deze poort bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="1b024-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="1b024-116">We beginnen __hier__ met de __qubits en in__ de $ \ket{0}$-status.</span><span class="sxs-lookup"><span data-stu-id="1b024-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="1b024-117">Na het entangling van deze qubits hebben ze de volgende status:</span><span class="sxs-lookup"><span data-stu-id="1b024-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="1b024-118">$ $ \ket{\phi ^ +} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="1b024-119">Stap 2: het bericht verzenden</span><span class="sxs-lookup"><span data-stu-id="1b024-119">Step 2: Send the message</span></span>
<span data-ttu-id="1b024-120">Als u het __bericht__ wilt verzenden, past u eerst een CNOT-Gate toe met het __bericht__ Qubit en __hier__ Qubit als invoer (het __bericht__ Qubit het besturings element en de Qubit als __doel Qubit,__ in dit geval).</span><span class="sxs-lookup"><span data-stu-id="1b024-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="1b024-121">Deze invoer status kan worden geschreven:</span><span class="sxs-lookup"><span data-stu-id="1b024-121">This input state can be written:</span></span>

<span data-ttu-id="1b024-122">$ $ \ket{\psi}\ket{\phi ^ +} = (\alpha\ket{0} + \beta\ket{1}) (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11})) $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="1b024-123">Dit kan worden uitgebreid naar:</span><span class="sxs-lookup"><span data-stu-id="1b024-123">This expands to:</span></span>

<span data-ttu-id="1b024-124">$ $ \ket{\psi}\ket{\phi ^ +} = \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="1b024-125">Als herinnering wordt de CNOT-Gate gespiegeld met de doel-Qubit wanneer het besturings element Qubit 1 is.</span><span class="sxs-lookup"><span data-stu-id="1b024-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="1b024-126">Een invoer van $ \ket{000}$ resulteert bijvoorbeeld in geen wijziging als de eerste Qubit (het besturings element) 0 is.</span><span class="sxs-lookup"><span data-stu-id="1b024-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="1b024-127">Doe echter een geval waarbij de eerste Qubit 1 is, bijvoorbeeld een invoer van $ \ket{100}$.</span><span class="sxs-lookup"><span data-stu-id="1b024-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="1b024-128">In dit geval is de uitvoer $ \ket{110}$, omdat de tweede Qubit (het doel) wordt gespiegeld door de CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="1b024-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="1b024-129">We beschouwen nu onze uitvoer zodra de CNOT-Gate op de bovenstaande invoer heeft gehandeld.</span><span class="sxs-lookup"><span data-stu-id="1b024-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="1b024-130">Het resultaat is:</span><span class="sxs-lookup"><span data-stu-id="1b024-130">The result is:</span></span>

<span data-ttu-id="1b024-131">$ $ \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{110} + \frac{\beta}{\sqrt{2}} \ket{101} $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="1b024-132">De volgende stap voor het verzenden van het __bericht__ is het Toep assen van een Hadamard-poort op het __bericht__ Qubit (dat is de eerste Qubit van elke term).</span><span class="sxs-lookup"><span data-stu-id="1b024-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="1b024-133">Als herinnering geeft de Hadamard-Gate het volgende:</span><span class="sxs-lookup"><span data-stu-id="1b024-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="1b024-134">Invoer</span><span class="sxs-lookup"><span data-stu-id="1b024-134">Input</span></span> | <span data-ttu-id="1b024-135">Uitvoer</span><span class="sxs-lookup"><span data-stu-id="1b024-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="1b024-136">$ \ket{0}$</span><span class="sxs-lookup"><span data-stu-id="1b024-136">$\ket{0}$</span></span>  | <span data-ttu-id="1b024-137">$ \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) $</span><span class="sxs-lookup"><span data-stu-id="1b024-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="1b024-138">$ \ket{1}$</span><span class="sxs-lookup"><span data-stu-id="1b024-138">$\ket{1}$</span></span>  | <span data-ttu-id="1b024-139">$ \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}) $</span><span class="sxs-lookup"><span data-stu-id="1b024-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="1b024-140">Als we de Hadamard-poort Toep assen op de eerste Qubit van elke periode van onze uitvoer hierboven, krijgen we het volgende resultaat:</span><span class="sxs-lookup"><span data-stu-id="1b024-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="1b024-141">$ $ \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{00} + \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{11} + \frac{\beta}{ \sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="1b024-142">Houd er rekening mee dat elke term $2 \frac{1}{\sqrt{2}} $-factoren heeft.</span><span class="sxs-lookup"><span data-stu-id="1b024-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="1b024-143">We kunnen deze uitvermenigvuldigen met het volgende resultaat:</span><span class="sxs-lookup"><span data-stu-id="1b024-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="1b024-144">$ $ \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{11} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{10} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="1b024-145">De $ \frac{1}{2}$-factor is gebruikelijk voor elke term zodat we deze nu buiten de vier Kante haken kunnen halen:</span><span class="sxs-lookup"><span data-stu-id="1b024-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="1b024-146">$ $ \frac{1}{2}\big [\alpha (\ket{0} + \ket{1}) \ket{00} + \alpha (\ket{0} + \ket{1}) \ket{11} + \beta (\ket{0}-\ket{1}) \ket{10} + \beta (\ket{0}-\ket{1}) \ket{01}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="1b024-147">De vier Kante haken kunnen vervolgens worden vermenigvuldigd voor elke term met het volgende:</span><span class="sxs-lookup"><span data-stu-id="1b024-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="1b024-148">$ $ \frac{1}{2}\big [\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010}-\beta\ket{110} + \beta\ket{001}-\beta\ket{101}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="1b024-149">Stap 3: het resultaat meten</span><span class="sxs-lookup"><span data-stu-id="1b024-149">Step 3: Measure the result</span></span>

<span data-ttu-id="1b024-150">Als gevolg van __hier__ en __er__ wordt Entangled, dan is de meting __hier__ van invloed op de __status.__</span><span class="sxs-lookup"><span data-stu-id="1b024-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="1b024-151">Als we de eerste en tweede Qubit (__bericht__ en __hier__) meten, kunnen we weten wat staat __er__ in, vanwege deze eigenschap van Entanglement.</span><span class="sxs-lookup"><span data-stu-id="1b024-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="1b024-152">Als we het resultaat 00 meten en ontvangen, wordt de superpositie samengevouwen, waardoor alleen de termen consistent zijn met dit resultaat.</span><span class="sxs-lookup"><span data-stu-id="1b024-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="1b024-153">Dat is $ \alpha\ket{000} + \beta\ket{001}$.</span><span class="sxs-lookup"><span data-stu-id="1b024-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="1b024-154">Dit kan worden herstructureeerd tot $ \ket{00}(\alpha\ket{0} + \beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="1b024-155">Als we de eerste en tweede Qubit meten als 00, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{0} + \beta\ket{1}) $ bevindt.</span><span class="sxs-lookup"><span data-stu-id="1b024-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="1b024-156">Als we het resultaat 01 meten en ophalen, wordt de superpositie samengevouwen, waardoor alleen de termen met dit resultaat overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="1b024-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="1b024-157">Dat is $ \alpha\ket{011} + \beta\ket{010}$.</span><span class="sxs-lookup"><span data-stu-id="1b024-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="1b024-158">Dit kan worden herstructureeerd tot $ \ket{01}(\alpha\ket{1} + \beta\ket{0}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="1b024-159">Als we de eerste en tweede Qubit meten als 01, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{1} + \beta\ket{0}) $ bevindt.</span><span class="sxs-lookup"><span data-stu-id="1b024-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="1b024-160">Als we het resultaat 10 meten en ophalen, wordt de superpositie samengevouwen, waardoor alleen de termen consistent zijn met dit resultaat.</span><span class="sxs-lookup"><span data-stu-id="1b024-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="1b024-161">Dat is $ \alpha\ket{100}-\beta\ket{101}$.</span><span class="sxs-lookup"><span data-stu-id="1b024-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="1b024-162">Dit kan worden herstructureeerd naar $ \ket{10}(\alpha\ket{0}-\beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="1b024-163">Als we de eerste en tweede Qubit naar 10 meten, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{0}-\beta\ket{1}) $ bevindt.</span><span class="sxs-lookup"><span data-stu-id="1b024-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="1b024-164">Als we het resultaat 11 meten en ophalen, wordt de superpositie samengevouwen, waardoor alleen de termen met dit resultaat overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="1b024-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="1b024-165">Dat is $ \alpha\ket{111}-\beta\ket{110}$.</span><span class="sxs-lookup"><span data-stu-id="1b024-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="1b024-166">Dit kan worden herstructureeerd naar $ \ket{11}(\alpha\ket{1}-\beta\ket{0}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="1b024-167">Als we de eerste en tweede Qubit meten in 11, weten we dat de derde Qubit, __daar__, zich in de status $ (\alpha\ket{1}-\beta\ket{0}) $ bevindt.</span><span class="sxs-lookup"><span data-stu-id="1b024-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="1b024-168">Stap 4: het resultaat interpreteren</span><span class="sxs-lookup"><span data-stu-id="1b024-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="1b024-169">Het oorspronkelijke __bericht__ dat we willen verzenden, is als herinnering:</span><span class="sxs-lookup"><span data-stu-id="1b024-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="1b024-170">$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $</span><span class="sxs-lookup"><span data-stu-id="1b024-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="1b024-171">We moeten de __er__ Qubit in deze staat ophalen, zodat de ontvangen status het certificaat is dat is bedoeld.</span><span class="sxs-lookup"><span data-stu-id="1b024-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="1b024-172">Als we hebben gemeten en een resultaat van 00 hebben ontvangen, bevindt de derde Qubit __er__in de status $ (\alpha\ket{0} + \beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="1b024-173">Aangezien dit het bedoelde __bericht__is, is er geen wijziging vereist.</span><span class="sxs-lookup"><span data-stu-id="1b024-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="1b024-174">Als we het resultaat van 01 hebben gemeten en ontvangen, bevindt de derde Qubit, __daar__, zich in de status $ (\alpha\ket{1} + \beta\ket{0}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="1b024-175">Dit verschilt van het beoogde __bericht__, maar het Toep assen van een not-Gate geeft ons de gewenste status $ (\alpha\ket{0} + \beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="1b024-176">Als we een resultaat van 10 hebben gemeten en ontvangen, bevindt de derde Qubit, __daar__, zich in de status $ (\alpha\ket{0}-\beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="1b024-177">Dit verschilt van het beoogde __bericht__, maar het Toep assen van een Z-Gate geeft ons de gewenste status $ (\alpha\ket{0} + \beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="1b024-178">Als we hebben gemeten en een resultaat van 11 hebben ontvangen, bevindt de derde Qubit __er__in de status $ (\alpha\ket{1}-\beta\ket{0}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="1b024-179">Dit verschilt van het beoogde __bericht__, maar het Toep assen van een niet-poort, gevolgd door een Z-Gate, geeft ons de gewenste status $ (\alpha\ket{0} + \beta\ket{1}) $.</span><span class="sxs-lookup"><span data-stu-id="1b024-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="1b024-180">Als we meten en de eerste Qubit is 1, wordt een Z-poort toegepast.</span><span class="sxs-lookup"><span data-stu-id="1b024-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="1b024-181">Als we meten en de tweede Qubit is 1, wordt er geen Gate toegepast.</span><span class="sxs-lookup"><span data-stu-id="1b024-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="1b024-182">Samenvatting</span><span class="sxs-lookup"><span data-stu-id="1b024-182">Summary</span></span>
<span data-ttu-id="1b024-183">Hieronder ziet u een Quantum-circuit (Text-Book) waarmee de teleportie wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="1b024-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="1b024-184">Van links naar rechts kunt u het volgende zien:</span><span class="sxs-lookup"><span data-stu-id="1b024-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="1b024-185">Stap 1: Entangling __hier__ en __er__ door een HADAMARD-Gate en CNOT-poort toe te passen.</span><span class="sxs-lookup"><span data-stu-id="1b024-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="1b024-186">Stap 2: het __bericht__ verzenden met behulp van een CNOT-Gate en een Hadamard-poort.</span><span class="sxs-lookup"><span data-stu-id="1b024-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="1b024-187">Stap 3: het maken van een meting van het eerste en tweede qubits, __bericht__ en __hier__.</span><span class="sxs-lookup"><span data-stu-id="1b024-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="1b024-188">Stap 4: een NOT-Gate of een Z-poort Toep assen, afhankelijk van het resultaat van de meting in stap 3.</span><span class="sxs-lookup"><span data-stu-id="1b024-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

![' Teleporten (msg: Qubit, daar: Qubit): eenheid '](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="1b024-190">Quantum-teleportie: code</span><span class="sxs-lookup"><span data-stu-id="1b024-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="1b024-191">We hebben ons circuit voor Quantum-teleportie:</span><span class="sxs-lookup"><span data-stu-id="1b024-191">We have our circuit for quantum teleportation:</span></span>

![' Teleporten (msg: Qubit, daar: Qubit): eenheid '](~/media/teleportation.svg)

<span data-ttu-id="1b024-193">We kunnen de stappen in dit Quantum circuit nu omzetten in Q #.</span><span class="sxs-lookup"><span data-stu-id="1b024-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="1b024-194">Stap 0: definitie</span><span class="sxs-lookup"><span data-stu-id="1b024-194">Step 0: Definition</span></span>
<span data-ttu-id="1b024-195">Wanneer we teleportie uitvoeren, moeten we het __bericht__ weten dat we willen verzenden en waar we het willen verzenden.</span><span class="sxs-lookup"><span data-stu-id="1b024-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="1b024-196">Daarom beginnen we met het definiëren van een nieuwe teleport-bewerking die twee qubits als argumenten, `msg` en `there`heeft.</span><span class="sxs-lookup"><span data-stu-id="1b024-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="1b024-197">We moeten ook een Qubit toewijzen `here` die wordt gerealiseerd met een `using` blok:</span><span class="sxs-lookup"><span data-stu-id="1b024-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="1b024-198">Stap 1: een Entangled-status maken</span><span class="sxs-lookup"><span data-stu-id="1b024-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="1b024-199">Vervolgens kunnen we het Entangled-paar maken tussen `here` en `there` met behulp van de @"microsoft.quantum.primitive.h"-en @"microsoft.quantum.primitive.cnot"-bewerkingen:</span><span class="sxs-lookup"><span data-stu-id="1b024-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.primitive.h" and @"microsoft.quantum.primitive.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="1b024-200">Stap 2: het bericht verzenden</span><span class="sxs-lookup"><span data-stu-id="1b024-200">Step 2: Send the message</span></span>
<span data-ttu-id="1b024-201">Vervolgens gebruiken we de volgende $ \operatorname{CNOT} $ en $H $ Gates om onze bericht Qubit te verplaatsen:</span><span class="sxs-lookup"><span data-stu-id="1b024-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="1b024-202">Stap 3 & 4: het resultaat meten en interpreteren</span><span class="sxs-lookup"><span data-stu-id="1b024-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="1b024-203">Ten slotte gebruiken we @"microsoft.quantum.primitive.m" om de metingen uit te voeren en de benodigde poort bewerkingen uit te voeren om de gewenste status te krijgen, zoals aangegeven door `if`-instructies:</span><span class="sxs-lookup"><span data-stu-id="1b024-203">Finally, we use @"microsoft.quantum.primitive.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

<span data-ttu-id="1b024-204">Hiermee voltooit u de definitie van onze teleportie-operator, waardoor we de toewijzing van `here`ongedaan kunnen maken, de hoofd tekst te beëindigen en de bewerking te beëindigen.</span><span class="sxs-lookup"><span data-stu-id="1b024-204">This finishes the definition of our teleportation operator, so we can deallocate `here`, end the body, and end the operation.</span></span>

```qsharp
    }
}
```
