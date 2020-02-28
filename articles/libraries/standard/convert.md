---
title: 'Type conversies in de Q # standaard-bibliotheken'
description: 'Meer informatie over de algemene en door de gebruiker gedefinieerde type conversie functies in de standaard bibliotheken van Q #.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: e941d7e3d76459546861410e91a03d7315183867
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907797"
---
# <a name="type-conversions"></a><span data-ttu-id="2dda3-103">Type conversies</span><span class="sxs-lookup"><span data-stu-id="2dda3-103">Type Conversions</span></span> #

<span data-ttu-id="2dda3-104">Q # is een **sterk getypeerde** taal.</span><span class="sxs-lookup"><span data-stu-id="2dda3-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="2dda3-105">Met name Q # wordt niet impliciet gecast tussen verschillende typen.</span><span class="sxs-lookup"><span data-stu-id="2dda3-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="2dda3-106">`1 + 2.0` is bijvoorbeeld geen geldige Q #-expressie.</span><span class="sxs-lookup"><span data-stu-id="2dda3-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="2dda3-107">In plaats daarvan biedt Q # diverse typen conversie functies voor het samen stellen van nieuwe waarden van een bepaald type.</span><span class="sxs-lookup"><span data-stu-id="2dda3-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="2dda3-108"><xref:microsoft.quantum.core.length> heeft bijvoorbeeld een uitvoer type van `Int`, dus de uitvoer moet eerst worden geconverteerd naar een `Double` voordat deze kan worden gebruikt als onderdeel van een drijvende-komma expressie.</span><span class="sxs-lookup"><span data-stu-id="2dda3-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="2dda3-109">U kunt dit doen met behulp van de functie <xref:microsoft.quantum.convert.intasdouble>:</span><span class="sxs-lookup"><span data-stu-id="2dda3-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="2dda3-110">De <xref:microsoft.quantum.convert> naam ruimte biedt algemene type conversie functies voor het werken met ingebouwde basis typen, zoals `Int`, `Double`, `BigInt`, `Result`en `Bool`:</span><span class="sxs-lookup"><span data-stu-id="2dda3-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="2dda3-111">De <xref:microsoft.quantum.convert>-naam ruimte bevat ook meer exotische conversies, zoals `FunctionAsOperation`, waarmee functies `'T -> 'U` worden geconverteerd naar nieuwe bewerkingen `'T => 'U`.</span><span class="sxs-lookup"><span data-stu-id="2dda3-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="2dda3-112">Ten slotte biedt de Q #-standaard bibliotheek een aantal door de gebruiker gedefinieerde typen, zoals <xref:microsoft.quantum.math.complex> en <xref:microsoft.quantum.arithmetic.littleendian>.</span><span class="sxs-lookup"><span data-stu-id="2dda3-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="2dda3-113">Samen met deze typen biedt de standaard bibliotheek functies als <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span><span class="sxs-lookup"><span data-stu-id="2dda3-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
