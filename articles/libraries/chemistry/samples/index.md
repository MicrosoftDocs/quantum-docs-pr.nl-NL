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
# <a name="quantum-chemistry-examples"></a>Voorbeelden kwantumchemie

In de kwantumchemische concepten hebben we handmatig hamiltonianen van fermionen geconstrueerd. Nu combineren we de algoritmen voor chemische simulatie zoals beschreven in [Hamiltoniaanse dynamica simuleren](xref:microsoft.quantum.libraries.standard.algorithms), met [kwantumfaseschatting](xref:microsoft.quantum.libraries.characterization) uit de canonbibliotheek. Hiermee kunnen we schattingen maken van energieniveaus in het gerepresenteerde molecuul: een van de belangrijkste toepassingen van kwantumchemie op een kwantumcomputer. 

In plaats van de termen van de hamiltoniaan een voor een te specificeren, behandelen we enkele voorbeelden waarmee we kwantumchemische experimenten op schaal kunnen uitvoeren. We beginnen met voorbeelden die een chemische hamiltoniaan laden die in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) is gecodeerd.

Ook op moleculen die te groot zijn voor [simulatie van hun volledige toestand](xref:microsoft.quantum.machines.full-state-simulator), kan nog steeds interessante wetenschap worden uitgevoerd. Zo kunnen bijvoorbeeld de kosten voor de uitvoering van grote chemische simulaties nog steeds worden geëvalueerd door middel van de [ trajectsimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).

Laten we nu een aantal interessante toepassingen van de bibliotheek voor chemische simulatie toelichten aan de hand van enkele voorbeelden.
