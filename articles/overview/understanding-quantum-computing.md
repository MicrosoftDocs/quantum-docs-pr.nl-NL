---
title: Kwantumcomputing begrijpen
description: Wat zijn kwantumcomputers en hoe maken ze gebruik van de principes van kwantummechanica?
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.understanding
ms.openlocfilehash: aa3de9290250e82bc2f3ea5f1d35a16095469f7e
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327727"
---
# <a name="understanding-quantum-computing"></a><span data-ttu-id="d73ae-103">Kwantumcomputing begrijpen</span><span class="sxs-lookup"><span data-stu-id="d73ae-103">Understanding quantum computing</span></span>

<span data-ttu-id="d73ae-104">Bij kwantumcomputing worden de principes van kwantummechanica gebruikt voor het verwerken van informatie.</span><span class="sxs-lookup"><span data-stu-id="d73ae-104">Quantum computing uses the principles of quantum mechanics to process information.</span></span> <span data-ttu-id="d73ae-105">Daarom vereist kwantumcomputing een andere benadering dan klassieke computing.</span><span class="sxs-lookup"><span data-stu-id="d73ae-105">Because of this, quantum computing requires a different approach than classical computing.</span></span>  <span data-ttu-id="d73ae-106">Een verschil, bijvoorbeeld, is de processor die in kwantumcomputers wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d73ae-106">One example of this difference is the processor used in quantum computers.</span></span>  <span data-ttu-id="d73ae-107">In klassieke computers worden welbekende siliciumchips gebruikt, terwijl in kwantumcomputers kwantummaterialen zoals atomen, ionen, fotonen of elektronen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d73ae-107">Where classical computers use familiar silicon-based chips, quantum computers use quantum materials such as atoms, ions, photons, or electrons.</span></span>  

<span data-ttu-id="d73ae-108">Het kwantummateriaal gedraagt zich in overeenstemming met de wetten van kwantummechanica, met behulp van concepten zoals probabilistische computing, superpositie en verstrengeling.</span><span class="sxs-lookup"><span data-stu-id="d73ae-108">The quantum material behaves according to the laws of quantum mechanics, leveraging concepts such as probabilistic computation, superposition, and entanglement.</span></span> <span data-ttu-id="d73ae-109">Deze concepten vormen de basis voor kwantumalgoritmen, die de kracht van kwantumcomputing benutten voor het oplossen van complexe problemen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-109">These concepts provide the basis for quantum algorithms that harness the power of quantum computing to solve complex problems.</span></span> <span data-ttu-id="d73ae-110">In dit artikel worden enkele essentiële concepten van kwantummechanica beschreven waarop kwantumcomputing is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="d73ae-110">This article describes some of the essential concepts of quantum mechanics on which quantum computing is based.</span></span>

## <a name="a-birds-eye-view-of-quantum-mechanics"></a><span data-ttu-id="d73ae-111">Overzicht van kwantummechanica</span><span class="sxs-lookup"><span data-stu-id="d73ae-111">A bird’s-eye view of quantum mechanics</span></span>

<span data-ttu-id="d73ae-112">Kwantummechanica, ook wel kwantumtheorie genoemd, is een tak van de natuurkunde die zich bezig houdt met deeltjes op atomair en subatomair niveau.</span><span class="sxs-lookup"><span data-stu-id="d73ae-112">Quantum mechanics, also called quantum theory, is a branch of physics that deals with particles at the atomic and subatomic levels.</span></span> <span data-ttu-id="d73ae-113">Op kwantumniveau zijn echter veel natuurkundige wetten die u voor vanzelfsprekend aanneemt, niet van toepassing.</span><span class="sxs-lookup"><span data-stu-id="d73ae-113">At the quantum level, however, many of the laws of mechanics you take for granted don’t apply.</span></span> <span data-ttu-id="d73ae-114">Superpositie, kwantummeting en verstrengeling zijn drie verschijnselen die centraal staan in kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="d73ae-114">Superposition, quantum measurement, and entanglement are three phenomena that are central to quantum computing.</span></span>  

### <a name="superposition-vs-binary-computing"></a><span data-ttu-id="d73ae-115">Superpositie versus binaire computing</span><span class="sxs-lookup"><span data-stu-id="d73ae-115">Superposition vs. binary computing</span></span>

<span data-ttu-id="d73ae-116">Stel, u doet lichamelijke oefeningen in uw woonkamer.</span><span class="sxs-lookup"><span data-stu-id="d73ae-116">Imagine that you are exercising in your living room.</span></span> <span data-ttu-id="d73ae-117">U draait helemaal naar links en vervolgens helemaal naar rechts.</span><span class="sxs-lookup"><span data-stu-id="d73ae-117">You turn all the way to your left and then all the way to your right.</span></span> <span data-ttu-id="d73ae-118">Draai nu tegelijkertijd naar links en rechts.</span><span class="sxs-lookup"><span data-stu-id="d73ae-118">Now turn to your left and your right at the same time.</span></span> <span data-ttu-id="d73ae-119">Dat kunt u niet (tenzij u zichzelf in tweeën kunt splitsen).</span><span class="sxs-lookup"><span data-stu-id="d73ae-119">You can’t do it (not without splitting yourself in two, at least).</span></span>  <span data-ttu-id="d73ae-120">Natuurlijk kunt u zich niet in twee standen tegelijk bevinden: u kunt niet op hetzelfde moment zowel naar links als naar rechts kijken.</span><span class="sxs-lookup"><span data-stu-id="d73ae-120">Obviously, you can’t be in both of those states at once – you can’t be facing left and facing right at the same time.</span></span>

<span data-ttu-id="d73ae-121">Als u echter een kwantumdeeltje bent, is er een bepaalde kans dat u *naar links* kijkt én een bepaalde kans dat u *naar rechts* kijkt als gevolg van het verschijnsel **superpositie** (ook wel bekend als **coherentie**).</span><span class="sxs-lookup"><span data-stu-id="d73ae-121">However, if you are a quantum particle, then you can have a certain probability of *facing left* AND a certain probability of *facing right* due to a phenomenon known as **superposition** (also known as **coherence**).</span></span>

<span data-ttu-id="d73ae-122">Een kwantumdeeltje, zoals een elektron, heeft zijn eigen eigenschappen voor de naar links of rechts kijkende toestand, zoals een **draaiing**, omhoog of omlaag. Om dit meer te relateren aan klassieke binaire computing, kunnen we die ook 1 of 0 noemen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-122">A quantum particle such as an electron has its own “facing left or facing right” properties, for example **spin**, referred to as either up or down, or to make it more relatable to classical binary computing, let’s just say 1 or 0.</span></span> <span data-ttu-id="d73ae-123">Wanneer een kwantumdeeltje zich in een toestand van superpositie bevindt, is het een lineaire combinatie van een oneindig aantal toestanden tussen 1 en 0, maar u weet niet welke toestand totdat u deze daadwerkelijk bekijkt. Daarmee komen we toe aan het volgende verschijnsel: **kwantummeting**.</span><span class="sxs-lookup"><span data-stu-id="d73ae-123">When a quantum particle is in a superposition state, it’s a linear combination of an infinite number of states between 1 and 0, but you don’t know which one it will be until you actually look at it, which brings up our next phenomenon, **quantum measurement**.</span></span>

### <a name="quantum-measurement"></a><span data-ttu-id="d73ae-124">Kwantummeting</span><span class="sxs-lookup"><span data-stu-id="d73ae-124">Quantum measurement</span></span>

<span data-ttu-id="d73ae-125">Stel nu dat een vriend(in) langskomt en een foto van u wil nemen terwijl u uw oefeningen doet.</span><span class="sxs-lookup"><span data-stu-id="d73ae-125">Now, let’s say your friend comes over and wants to take a picture of you exercising.</span></span> <span data-ttu-id="d73ae-126">Waarschijnlijk krijgt u een wazige afbeelding van uw positie terwijl u zich beweegt van helemaal links naar helemaal rechts of omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="d73ae-126">Most likely, they’ll get a blurry image of you turning somewhere between all the way left and all the way right.</span></span>

<span data-ttu-id="d73ae-127">Maar als u een kwantumdeeltje bent, gebeurt er iets interessants.</span><span class="sxs-lookup"><span data-stu-id="d73ae-127">But if you’re a quantum particle, an interesting thing happens.</span></span> <span data-ttu-id="d73ae-128">Ongeacht in welke positie uw foto wordt genomen, uw toestand wordt altijd weergegeven als helemaal links of helemaal rechts, nooit als iets er tussenin.</span><span class="sxs-lookup"><span data-stu-id="d73ae-128">No matter where you are when they take the picture, it will always show you either all the way left or all the way right – nothing in-between.</span></span>

<span data-ttu-id="d73ae-129">Dit komt omdat de toestand van superpositie bij observatie of meting van een kwantumdeeltje **ineenstort** (dit wordt ook wel **decoherentie** genoemd) en het deeltje een klassieke binaire toestand van 1 of 0 heeft.</span><span class="sxs-lookup"><span data-stu-id="d73ae-129">This is because the act of observing or measuring a quantum particle **collapses** the superposition state (also known as **decoherence**) and the particle takes on a classical binary state of either 1 or 0.</span></span>

<span data-ttu-id="d73ae-130">Deze binaire toestand is nuttig voor ons, omdat we in computing van alles kunnen doen met enen en nullen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-130">This binary state is helpful to us, because in computing you can do lots of things with 1’s and 0’s.</span></span> <span data-ttu-id="d73ae-131">Zodra een kwantumdeeltje is gemeten en ineengestort, blijft deze permanent in die toestand (net als uw foto) en is deze altijd 1 of 0.</span><span class="sxs-lookup"><span data-stu-id="d73ae-131">However, once a quantum particle has been measured and collapsed, it stays in that state forever (just like your picture) and will always be a 1 or 0.</span></span> <span data-ttu-id="d73ae-132">Zoals u later zult zien, zijn er in kwantumcomputing bewerkingen waarmee een deeltje opnieuw kan worden ingesteld op de toestand van superpositie, zodat het opnieuw kan worden gebruikt voor kwantumberekeningen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-132">As you’ll see later, though, in quantum computing there are operations that can “reset” a particle back to a superposition state so it can be used for quantum calculations again.</span></span>

### <a name="entanglement"></a><span data-ttu-id="d73ae-133">Verstrengeling</span><span class="sxs-lookup"><span data-stu-id="d73ae-133">Entanglement</span></span>

<span data-ttu-id="d73ae-134">Wellicht het interessantste verschijnsel van kwantummechanica is de mogelijkheid van twee of meer kwantumdeeltjes om met elkaar **verstrengeld** te raken.</span><span class="sxs-lookup"><span data-stu-id="d73ae-134">Possibly the most interesting phenomenon of quantum mechanics is the ability of two or more quantum particles to become **entangled** with each other.</span></span> <span data-ttu-id="d73ae-135">Wanneer deeltjes verstrengeld raken, vormen ze één systeem waarvan de kwantumtoestand van elk afzonderlijk deeltje niet onafhankelijk kan worden beschreven van de kwantumtoestand van de andere deeltjes.</span><span class="sxs-lookup"><span data-stu-id="d73ae-135">When particles become entangled, they form a single system such that the quantum state of any one particle cannot be described independently of the quantum state of the other particles.</span></span> <span data-ttu-id="d73ae-136">Als u dus een bewerking of proces toepast op een deeltje, is die bewerking of dat proces ook gecorreleerd aan de andere deeltjes.</span><span class="sxs-lookup"><span data-stu-id="d73ae-136">This means that whatever operation or process you apply to one particle correlates to the other particles as well.</span></span>

<span data-ttu-id="d73ae-137">Naast deze onderlinge afhankelijkheid kan deze verbinding tussen deeltjes behouden blijven, zelfs wanneer de deeltjes van elkaar zijn gescheiden door een ongelooflijk grote afstand, zelfs lichtjaren.</span><span class="sxs-lookup"><span data-stu-id="d73ae-137">In addition to this interdependency, particles can maintain this connection even when separated over incredibly large distances, even light-years.</span></span> <span data-ttu-id="d73ae-138">De effecten van kwantummeting zijn ook van toepassing op verstrengelde deeltjes. Als een deeltje wordt gemeten en ineenstort, stort ook het andere deeltje in.</span><span class="sxs-lookup"><span data-stu-id="d73ae-138">The effects of quantum measurement also apply to entangled particles, such that when one particle is measured and collapses, the other particle collapses as well.</span></span> <span data-ttu-id="d73ae-139">Omdat er sprake is van een correlatie tussen de verstrengelde qubits, biedt het meten van de toestand van een qubit informatie over de toestand van de andere qubit: deze eigenschap is zeer nuttig bij kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="d73ae-139">Because there is a correlation between the entangled qubits, measuring the state of one qubit provides information about the state of the other qubit – this particular property is very helpful in quantum computing.</span></span>

### <a name="qubits-and-probability"></a><span data-ttu-id="d73ae-140">Qubits en waarschijnlijkheid</span><span class="sxs-lookup"><span data-stu-id="d73ae-140">Qubits and probability</span></span>

<span data-ttu-id="d73ae-141">Op klassieke computers wordt informatie verwerkt en opgeslagen in bits, die een toestand van 1 of 0 kunnen hebben, maar nooit beide.</span><span class="sxs-lookup"><span data-stu-id="d73ae-141">Classical computers store and process information in bits, which can have a state of either 1 or 0, but never both.</span></span> <span data-ttu-id="d73ae-142">Het equivalent van een bit in kwantumcomputing is de **qubit**. Qubits geven de toestand van een kwantumdeeltje aan.</span><span class="sxs-lookup"><span data-stu-id="d73ae-142">The equivalent in quantum computing is the **qubit**, which represents the state of a quantum particle.</span></span> <span data-ttu-id="d73ae-143">Vanwege superpositie kan de toestand van qubits 1 of 0 zijn, of iets er tussenin.</span><span class="sxs-lookup"><span data-stu-id="d73ae-143">Because of superposition, qubits can either be 1 or 0 or anything in between.</span></span> <span data-ttu-id="d73ae-144">Afhankelijk van de configuratie van een qubit, heeft deze een bepaalde *kans* ineen te storten tot 1 of 0.</span><span class="sxs-lookup"><span data-stu-id="d73ae-144">Depending on its configuration, a qubit has a certain *probability* of collapsing to 1 or 0.</span></span> <span data-ttu-id="d73ae-145">De kans dat de qubit ineenstort tot een 1 of 0 wordt bepaald door **kwantuminterferentie**.</span><span class="sxs-lookup"><span data-stu-id="d73ae-145">The qubit's probability of collapsing one way or the other is determined by **quantum interference**.</span></span> 

<span data-ttu-id="d73ae-146">Weet u nog van die vriend(in) die een foto van u nam?</span><span class="sxs-lookup"><span data-stu-id="d73ae-146">Remember your friend that was taking your picture?</span></span> <span data-ttu-id="d73ae-147">Stel dat er een speciaal filter op de camera zat, en wel een *interferentiefilter*.</span><span class="sxs-lookup"><span data-stu-id="d73ae-147">Suppose they have special filters on their camera called *Interference* filters.</span></span> <span data-ttu-id="d73ae-148">Als we het filter *70/30* selecteren en vervolgens foto's nemen, kijkt u in 70% van de foto's naar links en in 30% van de foto's naar rechts.</span><span class="sxs-lookup"><span data-stu-id="d73ae-148">If they select the *70/30* filter and start taking pictures, in 70% of them you will be facing left, and in 30% you will be facing right.</span></span> <span data-ttu-id="d73ae-149">Het filter heeft de normale toestand van de camera beïnvloed om de kans op het gedrag ervan te beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="d73ae-149">The filter has interfered with the regular state of the camera to influence the probability of its behavior.</span></span>

<span data-ttu-id="d73ae-150">Op soortgelijke wijze beïnvloedt kwantuminterferentie de toestand van een qubit om de kans op een bepaalde uitkomst van een meting te beïnvloeden, en deze probabilistische toestand is waarin de kracht van kwantumcomputing uitblinkt.</span><span class="sxs-lookup"><span data-stu-id="d73ae-150">Similarly, quantum interference affects the state of a qubit in order to influence the probability of a certain outcome during measurement, and this probabilistic state is where the power of quantum computing excels.</span></span>

<span data-ttu-id="d73ae-151">Zo kunt u bijvoorbeeld met twee bits op een klassieke computer, waarbij elke bit 1 of 0 bevat, vier mogelijke waarden opslaan: **00**, **01**, **10** en **11**, maar slechts één tegelijk.</span><span class="sxs-lookup"><span data-stu-id="d73ae-151">For example, with two bits in a classical computer, each bit can store 1 or 0, so together you can store four possible values – **00**, **01**, **10**, and **11** – but only one of those at a time.</span></span> <span data-ttu-id="d73ae-152">Met twee qubits in superpositie kan elke qubit 1 of 0 of *beide* zijn. Daarmee kunnen dus dezelfde vier waarden tegelijkertijd worden uitgedrukt.</span><span class="sxs-lookup"><span data-stu-id="d73ae-152">With two qubits in superposition, however, each qubit can be 1 or 0 or *both*, so you can represent the same four values simultaneously.</span></span> <span data-ttu-id="d73ae-153">Met drie qubits kunnen acht waarden worden uitgedrukt, met vier qubits kunnen zestien waarden worden uitgedrukt, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="d73ae-153">With three qubits, you can represent eight values, with four qubits, you can represent 16 values, and so on.</span></span>

## <a name="summary"></a><span data-ttu-id="d73ae-154">Samenvatting</span><span class="sxs-lookup"><span data-stu-id="d73ae-154">Summary</span></span>

<span data-ttu-id="d73ae-155">Deze concepten vormen slechts het topje van de ijsberg van de krachtige mogelijkheden van kwantummechanica, maar zijn belangrijke grondbeginselen die u moet kennen voor kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="d73ae-155">These concepts just scratch the surface of quantum mechanics, but are fundamentally important concepts to know for quantum computing.</span></span>

- <span data-ttu-id="d73ae-156">**Superpositie**: de mogelijkheid van kwantumdeeltjes om een combinatie van alle mogelijke toestanden te vormen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-156">**Superposition** - The ability of quantum particles to be a combination of all possible states.</span></span>
- <span data-ttu-id="d73ae-157">**Kwantummeting**: de handeling van het observeren van een kwantumdeeltje in superpositie, hetgeen resulteert in een van de mogelijke toestanden.</span><span class="sxs-lookup"><span data-stu-id="d73ae-157">**Quantum measurement** - The act of observing a quantum particle in superposition and resulting in one of the possible states.</span></span>
- <span data-ttu-id="d73ae-158">**Verstrengeling**: de mogelijkheid van kwantumdeeltjes om de meetresultaten met elkaar te correleren.</span><span class="sxs-lookup"><span data-stu-id="d73ae-158">**Entanglement** - The ability of quantum particles to correlate their measurement results with each other.</span></span>
- <span data-ttu-id="d73ae-159">**Qubit**: de basiseenheid van informatie bij kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="d73ae-159">**Qubit** - The basic unit of information in quantum computing.</span></span> <span data-ttu-id="d73ae-160">Een qubit vertegenwoordigt een kwantumdeeltje in superpositie van alle mogelijke toestanden.</span><span class="sxs-lookup"><span data-stu-id="d73ae-160">A qubit represents a quantum particle in superposition of all possible states.</span></span>
- <span data-ttu-id="d73ae-161">**Interferentie**: intrinsiek gedrag van een qubit vanwege superpositie om de kans op ineenstorting tot de ene of andere toestand te beïnvloeden.</span><span class="sxs-lookup"><span data-stu-id="d73ae-161">**Interference** - Intrinsic behavior of a qubit due to superposition to influence the probability of it collapsing one way or another.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d73ae-162">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="d73ae-162">Next Steps</span></span>

[<span data-ttu-id="d73ae-163">Kwantumcomputers en kwantumsimulators</span><span class="sxs-lookup"><span data-stu-id="d73ae-163">Quantum computers and quantum simulators</span></span>](xref:microsoft.quantum.overview.simulators)