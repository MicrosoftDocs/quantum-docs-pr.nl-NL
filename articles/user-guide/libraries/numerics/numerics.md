---
title: De micro soft Q# Nummerings bibliotheek gebruiken
description: Meer informatie over de typen en bewerkingen die beschikbaar zijn in de micro soft Quantum Nummerings bibliotheek.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: conceptual
uid: microsoft.quantum.numerics.usage
no-loc:
- Q#
- $$v
ms.openlocfilehash: 92efd3b8677d2f27bc59f986ce6c9e915cd23652
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856448"
---
# <a name="using-the-numerics-library"></a>De numerieke bibliotheek gebruiken

## <a name="overview"></a>Overzicht

De numerieke bibliotheek bestaat uit drie onderdelen

1. **Eenvoudige reken kundige integer** met gehele getallen adders en comparators
1. **Gehele functionaliteit op hoog niveau** die is gebaseerd op de basis functionaliteit; Dit omvat vermenigvuldiging, deling, inversie, enzovoort.  voor ondertekende en niet-ondertekende gehele getallen.
1. **Reken kundige functionaliteit met vaste komma** met vaste-komma initialisatie, optellen, vermenigvuldigen, reciproque, polynoom-evaluatie en meting.

Al deze onderdelen kunnen worden geopend met één `open` instructie:
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a>Typen

De numerieke bibliotheek ondersteunt de volgende typen

1. **`LittleEndian`**: Een Qubit-matrix `qArr : Qubit[]` die een geheel getal vertegenwoordigt waarbij `qArr[0]` de minst significante bit wordt aangeduid.
1. **`SignedLittleEndian`**: Zelfde als `LittleEndian` , behalve dat dit staat voor een geheel getal met teken dat is opgeslagen in twee aanvullingen.
1. **`FixedPoint`**: Dit is een reëel getal dat bestaat uit een Qubit `qArr2 : Qubit[]` -matrix en een binaire punt positie `pos` , waarmee het aantal binaire cijfers links van het binaire punt wordt geteld. `qArr2` wordt op dezelfde manier opgeslagen als `SignedLittleEndian` .

## <a name="operations"></a>Operations

Voor elk van de volgende drie typen zijn er verschillende bewerkingen beschikbaar:

1. **`LittleEndian`**
    - Optellen
    - Vergelijking
    - Vermenigvuldigen
    - Squaring
    - Deling (met rest)

1. **`SignedLittleEndian`**
    - Optellen
    - Vergelijking
    - Aanvulling van inversie modulo 2
    - Vermenigvuldigen
    - Squaring

1. **`FixedPoint`**
    - Voor bereiding/initialisatie naar een klassieke waarde
    - Toevoeging (klassieke constante of andere Quantum vaste komma)
    - Vergelijking
    - Vermenigvuldigen
    - Squaring
    - Polynoom-evaluatie met specialisatie voor even en oneven functies
    - Reciproque (1/x)
    - Meting (klassiek dubbel)

Zie Q# naslag documenten voor bibliotheken op [docs.Microsoft.com](https://docs.microsoft.com/quantum) voor meer informatie en gedetailleerde documentatie voor elk van deze bewerkingen.

## <a name="sample-integer-addition"></a>Voor beeld: geheel getal toevoegen

Als basis voorbeeld moet u rekening houden met de bewerking $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $. Dit is een bewerking die een n-Qubit geheel getal $x $ en een n-of (n + 1)-Qubit registreert $y $ als invoer, waarvan deze is toegewezen aan de som $ (x + y) $. Houd er rekening mee dat de som berekend modulo $2 ^ n $ als $y $ wordt opgeslagen in een $n $-bit-REGI ster.

Met de Quantum Development Kit kan deze bewerking als volgt worden toegepast:
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a>Voor beeld: vloeiende functies evalueren

Voor het evalueren van vloeiende functies, zoals $ \sin (x) $ op een quantum computer, waarbij $x $ een Quantum `FixedPoint` nummer is, levert de nummer bibliotheek van de Quantum Development Kit de bewerkingen `EvaluatePolynomialFxP` en `Evaluate[Even/Odd]PolynomialFxP` .

De eerste, `EvaluatePolynomialFxP` , geeft u de mogelijkheid om een polynoom van het formulier $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $ te evalueren waarbij $d $ de *graad* aangeeft. Hiervoor moeten alle benodigde geoefficienties `[a_0,..., a_d]` (van het type `Double[]` ), de invoer `x : FixedPoint` en de uitvoer `y : FixedPoint` (aanvankelijk nul) zijn:
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
Het resultaat, $P (x) = 1 + 2x $, wordt opgeslagen in `yFxP` .

De tweede, `EvaluateEvenPolynomialFxP` , en de derde, `EvaluateOddPolynomialFxP` zijn specialisaties voor de gevallen van respectievelijk zelfs en oneven functies. Dat wil zeggen dat voor een even/oneven-functie $f (x) $ en $ $ P_ {ook} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ is goed geraamd op $P _ {ook} (x) $ of $P _ {oneven} (x): = x\cdot {even} (x) $. P_
In Q# kunnen deze twee gevallen als volgt worden verwerkt:
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
Hiermee wordt geëvalueerd $P _ {even} (x) = 1 + 2x ^ 2 $, en
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
Hiermee wordt geëvalueerd $P _ {oneven} (x) = x + 2x ^ 3 $.

## <a name="more-samples"></a>Meer voorbeelden

Meer voor beelden vindt u in de [opslag plaats](https://github.com/Microsoft/Quantum)voor voor beelden.

Als u aan de slag wilt gaan, kloont u de opslag plaats en opent u de `Numerics` submap:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics
```

Ga vervolgens `cd` naar een van de voorbeeld mappen en voer het voor beeld uit via

```bash
dotnet run
```
