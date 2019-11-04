---
title: Inleiding in de bibliotheek voor kwantumberekening | Microsoft Docs
description: Inleiding in de bibliotheek voor kwantumberekening
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.intro
ms.openlocfilehash: efd1a712616534ac281433fc008f0983271881d7
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442444"
---
# <a name="introduction-to-the-quantum-numerics-library"></a><span data-ttu-id="d10dd-103">Inleiding in de bibliotheek voor kwantumberekening</span><span class="sxs-lookup"><span data-stu-id="d10dd-103">Introduction to the Quantum Numerics Library</span></span>

<span data-ttu-id="d10dd-104">Veel kwantumalgoritmen zijn gebaseerd op zogeheten [oracle](xref:microsoft.quantum.concepts.oracles) die wiskundige functies uitvoeren op een superpositie van invoer.</span><span class="sxs-lookup"><span data-stu-id="d10dd-104">Many quantum algorithms rely on [oracles](xref:microsoft.quantum.concepts.oracles) that evaluate mathematical functions on a superposition of inputs.</span></span>
<span data-ttu-id="d10dd-105">Het belangrijkste onderdeel van het Shor-algoritme voert bijvoorbeeld $f(x) = a^x\operatorname{mod} N$ uit voor een vaste $a$, het te factoriseren getal $N$ en een geheel $2n$-qubitgetal in een uniforme superpositie over alle $2n$-strings.</span><span class="sxs-lookup"><span data-stu-id="d10dd-105">The main component of Shor's algorithm, for example, evaluates $f(x) = a^x\operatorname{mod} N$ for a fixed $a$, the number to factor $N$, and $x$ a $2n$-qubit integer in a uniform superposition over all $2n$-bit strings.</span></span>

<span data-ttu-id="d10dd-106">Om het Shor-algoritme op een echte kwantumcomputer te kunnen gebruiken, moet deze functie worden geschreven in termen van de oorspronkelijke bewerkingen van de doelmachine.</span><span class="sxs-lookup"><span data-stu-id="d10dd-106">To run Shor's algorithm on an actual quantum computer, this function has to be written in terms of the native operations of the target machine.</span></span>
<span data-ttu-id="d10dd-107">Met behulp van de binaire representatie van $x$, waarbij $x_i$ verwijst naar de $i$-ste bit-telling vanaf de minst significante bit, kan $f(x)$ worden geschreven als $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.</span><span class="sxs-lookup"><span data-stu-id="d10dd-107">Using the binary representation of $x$ with $x_i$ denoting the $i$-th bit counting from the least-significant bit, $f(x)$ can be written as $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.</span></span>
<span data-ttu-id="d10dd-108">Dit kan weer worden geschreven als een product (mod N) van de termen $a^{2^i x_i}=(a^{2^i})^{x_i}$.</span><span class="sxs-lookup"><span data-stu-id="d10dd-108">In turn, this can be written as a product (mod N) of terms $a^{2^i x_i}=(a^{2^i})^{x_i}$.</span></span> <span data-ttu-id="d10dd-109">De functie $f(x)$ kan dus worden geïmplementeerd met behulp van een reeks van $2n$ (modulaire) vermenigvuldigingen met $a^{2^i}$ op voorwaarde dat $x_i$ niet nul is.</span><span class="sxs-lookup"><span data-stu-id="d10dd-109">The function $f(x)$ can thus be implemented using a sequence of $2n$ (modular) multiplications by $a^{2^i}$ conditional on $x_i$ being nonzero.</span></span> <span data-ttu-id="d10dd-110">De constanten $a^{2^i}$ kunnen vooraf worden berekend en modulo N worden gereduceerd voordat het algoritme wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d10dd-110">The constants $a^{2^i}$ can be precomputed and reduced modulo N before running the algorithm.</span></span>

<span data-ttu-id="d10dd-111">Deze reeks van gecontroleerde modulaire vermenigvuldigingen kan verder worden vereenvoudigd: elke vermenigvuldiging kan worden uitgevoerd met behulp van een reeks van $n$ gecontroleerde modulaire optellingen, en elke modulaire optellingen kan worden opgebouwd uit een reguliere optellingen en een comparator.</span><span class="sxs-lookup"><span data-stu-id="d10dd-111">This sequence of controlled modular multiplications can be simplified further: Each multiplication can be performed using a sequence of $n$ controlled modular additions; and each modular addition can be built from a regular addition and a comparator.</span></span>


<span data-ttu-id="d10dd-112">Aangezien er zoveel stappen nodig zijn om tot een daadwerkelijke implementatie te komen, zou het zeer nuttig zijn om van meet af aan passende functies te hebben.</span><span class="sxs-lookup"><span data-stu-id="d10dd-112">Given that so many steps are necessary to arrive at an actual implementation, it would be extremely helpful to have such functionality available from the start.</span></span>
<span data-ttu-id="d10dd-113">Daarom biedt de Quantum Development Kit ondersteuning voor een breed scala aan berekeningsfuncties.</span><span class="sxs-lookup"><span data-stu-id="d10dd-113">This is why the Quantum Development Kit provides support for a wide range of numerics functionality.</span></span>


## <a name="functionality"></a><span data-ttu-id="d10dd-114">Functionaliteit</span><span class="sxs-lookup"><span data-stu-id="d10dd-114">Functionality</span></span>

<span data-ttu-id="d10dd-115">Naast de tot dusver genoemde berekeningen met gehele getallen bevat de bibliotheek voor berekeningen ook</span><span class="sxs-lookup"><span data-stu-id="d10dd-115">Besides the integer arithmetic mentioned thus far, the numerics library provides</span></span>

 - <span data-ttu-id="d10dd-116">Functies voor gehele getallen met en zonder tekens (vermenigvuldigen, kwadrateren, delen met rest, inversie enz.) met één of twee gehele kwantumgetallen als input</span><span class="sxs-lookup"><span data-stu-id="d10dd-116">(Un)signed integer functionality (multiply, square, division with remainder, inversion, ...) with one or two quantum integer numbers as input</span></span>
 - <span data-ttu-id="d10dd-117">Functies voor vaste-puntgetallen (optellen / aftrekken, vermenigvuldigen, kwadrateren, 1/x, polynomiale berekening) met een of twee kwantumgetallen met vaste punten als input</span><span class="sxs-lookup"><span data-stu-id="d10dd-117">Fixed-point functionality (add / subtract, multiply, square, 1/x, polynomial evaluation) with one or two quantum fixed-point numbers as input</span></span>

## <a name="getting-started"></a><span data-ttu-id="d10dd-118">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="d10dd-118">Getting started</span></span>

<span data-ttu-id="d10dd-119">Om aan de slag te gaan met de bibliotheek voor berekeningen, raadpleegt u de [ installatiegids](xref:microsoft.quantum.numerics.installation) en meer informatie over het [gebruik van de bibliotheek voor berekeningen](xref:microsoft.quantum.numerics.usage).</span><span class="sxs-lookup"><span data-stu-id="d10dd-119">To get started with the Numerics Library, check out the [installation guide](xref:microsoft.quantum.numerics.installation) and more information on [using the Numerics Library](xref:microsoft.quantum.numerics.usage).</span></span>
