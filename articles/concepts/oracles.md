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
# <a name="quantum-oracles"></a>Quantum Oracle

Een Oracle-$O $ is een Black Box-bewerking die als invoer wordt gebruikt voor een ander algoritme.
Dergelijke bewerkingen worden vaak gedefinieerd met behulp van een klassieke functie $f: \\ {0, 1 \\ } ^ n \to \\ {0, 1 \\ } ^ m $ die een $n $ bits binaire invoer maakt en een $m $ -bits binaire uitvoer produceert.
Als u dit wilt doen, moet u een bepaalde binaire invoer $x = (x_ {0 } , x_ {1 } , \dots, x_ {n-1 } ) $.
We kunnen Qubit Staten labelen als $ \ket { \vec{x } } = \ket{x_ {0 } } \otimes \ket{x_ {1 } } \otimes \cdots \otimes \ket{x_ {n-1 } } $.

We kunnen eerst proberen om $O te definiëren $ , zodat $O \ket {x } = \ket{f (x)} $, maar dit heeft een aantal problemen.
Ten eerste $f $ mogelijk een andere grootte van invoer en uitvoer ($n \ne m $ ), zodat het Toep assen $ van $O het aantal qubits in de kassa wijzigt.
Ten tweede, zelfs als $n = m $ , mag de functie niet omkeerbaar zijn: als $f (x) = f (y) $ voor sommige $x \ne y $ , $O \ket {x } = O \ket {y } $, maar $O ^ \dagger o \ket {x } \ne o ^ \dagger o \ket {y } $.
Dit betekent dat we de adjoint-bewerking niet kunnen bouwen $O ^ \dagger $ en dat er voor Oracle een adjoint is gedefinieerd.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>Het definiëren van een Oracle op basis van de reken status
Deze problemen kunnen worden opgelost door een tweede REGI ster van $m $ qubits te introduceren om ons antwoord te houden.
Vervolgens definiëren we het effect van de Oracle op alle reken kundige basis Staten: voor alle $x \in \\ {0, 1 \\ } ^ n $ en $y \in \\ {0, 1 \\ } ^ m $ ,

$ $ \begin{align}
    O (\ket{x } \otimes \ket{y } ) = \ket{x } \otimes \ket{y \oplus f (x)}.
\end{align}
$$

Nu $O = O ^ \dagger $ per constructie, waardoor we beide problemen hebben opgelost.

> [!TIP]
> Als u wilt zien dat $O = O ^ {\dagger $, moet u er } rekening mee houden dat $O ^ 2 = \boldone $ sinds $a \oplus b \oplus b = a $ voor alle $a, b \in \{ 0, 1 \} $.
> Als gevolg hiervan $O \ket{x } \ket{y \oplus f (x)} = \ket{x } \ket{y \oplus f (x) \oplus f (x)} = \ket{x } \ket{y } $.

Het is belang rijk dat u een Oracle op deze manier definieert voor elke berekening van de status $ \ket{x } \ket{y } $ definieert hoe $O $ worden uitgevoerd voor een andere status.
Dit volgt onmiddellijk van het feit dat $O $ , zoals alle Quantum bewerkingen, lineair is in de status waarop het wordt uitgevoerd.
Denk na over de bewerking Hadamard, bijvoorbeeld die is gedefinieerd door $H \ket{0 } = \ket { +} $ en $H \ket{1 } = \ket { -} $.
Als we willen weten hoe $H $ op $ \ket { +} $ werkt, kunnen we gebruiken dat $H $ lineair is,

$ $ \begin{align}
H \ket { +} & = \frac{1 } {\sqrt{2 } } H (\ket{0 } + \ket{1 } ) = \frac{1 } {\sqrt{2 } } (H \ket {0 } + H \ket {1 } ) \\ \\ & = \frac{1 } {\sqrt{2 } } (\ket { +} + \ket { -}) = \frac12 (\ket{0 } + \ket{1 } + \ket{0 } -\ket{1 } ) = \ket{0 } .
\end{align}
$$

In het geval van het definiëren van de Oracle $ -$O, kunnen we ook gebruiken dat elke status $ \ket { \psi } $ op $n + m $ qubits kan worden geschreven als

$ $ \begin{align}
\ket { \psi } & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y}
\end{align}
$$

waarbij $ \alpha: \\ {0, 1 \\ } ^ n \times \\ {0, 1 \\ } ^ m \to \mathbb{C } $ staat voor de coëfficiënten van de status $ \ket { \psi } $. Zeep

$ $ \begin{align}
O \ket { \psi } & = O \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y } \\ \\ & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) O \ket{x } \ket{y } \\ \\ & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y \oplus f (x)}.
\end{align}
$$

## <a name="phase-oracles"></a>Fase Oracle
Het is ook mogelijk om $f te coderen $ in een Oracle-$O $ door een _fase_ toe te passen op basis van de invoer voor $O $ .
We kunnen bijvoorbeeld $O definiëren $ die $ $ \begin{align}
    O \ket{x } = (-1) ^ {f (x)} \ket{x } .
\end{align}
$ $ Als een fase Oracle in eerste instantie op een registratie wordt uitgevoerd in de status van een berekening $ \ket{x } $, is deze fase een globale fase en daarom niet waarneembaar.
Maar zo'n Oracle kan een zeer krachtige bron zijn als deze wordt toegepast op een superpositie of als een beheerde bewerking.
U kunt bijvoorbeeld een fase orcale $O _f $ voor een Qubit-functie $f gebruiken $ .
Vervolgens $ $ \begin{align}
    O_f \ket { +} & = O_f (\ket{0 } + \ket{1 } )/\sqrt{2 } \\ \\ & = ((-1) ^ {f (0)} \ket{0 } + (-1) ^ {f (1)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} (\ket{0 } + (-1) ^ {f (1)-f (0)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket { +}.
\end{align}
$$

In het algemeen kunnen beide weer gaven van Oracle worden uitgebreid met klassieke functies die echte aantallen retour neren in plaats van slechts één bit.

Het kiezen van de beste manier om een Oracle te implementeren, is afhankelijk van hoe deze Oracle wordt gebruikt binnen een bepaalde algoritme.
Zo is [Deutsch-Jozsa-algoritme](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) afhankelijk van de Oracle die in de eerste manier is geïmplementeerd, terwijl het [algoritme van Grover afhankelijk is](https://en.wikipedia.org/wiki/Grover's_algorithm) van de Oracle die op de tweede manier is geïmplementeerd.


Voor meer informatie wordt de discussie in [Gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465)voorgesteld.
