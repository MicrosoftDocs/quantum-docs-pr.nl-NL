---
title: Quantum Oracle | Microsoft Docs
description: Quantum Oracle
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
ms.openlocfilehash: 96949b371a3a5a1135d624690933a48ea0214a2e
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184709"
---
# <a name="quantum-oracles"></a><span data-ttu-id="41af5-103">Quantum Oracle</span><span class="sxs-lookup"><span data-stu-id="41af5-103">Quantum Oracles</span></span>

<span data-ttu-id="41af5-104">Een Oracle-$O $ is een "Black Box"-bewerking die als invoer wordt gebruikt voor een ander algoritme.</span><span class="sxs-lookup"><span data-stu-id="41af5-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="41af5-105">Dergelijke bewerkingen worden vaak gedefinieerd met behulp van een klassieke functie $f: \\{0, 1\\} ^ n \to \\{0, 1\\} ^ m $, die een $n $-bit binaire invoer maakt en een $m $-bits binaire uitvoer produceert.</span><span class="sxs-lookup"><span data-stu-id="41af5-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="41af5-106">Als u dit wilt doen, moet u een bepaalde binaire invoer $x = (x_{0}, x_{1}, \dots, x_ {n-1}) $.</span><span class="sxs-lookup"><span data-stu-id="41af5-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="41af5-107">We kunnen Qubit Staten labelen als $ \ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}} $.</span><span class="sxs-lookup"><span data-stu-id="41af5-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="41af5-108">We kunnen eerst proberen om $O $ te definiëren, zodat $O \ket{x} = \ket{f (x)} $, maar dit heeft een aantal problemen.</span><span class="sxs-lookup"><span data-stu-id="41af5-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="41af5-109">Ten eerste kan $f $ een andere grootte van invoer en uitvoer hebben ($n \ne m $), zodat $O $ het aantal qubits in de kassa wijzigt.</span><span class="sxs-lookup"><span data-stu-id="41af5-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="41af5-110">Ten tweede, zelfs als $n = m $, mag de functie niet omkeerbaar zijn: als $f (x) = f (y) $ voor sommige $x \ne y $, $O \ket{x} = O\ket {y} $, maar $O ^ \dagger O\ket {x} \ne O ^ \dagger O\ket {y} $.</span><span class="sxs-lookup"><span data-stu-id="41af5-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="41af5-111">Dit betekent dat we de adjoint-bewerking niet kunnen bouwen $O ^ \dagger $ en dat er voor Oracle een adjoint is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="41af5-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="41af5-112">Het definiëren van een Oracle op basis van de reken status</span><span class="sxs-lookup"><span data-stu-id="41af5-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="41af5-113">Deze problemen kunnen worden opgelost door een tweede REGI ster van $m $ qubits te introduceren om ons antwoord te houden.</span><span class="sxs-lookup"><span data-stu-id="41af5-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="41af5-114">Vervolgens definiëren we het effect van de Oracle op alle reken kundige basis Staten: voor alle $x \in \\{0, 1\\} ^ n $ en $y \in \\{0, 1\\} ^ m $,</span><span class="sxs-lookup"><span data-stu-id="41af5-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="41af5-115">$ $ \begin{align} O (\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="41af5-115">$$ \begin{align} O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="41af5-116">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="41af5-116">\end{align} $$</span></span>

<span data-ttu-id="41af5-117">Nu $O = O ^ \dagger $ per constructie, waardoor we beide problemen hebben opgelost.</span><span class="sxs-lookup"><span data-stu-id="41af5-117">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="41af5-118">Als u wilt zien dat $O = O ^ {\dagger} $, moet u er rekening mee houden dat $O ^ 2 = \boldone $ sinds $a \oplus b \oplus b = a $ voor alle $a, b \in \{0, 1\}$.</span><span class="sxs-lookup"><span data-stu-id="41af5-118">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="41af5-119">Als gevolg hiervan $O \ket{x} \ket{y \oplus f (x)} = \ket{x} \ket{y \oplus f (x) \oplus f (x)} = \ket{x} \ket{y} $.</span><span class="sxs-lookup"><span data-stu-id="41af5-119">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="41af5-120">Het is belang rijk dat u een Oracle op deze manier definieert voor elke reken kundige status $ \ket{x}\ket{y} $ definieert ook hoe $O $ voor een andere status optreedt.</span><span class="sxs-lookup"><span data-stu-id="41af5-120">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="41af5-121">Dit volgt onmiddellijk van het feit dat $O $, zoals alle Quantum bewerkingen, lineair is in de status waarop het wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="41af5-121">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="41af5-122">Houd rekening met de Hadamard-bewerking, bijvoorbeeld die is gedefinieerd door $H \ket{0} = \ket{+} $ en $H \ket{1} = \ket{-}$.</span><span class="sxs-lookup"><span data-stu-id="41af5-122">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="41af5-123">Als we willen weten hoe $H $ op $ \ket{+} $ reageert, kunnen we gebruiken dat $H $ lineair is,</span><span class="sxs-lookup"><span data-stu-id="41af5-123">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="41af5-124">$ $ \begin{align} H\ket {+} & = \frac{1}{\sqrt{2}} H (\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ Ket {+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0}-\ket{1}) = \ket{0}.</span><span class="sxs-lookup"><span data-stu-id="41af5-124">$$ \begin{align} H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="41af5-125">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="41af5-125">\end{align} $$</span></span>

<span data-ttu-id="41af5-126">In het geval van het definiëren van onze Oracle-$O $, kunnen we ook gebruiken dat elke status $ \ket{\psi} $ op $n + m $ qubits kan worden geschreven als</span><span class="sxs-lookup"><span data-stu-id="41af5-126">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="41af5-127">$ $ \begin{align} \ket{\psi} & = \sum_{x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \alpha (x, y) \ket{x} \ket{y} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="41af5-127">$$ \begin{align} \ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \end{align} $$</span></span>

<span data-ttu-id="41af5-128">waar $ \alpha: \\{0, 1\\} ^ n \times \\{0, 1\\} ^ m \to \mathbb{C} $ staat voor de coëfficiënten van de status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="41af5-128">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="41af5-129">Zeep</span><span class="sxs-lookup"><span data-stu-id="41af5-129">Thus,</span></span>

<span data-ttu-id="41af5-130">$ $ \begin{align} O \ket{\psi} & = O \sum_{x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \alpha (x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0 , 1\\} ^ n, y \in \\{0, 1\\} ^ m} \alpha (x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\} ^ n, y \in \\{0 , 1\\} ^ m} \alpha (x, y) \ket{x} \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="41af5-130">$$ \begin{align} O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="41af5-131">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="41af5-131">\end{align} $$</span></span>

## <a name="phase-oracles"></a><span data-ttu-id="41af5-132">Fase Oracle</span><span class="sxs-lookup"><span data-stu-id="41af5-132">Phase oracles</span></span>
<span data-ttu-id="41af5-133">Het is ook mogelijk om $f $ te coderen in een Oracle-$O $ door een _fase_ toe te passen op basis van de invoer voor $O $.</span><span class="sxs-lookup"><span data-stu-id="41af5-133">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="41af5-134">We kunnen bijvoorbeeld $O $ zodanig definiëren dat $ $ \begin{align} O \ket{x} = (-1) ^ {f (x)} \ket{x}.</span><span class="sxs-lookup"><span data-stu-id="41af5-134">For instance, we might define $O$ such that $$ \begin{align} O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="41af5-135">\end{align} $ $ als een Phase Oracle in eerste instantie een registratie op basis van een reken status $ \ket{x} $ uitvoert, is deze fase een globale fase en daarom niet waarneembaar.</span><span class="sxs-lookup"><span data-stu-id="41af5-135">\end{align} $$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="41af5-136">Maar zo'n Oracle kan een zeer krachtige bron zijn als deze wordt toegepast op een superpositie of als een beheerde bewerking.</span><span class="sxs-lookup"><span data-stu-id="41af5-136">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="41af5-137">Denk bijvoorbeeld aan een fase orcale $O _f $ voor een functie met één Qubit $f $.</span><span class="sxs-lookup"><span data-stu-id="41af5-137">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="41af5-138">Then, $ $ \begin{align} O_f \ket{+} & = O_f (\ket{0} + \ket{1})/\sqrt{2} \\\\ & = ((-1) ^ {f (0)} \ket{0} + (-1) ^ {f (1)} \ket{1})/\sqrt{2} \\\\ & = (-1) ^ {f ( 0)} (\ket{0} + (-1) ^ {f (1)-f (0)} \ket{1})/\sqrt{2} \\\\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket{+}.</span><span class="sxs-lookup"><span data-stu-id="41af5-138">Then, $$ \begin{align} O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="41af5-139">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="41af5-139">\end{align} $$</span></span>

<span data-ttu-id="41af5-140">In het algemeen kunnen beide weer gaven van Oracle worden uitgebreid met klassieke functies die echte aantallen retour neren in plaats van slechts één bit.</span><span class="sxs-lookup"><span data-stu-id="41af5-140">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="41af5-141">Het kiezen van de beste manier om een Oracle te implementeren, is afhankelijk van hoe deze Oracle wordt gebruikt binnen een bepaalde algoritme.</span><span class="sxs-lookup"><span data-stu-id="41af5-141">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="41af5-142">Zo is [Deutsch-Jozsa-algoritme](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) afhankelijk van de Oracle die in de eerste manier is geïmplementeerd, terwijl het [algoritme van Grover afhankelijk is](https://en.wikipedia.org/wiki/Grover's_algorithm) van de Oracle die op de tweede manier is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="41af5-142">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="41af5-143">Voor meer informatie wordt de discussie in [Gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465)voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="41af5-143">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
