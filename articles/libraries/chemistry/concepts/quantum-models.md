---
title: Quantum modellen voor elektronische systemen | Microsoft Docs
description: Quantum modellen voor elektronische systemen conceptuele documenten
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantummodels
ms.openlocfilehash: 45d134333c8a3c8937d206cb0a4a9cc6101a85df
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184148"
---
# <a name="quantum-models-for-electronic-systems"></a>Quantum modellen voor elektronische systemen

Om elektronische systemen te simuleren, moeten we eerst de Hamiltonian opgeven, die kan worden gevonden door de canonieke kwantisatiefouten-procedure die hierboven wordt beschreven.
In het bijzonder, voor $N _e $ electrons met Momenta $p _I $ (in drie dimensies) en massa $m _e $ en positie vectoren $x _I $ samen met de nuclei met kosten $Z _k e $ op posities $y _k $, de Hamiltonian-operator leest \begin{Equation} \hat{H} = \sum\_{i = 1} ^ {N @no_ _t_1_ e} \frac{\hat{p}\_i ^ 2} {2 min.\_e} + \frac{1}{2}\sum\_{i\ne j} \frac{e ^ 2} {| \hat{x}\_i-\hat{x}\_j |}-\sum\_{i , k} \frac{Z\_ke ^ 2} {| \hat{x}\_i-{y}\_k |} + \frac{1}{2} \sum_{k\ne k} \frac{Z\_kZ\_{k '} e ^ 2} {| y\_k-y\_k ' |}. \label{EQ: \end{Equation}} de Momenta-Opera tors $ \hat{p}\_i ^ 2 $ kunnen worden weer gegeven in echte ruimte als Laplacian-Opera Tors, d.w.z. $ \hat{p}\_i ^ 2 =-\partial\_{x\_i} ^ 2-\partial\_{y\_i} ^ 2-\partial\_{z\_i} ^ 2 $.
Hier hebben we de veronderstelling gemaakt dat de nuclei in rust zijn voor het molecuul.
Dit staat bekend als de Oppenheimer benadering en is doorgaans geldig voor het energie spectrum met een laag energie niveau van $ \hat{H} $, aangezien de massa van het elektroeen ongeveer $1/1836 $ de massa van een proton.
Deze Hamiltonian-operator kan eenvoudig worden gevonden door de energie te schrijven voor een systeem van $N\_e $ electrons en het canonieke kwantisatiefouten-proces toe te passen dat wordt beschreven in [Quantum Dynamics](xref:microsoft.quantum.chemistry.concepts.quantumdynamics).

Als u de unitary matrix representatie voor $e ^ {-i\hat {H} t} wilt maken, moet u de operator $ \hat{H} $ als matrix vertegenwoordigen.
Hiervoor moet u een coördinaten systeem of basis kiezen om het probleem in te representeren.
Als $ \psi_j $ bijvoorbeeld een reeks rechthoekige basis functies voor de $N _e $ electrons zijn, kunnen we de matrix definiëren

\begin{Equation} H\_{i, j} = \int\_{-\infty} ^ \infty\int\_{-\infty} ^ \infty \psi ^ {\*}\_i (x\_1) \hat{H} \psi\_j (x\_2) \dd ^ 3x\_1 \dd ^ 3x\_2. \ label {EQ: discreteHam} \end{Equation}

In principe is de operator $ \hat{H} $ ongebonden en reageert deze niet op een beperkt afmetings gebied, de matrix met elementen $H\_\{i, j\}$ hierboven.
Dit betekent dat fouten worden gemaakt door te klein van een basisset te kiezen. het kiezen van een grote basis kan er echter toe zorgen dat de chemische dynamiek niet praktisch wordt gesimuleerd.
Daarom is het kiezen van een basis waarmee het probleem beknopt kan worden aangegeven, het is essentieel om het probleem met de elektronische structuur op te lossen.

Er zijn veel geschikte bases die kunnen worden gebruikt en de keuze van een goede basis om het probleem aan te passen, is veel van de grafische schei kunde.
Misschien zijn de eenvoudigste, dergelijke basis sets Slater (WAARSCHUWINGSD) die zijn (gevormde) oplossingen voor de Schrödinger-vergelijking (dus eigenfunctions van $ \hat{H} $) voor waterstof achtige atomen.
Andere basis sets, zoals een vlieg tuig of een laag ruimte niveau, kunnen worden gebruikt en voor meer informatie hebben we de nieuws lezer naar de standaard tekst [' moleculaire elektronische-structuur theorie '](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119019572) door Helgaker.

Hoewel de staten die in het bovenstaande model worden gebruikt, een wille keurige vorm kunnen hebben, plaatsen Quantum monteurs beperkingen op de statussen die in de natuur kunnen worden gevonden.
Met name moeten alle geldige elektronische Quantum Staten antisymmetrisch zijn onder uitwisseling van elektronen labels.
Dat wil zeggen dat $ \psi (x_1, x_2) $ de functie Wave had voor de gezamenlijke Quantum status van twee electrons, dan moeten we dat $ $ \psi (x_1, x_2) =-\psi (x_2, x_1) hebben.
$ $ Het uitsluitings principe van de Pauli dat twee electrons in dezelfde Quantum staat verbiedt, is fascinatingly, een rechtstreeks gevolg van deze wet dat kan worden afgeleid van het feit dat als we twee electrons hebben gewisseld op dezelfde positie $ \psi (x_1, x_1) \mapsto \psi ( x_1, x_1) \ne-\psi (x_1, x_1) $ tenzij $ \psi (x_1, x_1) = 0 $.
Daarom moeten de initiële statussen worden gekozen voor het volgen van deze antisymmetrie-eigenschap en op zijn beurt nooit twee electrons in dezelfde staat tegelijk hebben.
Dit is van cruciaal belang voor de elektronische structuur, omdat het niet meer dan één electrons in dezelfde staat kan bevinden. op zijn beurt kunnen quantum computers een enkele Quantum bit gebruiken om het aantal electrons in een bepaalde Quantum status op te slaan.

Hoewel Quantum mechanismen kunnen worden gesimuleerd op een quantum computer door onderscheiden deze Staten, is de meeste werk in het veld van eschewed deze benadering omdat het veel qubits nodig heeft om de Staten op te slaan en een gecompliceerde status voorbereidings procedure nodig heeft om een niet-symmetrische begin status.
Gelukkig kunnen deze problemen echter worden sidestepped door het simulatie probleem vanuit een ander perspectief te bekijken.