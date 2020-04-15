---
title: De programmeertaal Q#
description: Inleiding tot de Q#-taal voor het ontwikkelen van kwantumprogramma's.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: b62e6866fc3609d95c26a5eab2a6eac325dfe330
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907372"
---
# <a name="the-q-programming-language"></a>De programmeertaal Q#

## <a name="introduction"></a>Inleiding

Een natuurlijk model voor kwantumberekening is de kwantumcomputer te behandelen als een coprocessor, vergelijkbaar met coprocessoren voor GPU's, FPGA's en andere adjunct-processoren.
De primaire besturingslogica voert klassieke code uit op een klassieke hostcomputer.
Zo nodig kan het hostprogramma een subroutine aanroepen die wordt uitgevoerd op de adjunct-processor.
Wanneer de subroutine is voltooid, krijgt het hostprogramma toegang tot de resultaten van de subroutine.

Q# (Q-sharp) is een domein-specifieke programmeertaal die wordt gebruikt voor het uitdrukken van kwantumalgoritmen.
Q# kan worden gebruikt voor het schrijven van subroutines die worden uitgevoerd op een adjunct-kwantumprocessor, onder controle van een klassiek hostprogramma en een klassieke computer.
Totdat kwantumprocessoren algemeen beschikbaar zijn, worden Q#-subroutines uitgevoerd op een simulator.

Q# bevat een kleine set primitieve typen, samen met twee manieren (matrices en tuples) voor het maken van nieuwe, gestructureerde typen.
Het ondersteunt een basisproceduremodel voor het schrijven van programma's, met lussen en if/then-instructies.
Constructs van het hoogste niveau in Q# zijn door de gebruiker gedefinieerde typen, bewerkingen en functies.

In de volgende secties vindt u gedetailleerde informatie over het volgende:
- [Het typemodel](xref:microsoft.quantum.language.type-model)
- [Expressies](xref:microsoft.quantum.language.expressions)
- [Instructies](xref:microsoft.quantum.language.statements)
- [Bestandsstructuur](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a>Conventies

We streven naar een consistent gebruik van gangbare interpunctietekens in alle situaties.
Hierdoor is Q# makkelijker te leren en te lezen omdat deze tekens altijd hetzelfde betekenen, en hetzelfde begrip altijd op dezelfde manier wordt weergegeven.

Met name:

- De puntkomma, `;`, wordt gebruikt voor het beëindigen van een instructie of een instructie van één regel.
  De puntkomma wordt niet gebruikt voor andere doeleinden.
- De komma, `,`, wordt gebruikt om elementen van een reeks van elkaar te scheiden. De komma wordt gebruikt voor letterlijke waarden van tuples, letterlijke waarden van matrices, lijsten van argumenten, definities van tuples en lijsten van typen. **In tegenstelling tot eerdere versies, wordt `;` niet meer ondersteund als scheidingsteken voor letterlijke waarden van matrices.**
- De dubbele punt, `:`, wordt gebruikt voor het introduceren van een type-aantekening. De dubbele punt wordt voornamelijk gebruikt in aanroepbare handtekeningen.
  Omdat met een dubbele punt altijd een typehandtekening wordt geïntroduceerd, wordt in de ternaire voorwaardelijke operator die in versie 0.3 is geïntroduceerd, een verticale streep, `|`, gebruikt om de true- en false-waarden van elkaar te scheiden; in Q# wordt dus `cond ? tval | fval` als scheidingsteken gebruikt in plaats van de dubbele punt zoals in C.
  
