---
title: Kwantum-oracles
description: Informatie over het werken met en het definiëren van Quantum Oracle, Black Box-bewerkingen die worden gebruikt als invoer voor een ander algoritme.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 747c08df110f1f10efe552628d15e3500509b690
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269555"
---
# <a name="quantum-oracles"></a><span data-ttu-id="2ac5e-103">Quantum Oracle</span><span class="sxs-lookup"><span data-stu-id="2ac5e-103">Quantum Oracles</span></span>

<span data-ttu-id="2ac5e-104">Een Oracle-$O $ is een Black Box-bewerking die als invoer wordt gebruikt voor een ander algoritme.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="2ac5e-105">Dergelijke bewerkingen worden vaak gedefinieerd met behulp van een klassieke functie $f: \\ {0, 1 \\ } ^ n \to \\ {0, 1 \\ } ^ m $ die een $n $ bits binaire invoer maakt en een $m $ -bits binaire uitvoer produceert.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="2ac5e-106">Als u dit wilt doen, moet u een bepaalde binaire invoer $x = (x_ {0 } , x_ {1 } , \dots, x_ {n-1 } ) $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="2ac5e-107">We kunnen Qubit Staten labelen als $ \ket { \vec{x } } = \ket{x_ {0 } } \otimes \ket{x_ {1 } } \otimes \cdots \otimes \ket{x_ {n-1 } } $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="2ac5e-108">We kunnen eerst proberen om $O te definiëren $ , zodat $O \ket {x } = \ket{f (x)} $, maar dit heeft een aantal problemen.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="2ac5e-109">Ten eerste $f $ mogelijk een andere grootte van invoer en uitvoer ($n \ne m $ ), zodat het Toep assen $ van $O het aantal qubits in de kassa wijzigt.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="2ac5e-110">Ten tweede, zelfs als $n = m $ , mag de functie niet omkeerbaar zijn: als $f (x) = f (y) $ voor sommige $x \ne y $ , $O \ket {x } = O \ket {y } $, maar $O ^ \dagger o \ket {x } \ne o ^ \dagger o \ket {y } $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="2ac5e-111">Dit betekent dat we de adjoint-bewerking niet kunnen bouwen $O ^ \dagger $ en dat er voor Oracle een adjoint is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="2ac5e-112">Het definiëren van een Oracle op basis van de reken status</span><span class="sxs-lookup"><span data-stu-id="2ac5e-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="2ac5e-113">Deze problemen kunnen worden opgelost door een tweede REGI ster van $m $ qubits te introduceren om ons antwoord te houden.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="2ac5e-114">Vervolgens definiëren we het effect van de Oracle op alle reken kundige basis Staten: voor alle $x \in \\ {0, 1 \\ } ^ n $ en $y \in \\ {0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="2ac5e-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="2ac5e-115">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-115">$$ \begin{align}</span></span>
    <span data-ttu-id="2ac5e-116">O (\ket{x } \otimes \ket{y } ) = \ket{x } \otimes \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-116">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="2ac5e-117">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-117">\end{align}</span></span>
$$

<span data-ttu-id="2ac5e-118">Nu $O = O ^ \dagger $ per constructie, waardoor we beide problemen hebben opgelost.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-118">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="2ac5e-119">Als u wilt zien dat $O = O ^ {\dagger $, moet u er } rekening mee houden dat $O ^ 2 = \boldone $ sinds $a \oplus b \oplus b = a $ voor alle $a, b \in \{ 0, 1 \} $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-119">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="2ac5e-120">Als gevolg hiervan $O \ket{x } \ket{y \oplus f (x)} = \ket{x } \ket{y \oplus f (x) \oplus f (x)} = \ket{x } \ket{y } $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-120">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="2ac5e-121">Het is belang rijk dat u een Oracle op deze manier definieert voor elke berekening van de status $ \ket{x } \ket{y } $ definieert hoe $O $ worden uitgevoerd voor een andere status.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-121">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="2ac5e-122">Dit volgt onmiddellijk van het feit dat $O $ , zoals alle Quantum bewerkingen, lineair is in de status waarop het wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-122">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="2ac5e-123">Denk na over de bewerking Hadamard, bijvoorbeeld die is gedefinieerd door $H \ket{0 } = \ket { +} $ en $H \ket{1 } = \ket { -} $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-123">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="2ac5e-124">Als we willen weten hoe $H $ op $ \ket { +} $ werkt, kunnen we gebruiken dat $H $ lineair is,</span><span class="sxs-lookup"><span data-stu-id="2ac5e-124">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="2ac5e-125">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-125">$$ \begin{align}</span></span>
<span data-ttu-id="2ac5e-126">H \ket { +} & = \frac{1 } {\sqrt{2 } } H (\ket{0 } + \ket{1 } ) = \frac{1 } {\sqrt{2 } } (H \ket {0 } + H \ket {1 } ) \\ \\ & = \frac{1 } {\sqrt{2 } } (\ket { +} + \ket { -}) = \frac12 (\ket{0 } + \ket{1 } + \ket{0 } -\ket{1 } ) = \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="2ac5e-126">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="2ac5e-127">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-127">\end{align}</span></span>
$$

<span data-ttu-id="2ac5e-128">In het geval van het definiëren van de Oracle $ -$O, kunnen we ook gebruiken dat elke status $ \ket { \psi } $ op $n + m $ qubits kan worden geschreven als</span><span class="sxs-lookup"><span data-stu-id="2ac5e-128">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="2ac5e-129">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-129">$$ \begin{align}</span></span>
<span data-ttu-id="2ac5e-130">\ket { \psi } & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-130">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
<span data-ttu-id="2ac5e-131">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-131">\end{align}</span></span>
$$

<span data-ttu-id="2ac5e-132">waarbij $ \alpha: \\ {0, 1 \\ } ^ n \times \\ {0, 1 \\ } ^ m \to \mathbb{C } $ staat voor de coëfficiënten van de status $ \ket { \psi } $.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-132">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="2ac5e-133">Zeep</span><span class="sxs-lookup"><span data-stu-id="2ac5e-133">Thus,</span></span>

<span data-ttu-id="2ac5e-134">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-134">$$ \begin{align}</span></span>
<span data-ttu-id="2ac5e-135">O \ket { \psi } & = O \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y } \\ \\ & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) O \ket{x } \ket{y } \\ \\ & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-135">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="2ac5e-136">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-136">\end{align}</span></span>
$$

## <a name="phase-oracles"></a><span data-ttu-id="2ac5e-137">Fase Oracle</span><span class="sxs-lookup"><span data-stu-id="2ac5e-137">Phase oracles</span></span>
<span data-ttu-id="2ac5e-138">Het is ook mogelijk om $f te coderen $ in een Oracle-$O $ door een _fase_ toe te passen op basis van de invoer voor $O $ .</span><span class="sxs-lookup"><span data-stu-id="2ac5e-138">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="2ac5e-139">We kunnen bijvoorbeeld $O definiëren $ die $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-139">For instance, we might define $O$ such that $$ \begin{align}</span></span>
    <span data-ttu-id="2ac5e-140">O \ket{x } = (-1) ^ {f (x)} \ket{x } .</span><span class="sxs-lookup"><span data-stu-id="2ac5e-140">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="2ac5e-141">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-141">\end{align}</span></span>
<span data-ttu-id="2ac5e-142">$ $ Als een fase Oracle in eerste instantie op een registratie wordt uitgevoerd in de status van een berekening $ \ket{x } $, is deze fase een globale fase en daarom niet waarneembaar.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-142">$$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="2ac5e-143">Maar zo'n Oracle kan een zeer krachtige bron zijn als deze wordt toegepast op een superpositie of als een beheerde bewerking.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-143">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="2ac5e-144">U kunt bijvoorbeeld een fase orcale $O _f $ voor een Qubit-functie $f gebruiken $ .</span><span class="sxs-lookup"><span data-stu-id="2ac5e-144">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="2ac5e-145">Vervolgens $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-145">Then, $$ \begin{align}</span></span>
    <span data-ttu-id="2ac5e-146">O_f \ket { +} & = O_f (\ket{0 } + \ket{1 } )/\sqrt{2 } \\ \\ & = ((-1) ^ {f (0)} \ket{0 } + (-1) ^ {f (1)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} (\ket{0 } + (-1) ^ {f (1)-f (0)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket { +}.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-146">O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="2ac5e-147">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2ac5e-147">\end{align}</span></span>
$$

<span data-ttu-id="2ac5e-148">In het algemeen kunnen beide weer gaven van Oracle worden uitgebreid met klassieke functies die echte aantallen retour neren in plaats van slechts één bit.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-148">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="2ac5e-149">Het kiezen van de beste manier om een Oracle te implementeren, is afhankelijk van hoe deze Oracle wordt gebruikt binnen een bepaalde algoritme.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-149">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="2ac5e-150">Zo is [Deutsch-Jozsa-algoritme](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) afhankelijk van de Oracle die in de eerste manier is geïmplementeerd, terwijl het [algoritme van Grover afhankelijk is](https://en.wikipedia.org/wiki/Grover's_algorithm) van de Oracle die op de tweede manier is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-150">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="2ac5e-151">Voor meer informatie wordt de discussie in [Gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465)voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="2ac5e-151">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
