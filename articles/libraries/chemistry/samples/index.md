---
title: Voorbeeldtoepassingen voor kwantumchemie
description: Ontdek voorbeeldtoepassingen van de Microsoft-bibliotheek voor kwantumchemie.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples
ms.openlocfilehash: 5168fc8592d34a32ba67e5a0c4793aa17599fd35
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2020
ms.locfileid: "77906488"
---
# <a name="quantum-chemistry-examples"></a><span data-ttu-id="a9e7a-103">Voorbeelden kwantumchemie</span><span class="sxs-lookup"><span data-stu-id="a9e7a-103">Quantum chemistry examples</span></span>

<span data-ttu-id="a9e7a-104">In de kwantumchemische concepten hebben we handmatig hamiltonianen van fermionen geconstrueerd.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-104">In the quantum chemistry concepts, we manually constructed example fermion Hamiltonians.</span></span> <span data-ttu-id="a9e7a-105">Nu combineren we de algoritmen voor chemische simulatie zoals beschreven in [Hamiltoniaanse dynamica simuleren](xref:microsoft.quantum.libraries.standard.algorithms), met [kwantumfaseschatting](xref:microsoft.quantum.libraries.characterization) uit de canonbibliotheek.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-105">We now combine the chemistry simulation algorithms outlined in [Simulating Hamiltonian dynamics](xref:microsoft.quantum.libraries.standard.algorithms) with [quantum phase estimation](xref:microsoft.quantum.libraries.characterization) in the canon library.</span></span> <span data-ttu-id="a9e7a-106">Hiermee kunnen we schattingen maken van energieniveaus in het gerepresenteerde molecuul: een van de belangrijkste toepassingen van kwantumchemie op een kwantumcomputer.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-106">This combination allows us to obtain  estimates of energy levels in the represented molecule, which is one of the key applications of quantum chemistry on a quantum computer.</span></span> 

<span data-ttu-id="a9e7a-107">In plaats van de termen van de hamiltoniaan een voor een te specificeren, behandelen we enkele voorbeelden waarmee we kwantumchemische experimenten op schaal kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-107">Instead of specifying terms of the Hamiltonian one-by-one, we also work through some examples that allow us to perform quantum chemistry experiments at scale.</span></span> <span data-ttu-id="a9e7a-108">We beginnen met voorbeelden die een chemische hamiltoniaan laden die in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) is gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-108">We begin with examples that load a chemistry Hamiltonian encoded in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).</span></span>

<span data-ttu-id="a9e7a-109">Ook op moleculen die te groot zijn voor [simulatie van hun volledige toestand](xref:microsoft.quantum.machines.full-state-simulator), kan nog steeds interessante wetenschap worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-109">For molecules that are too large to simulate on the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), interesting science can still be performed.</span></span> <span data-ttu-id="a9e7a-110">Zo kunnen bijvoorbeeld de kosten voor de uitvoering van grote chemische simulaties nog steeds worden geëvalueerd door middel van de [ trajectsimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="a9e7a-110">For instance, the resource costs of performing large chemistry simulations may still be evaluated by targeting the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>

<span data-ttu-id="a9e7a-111">Laten we nu een aantal interessante toepassingen van de bibliotheek voor chemische simulatie toelichten aan de hand van enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="a9e7a-111">Let us now illustrate interesting applications of the chemistry simulation library through a few of the provided samples.</span></span>
