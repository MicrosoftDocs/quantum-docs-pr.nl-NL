---
title: Type conversies in de Q# standaard bibliotheken
description: Meer informatie over de algemene en door de gebruiker gedefinieerde type conversie functies in de Q# standaard bibliotheken.
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: aa8a1ad624067906998d2735c7a95174a163ce97
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835601"
---
# <a name="type-conversions"></a>Type conversies #

Q# is een **sterk getypeerde** taal.
Met name Q# wordt niet impliciet gecast tussen verschillende typen. Bijvoorbeeld, `1 + 2.0` is geen geldige Q# expressie.
Biedt in plaats daarvan Q# diverse typen conversie functies voor het samen stellen van nieuwe waarden van een bepaald type.

<xref:microsoft.quantum.core.length>Heeft bijvoorbeeld een uitvoer type van `Int` , dus de uitvoer moet eerst worden geconverteerd naar a `Double` voordat deze kan worden gebruikt als onderdeel van een drijvende-komma expressie.
U kunt dit doen met behulp van de <xref:microsoft.quantum.convert.intasdouble> functie:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

De <xref:microsoft.quantum.convert> naam ruimte biedt algemene type conversie functies voor het werken met ingebouwde basis typen, zoals,, `Int` `Double` `BigInt` , `Result` en `Bool` :

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

De <xref:microsoft.quantum.convert> naam ruimte bevat ook meer exotische-conversies, zoals `FunctionAsOperation` , waarmee functies worden geconverteerd `'T -> 'U` naar nieuwe bewerkingen `'T => 'U` .

Ten slotte Q# biedt de standaard bibliotheek een aantal door de gebruiker gedefinieerde typen, zoals <xref:microsoft.quantum.math.complex> en <xref:microsoft.quantum.arithmetic.littleendian> .
Samen met deze typen biedt de standaard bibliotheek functies zoals <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> :

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
