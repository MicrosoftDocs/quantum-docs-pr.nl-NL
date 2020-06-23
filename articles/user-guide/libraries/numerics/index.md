---
title: Inleiding in de bibliotheek voor kwantumberekening | Microsoft Docs
description: Inleiding in de bibliotheek voor kwantumberekening
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.intro
ms.openlocfilehash: efd1a712616534ac281433fc008f0983271881d7
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273398"
---
# <a name="introduction-to-the-quantum-numerics-library"></a>Inleiding in de bibliotheek voor kwantumberekening

Veel kwantumalgoritmen zijn gebaseerd op zogeheten [oracle](xref:microsoft.quantum.concepts.oracles) die wiskundige functies uitvoeren op een superpositie van invoer.
Het belangrijkste onderdeel van het Shor-algoritme voert bijvoorbeeld $f(x) = a^x\operatorname{mod} N$ uit voor een vaste $a$, het te factoriseren getal $N$ en een geheel $2n$-qubitgetal in een uniforme superpositie over alle $2n$-strings.

Om het Shor-algoritme op een echte kwantumcomputer te kunnen gebruiken, moet deze functie worden geschreven in termen van de oorspronkelijke bewerkingen van de doelmachine.
Met behulp van de binaire representatie van $x$, waarbij $x_i$ verwijst naar de $i$-ste bit-telling vanaf de minst significante bit, kan $f(x)$ worden geschreven als $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.
Dit kan weer worden geschreven als een product (mod N) van de termen $a^{2^i x_i}=(a^{2^i})^{x_i}$. De functie $f(x)$ kan dus worden geïmplementeerd met behulp van een reeks van $2n$ (modulaire) vermenigvuldigingen met $a^{2^i}$ op voorwaarde dat $x_i$ niet nul is. De constanten $a^{2^i}$ kunnen vooraf worden berekend en modulo N worden gereduceerd voordat het algoritme wordt uitgevoerd.

Deze reeks van gecontroleerde modulaire vermenigvuldigingen kan verder worden vereenvoudigd: elke vermenigvuldiging kan worden uitgevoerd met behulp van een reeks van $n$ gecontroleerde modulaire optellingen, en elke modulaire optellingen kan worden opgebouwd uit een reguliere optellingen en een comparator.


Aangezien er zoveel stappen nodig zijn om tot een daadwerkelijke implementatie te komen, zou het zeer nuttig zijn om van meet af aan passende functies te hebben.
Daarom biedt de Quantum Development Kit ondersteuning voor een breed scala aan berekeningsfuncties.


## <a name="functionality"></a>Functionaliteit

Naast de tot dusver genoemde berekeningen met gehele getallen bevat de bibliotheek voor berekeningen ook

 - Functies voor gehele getallen met en zonder tekens (vermenigvuldigen, kwadrateren, delen met rest, inversie enz.) met één of twee gehele kwantumgetallen als input
 - Functies voor vaste-puntgetallen (optellen / aftrekken, vermenigvuldigen, kwadrateren, 1/x, polynomiale berekening) met een of twee kwantumgetallen met vaste punten als input

## <a name="getting-started"></a>Aan de slag

Om aan de slag te gaan met de bibliotheek voor berekeningen, raadpleegt u de [ installatiegids](xref:microsoft.quantum.numerics.installation) en meer informatie over het [gebruik van de bibliotheek voor berekeningen](xref:microsoft.quantum.numerics.usage).
