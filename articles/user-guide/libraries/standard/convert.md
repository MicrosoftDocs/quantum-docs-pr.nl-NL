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
ms.openlocfilehash: 9ec3a2ecd2aa59a10a7033e7b3067eb147ce4035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691110"
---
# <a name="type-conversions"></a>Type conversies #

Q# is een **sterk getypeerde** taal.
Met name Q# wordt niet impliciet gecast tussen verschillende typen. Bijvoorbeeld, `1 + 2.0` is geen geldige Q# expressie.
Biedt in plaats daarvan Q# diverse typen conversie functies voor het samen stellen van nieuwe waarden van een bepaald type.

<xref:Microsoft.Quantum.Core.Length>Heeft bijvoorbeeld een uitvoer type van `Int` , dus de uitvoer moet eerst worden geconverteerd naar a `Double` voordat deze kan worden gebruikt als onderdeel van een drijvende-komma expressie.
U kunt dit doen met behulp van de <xref:Microsoft.Quantum.Convert.IntAsDouble> functie:

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

De <xref:Microsoft.Quantum.Convert> naam ruimte biedt algemene type conversie functies voor het werken met ingebouwde basis typen, zoals,, `Int` `Double` `BigInt` , `Result` en `Bool` :

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

De <xref:Microsoft.Quantum.Convert> naam ruimte bevat ook meer exotische-conversies, zoals `FunctionAsOperation` , waarmee functies worden geconverteerd `'T -> 'U` naar nieuwe bewerkingen `'T => 'U` .

Ten slotte Q# biedt de standaard bibliotheek een aantal door de gebruiker gedefinieerde typen, zoals <xref:Microsoft.Quantum.Math.Complex> en <xref:Microsoft.Quantum.Arithmetic.LittleEndian> .
Samen met deze typen biedt de standaard bibliotheek functies zoals <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> :

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
