---
title: 'Q # standaard-bibliotheken-type conversies | Microsoft Docs'
description: 'Q # standaard bibliotheken-type conversies'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 4716f0d9562229f08ef6f0f5f80961f793de4c5c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184471"
---
# <a name="type-conversions"></a>Type conversies #

Q # is een **sterk getypeerde** taal.
Met name Q # wordt niet impliciet gecast tussen verschillende typen. `1 + 2.0` is bijvoorbeeld geen geldige Q #-expressie.
In plaats daarvan biedt Q # diverse typen conversie functies voor het samen stellen van nieuwe waarden van een bepaald type.

<xref:microsoft.quantum.core.length> heeft bijvoorbeeld een uitvoer type van `Int`, dus de uitvoer moet eerst worden geconverteerd naar een `Double` voordat deze kan worden gebruikt als onderdeel van een drijvende-komma expressie.
U kunt dit doen met behulp van de functie <xref:microsoft.quantum.convert.intasdouble>:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

De <xref:microsoft.quantum.convert> naam ruimte biedt algemene type conversie functies voor het werken met ingebouwde basis typen, zoals `Int`, `Double`, `BigInt`, `Result`en `Bool`:

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

De <xref:microsoft.quantum.convert>-naam ruimte bevat ook meer exotische conversies, zoals `FunctionAsOperation`, waarmee functies `'T -> 'U` worden geconverteerd naar nieuwe bewerkingen `'T => 'U`.

Ten slotte biedt de Q #-standaard bibliotheek een aantal door de gebruiker gedefinieerde typen, zoals <xref:microsoft.quantum.math.complex> en <xref:microsoft.quantum.arithmetic.littleendian>.
Samen met deze typen biedt de standaard bibliotheek functies als <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
