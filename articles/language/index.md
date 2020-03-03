---
title: De programmeertaal Q#
description: Inleiding tot de Q#-taal voor het ontwikkelen van kwantumprogramma's.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: b62e6866fc3609d95c26a5eab2a6eac325dfe330
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907372"
---
# <a name="the-q-programming-language"></a><span data-ttu-id="06a9b-103">De programmeertaal Q#</span><span class="sxs-lookup"><span data-stu-id="06a9b-103">The Q# Programming Language</span></span>

## <a name="introduction"></a><span data-ttu-id="06a9b-104">Inleiding</span><span class="sxs-lookup"><span data-stu-id="06a9b-104">Introduction</span></span>

<span data-ttu-id="06a9b-105">Een natuurlijk model voor kwantumberekening is de kwantumcomputer te behandelen als een coprocessor, vergelijkbaar met coprocessoren voor GPU's, FPGA's en andere adjunct-processoren.</span><span class="sxs-lookup"><span data-stu-id="06a9b-105">A natural model for quantum computation is to treat the quantum computer as a coprocessor, similar to that used for GPUs, FPGAs, and other adjunct processors.</span></span>
<span data-ttu-id="06a9b-106">De primaire besturingslogica voert klassieke code uit op een klassieke hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="06a9b-106">The primary control logic runs classical code on a classical "host" computer.</span></span>
<span data-ttu-id="06a9b-107">Zo nodig kan het hostprogramma een subroutine aanroepen die wordt uitgevoerd op de adjunct-processor.</span><span class="sxs-lookup"><span data-stu-id="06a9b-107">When appropriate and necessary, the host program can invoke a subroutine that runs on the adjunct processor.</span></span>
<span data-ttu-id="06a9b-108">Wanneer de subroutine is voltooid, krijgt het hostprogramma toegang tot de resultaten van de subroutine.</span><span class="sxs-lookup"><span data-stu-id="06a9b-108">When the subroutine completes, the host program gets access to the subroutine's results.</span></span>

<span data-ttu-id="06a9b-109">Q# (Q-sharp) is een domein-specifieke programmeertaal die wordt gebruikt voor het uitdrukken van kwantumalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="06a9b-109">Q# (Q-sharp) is a domain-specific programming language used for expressing quantum algorithms.</span></span>
<span data-ttu-id="06a9b-110">Q# kan worden gebruikt voor het schrijven van subroutines die worden uitgevoerd op een adjunct-kwantumprocessor, onder controle van een klassiek hostprogramma en een klassieke computer.</span><span class="sxs-lookup"><span data-stu-id="06a9b-110">It is to be used for writing subroutines that execute on an adjunct quantum processor, under the control of a classical host program and computer.</span></span>
<span data-ttu-id="06a9b-111">Totdat kwantumprocessoren algemeen beschikbaar zijn, worden Q#-subroutines uitgevoerd op een simulator.</span><span class="sxs-lookup"><span data-stu-id="06a9b-111">Until quantum processors are widely available, Q# subroutines execute on a simulator.</span></span>

<span data-ttu-id="06a9b-112">Q# bevat een kleine set primitieve typen, samen met twee manieren (matrices en tuples) voor het maken van nieuwe, gestructureerde typen.</span><span class="sxs-lookup"><span data-stu-id="06a9b-112">Q# provides a small set of primitive types, along with two ways (arrays and tuples) for creating new, structured types.</span></span>
<span data-ttu-id="06a9b-113">Het ondersteunt een basisproceduremodel voor het schrijven van programma's, met lussen en if/then-instructies.</span><span class="sxs-lookup"><span data-stu-id="06a9b-113">It supports a basic procedural model for writing programs, with loops and if/then statements.</span></span>
<span data-ttu-id="06a9b-114">Constructs van het hoogste niveau in Q# zijn door de gebruiker gedefinieerde typen, bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="06a9b-114">The top-level constructs in Q# are user defined types, operations, and functions.</span></span>

<span data-ttu-id="06a9b-115">In de volgende secties vindt u gedetailleerde informatie over het volgende:</span><span class="sxs-lookup"><span data-stu-id="06a9b-115">The following sections detail:</span></span>
- [<span data-ttu-id="06a9b-116">Het typemodel</span><span class="sxs-lookup"><span data-stu-id="06a9b-116">The Type Model</span></span>](xref:microsoft.quantum.language.type-model)
- [<span data-ttu-id="06a9b-117">Expressies</span><span class="sxs-lookup"><span data-stu-id="06a9b-117">Expressions</span></span>](xref:microsoft.quantum.language.expressions)
- [<span data-ttu-id="06a9b-118">Instructies</span><span class="sxs-lookup"><span data-stu-id="06a9b-118">Statements</span></span>](xref:microsoft.quantum.language.statements)
- [<span data-ttu-id="06a9b-119">Bestandsstructuur</span><span class="sxs-lookup"><span data-stu-id="06a9b-119">File Structure</span></span>](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a><span data-ttu-id="06a9b-120">Conventies</span><span class="sxs-lookup"><span data-stu-id="06a9b-120">Conventions</span></span>

<span data-ttu-id="06a9b-121">We streven naar een consistent gebruik van gangbare interpunctietekens in alle situaties.</span><span class="sxs-lookup"><span data-stu-id="06a9b-121">We are working to ensure that common punctuation marks are used consistently in all situations.</span></span>
<span data-ttu-id="06a9b-122">Hierdoor is Q# makkelijker te leren en te lezen omdat deze tekens altijd hetzelfde betekenen, en hetzelfde begrip altijd op dezelfde manier wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="06a9b-122">We expect that this will make Q# easier to learn and to read because these marks always mean the same thing, and the same concept is always represented the same way.</span></span>

<span data-ttu-id="06a9b-123">Met name:</span><span class="sxs-lookup"><span data-stu-id="06a9b-123">Specifically:</span></span>

- <span data-ttu-id="06a9b-124">De puntkomma, `;`, wordt gebruikt voor het beëindigen van een instructie of een instructie van één regel.</span><span class="sxs-lookup"><span data-stu-id="06a9b-124">The semi-colon, `;`, is used to end a statement or single-line directive.</span></span>
  <span data-ttu-id="06a9b-125">De puntkomma wordt niet gebruikt voor andere doeleinden.</span><span class="sxs-lookup"><span data-stu-id="06a9b-125">It is not used for any other purpose.</span></span>
- <span data-ttu-id="06a9b-126">De komma, `,`, wordt gebruikt om elementen van een reeks van elkaar te scheiden.</span><span class="sxs-lookup"><span data-stu-id="06a9b-126">The comma, `,`, is used to separate elements of a sequence.</span></span> <span data-ttu-id="06a9b-127">De komma wordt gebruikt voor letterlijke waarden van tuples, letterlijke waarden van matrices, lijsten van argumenten, definities van tuples en lijsten van typen.</span><span class="sxs-lookup"><span data-stu-id="06a9b-127">It is used for tuple literals, array literals, argument lists, tuple definitions, and type lists.</span></span> <span data-ttu-id="06a9b-128">**In tegenstelling tot eerdere versies, wordt `;` niet meer ondersteund als scheidingsteken voor letterlijke waarden van matrices.**</span><span class="sxs-lookup"><span data-stu-id="06a9b-128">**In a change from earlier versions, `;` is no longer supported as an array literal separator.**</span></span>
- <span data-ttu-id="06a9b-129">De dubbele punt, `:`, wordt gebruikt voor het introduceren van een type-aantekening.</span><span class="sxs-lookup"><span data-stu-id="06a9b-129">The colon, `:`, is used to introduce a type annotation.</span></span> <span data-ttu-id="06a9b-130">De dubbele punt wordt voornamelijk gebruikt in aanroepbare handtekeningen.</span><span class="sxs-lookup"><span data-stu-id="06a9b-130">It is primarily used in callable signatures.</span></span>
  <span data-ttu-id="06a9b-131">Omdat met een dubbele punt altijd een typehandtekening wordt geïntroduceerd, wordt in de ternaire voorwaardelijke operator die in versie 0.3 is geïntroduceerd, een verticale streep, `|`, gebruikt om de true- en false-waarden van elkaar te scheiden; in Q# wordt dus `cond ? tval | fval` als scheidingsteken gebruikt in plaats van de dubbele punt zoals in C.</span><span class="sxs-lookup"><span data-stu-id="06a9b-131">Because colon always introduces a type signature, the ternary conditional operator introduced in 0.3 uses a vertical bar, `|`, to separate the true and false values; thus, Q# uses `cond ? tval | fval` instead of the colon as separator as in C.</span></span>
  
