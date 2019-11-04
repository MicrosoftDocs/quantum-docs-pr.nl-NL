---
title: De numerieke bibliotheek gebruiken | Microsoft Docs
description: De numerieke bibliotheek gebruiken
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.usage
ms.openlocfilehash: 332781a4356015461426ee7640fd931a41450367
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184607"
---
# <a name="using-the-numerics-library"></a>De numerieke bibliotheek gebruiken

## <a name="overview"></a>Overzicht

De numerieke bibliotheek bestaat uit drie onderdelen

1. **Eenvoudige reken kundige integer** met gehele getallen adders en comparators
1. **Gehele functionaliteit op hoog niveau** die is gebaseerd op de basis functionaliteit; Dit omvat vermenigvuldiging, deling, inversie, enzovoort.  voor ondertekende en niet-ondertekende gehele getallen.
1. **Reken kundige functionaliteit met vaste komma** met vaste-komma initialisatie, optellen, vermenigvuldigen, reciproque, polynoom-evaluatie en meting.

Al deze onderdelen kunnen worden geopend met behulp van een enkele `open`-instructie:
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a>Dergelijke

De numerieke bibliotheek ondersteunt de volgende typen

1. **`LittleEndian`** : een Qubit-matrix `qArr : Qubit[]` die een geheel getal vertegenwoordigt waarbij `qArr[0]` de minst significante bit aangeeft.
1. **`SignedLittleEndian`** : hetzelfde als `LittleEndian`, behalve dat het een geheel getal met teken vertegenwoordigt dat is opgeslagen in twee aanvullingen.
1. **`FixedPoint`** : vertegenwoordigt een reëel getal dat bestaat uit een Qubit-matrix `qArr2 : Qubit[]` en een binaire punt positie `pos`, waarmee het aantal binaire cijfers links van het binaire punt wordt geteld. `qArr2` wordt op dezelfde manier opgeslagen als `SignedLittleEndian`.

## <a name="operations"></a>Operations

Voor elk van de volgende drie typen zijn er verschillende bewerkingen beschikbaar:

1. **`LittleEndian`**
    - Toevoegingen
    - Vergelijking
    - Vermenigvuldigen
    - Squaring
    - Deling (met rest)

1. **`SignedLittleEndian`**
    - Toevoegingen
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

Zie voor meer informatie en gedetailleerde documentatie voor elk van deze bewerkingen de Q # Library Reference docs op [docs.Microsoft.com](https://docs.microsoft.com/en-us/quantum)

## <a name="sample-integer-addition"></a>Voor beeld: geheel getal toevoegen

Als basis voorbeeld moet u rekening houden met de bewerking $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $. Dit is een bewerking die een n-Qubit geheel getal $x $ en een n-of (n + 1)-Qubit registreert $y $ als invoer, waarvan deze is toegewezen aan de som $ (x + y) $. Houd er rekening mee dat de som berekend modulo $2 ^ n $ als $y $ wordt opgeslagen in een $n $-bit-REGI ster.

Met de Quantum Development Kit kan deze bewerking als volgt worden toegepast:
```qsharp
operation MyAdditionTest (xInt : Int, yInt : Int, n : Int) : Unit
{
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        x = LittleEndian(xQubits); // define bit order
        y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xInt, x); // initialize values
        ApplyXorInPlace(yInt, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a>Voor beeld: vloeiende functies evalueren

Als u vloeiende functies, zoals $ \sin (x) $ op een quantum computer, wilt evalueren, waarbij $x $ een Quantum `FixedPoint` getal is, biedt de nummer bibliotheek van de Quantum Development Kit de bewerkingen `EvaluatePolynomialFxP` en `Evaluate[Even/Odd]PolynomialFxP`.

Met de eerste, `EvaluatePolynomialFxP`, kunt u een polynoom van de notatie $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $, waarbij $d $ de *mate*aangeeft. Om dit te doen, zijn alle benodigde `[a_0,..., a_d]` de polynomiale coëfficiënten (van het type `Double[]`), de invoer `x : FixedPoint` en de uitvoer `y : FixedPoint` (aanvankelijk nul):
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], xFxP, yFxP);
```
Het resultaat, $P (x) = 1 + 2x $, wordt opgeslagen in `yFxP`.

De tweede, `EvaluateEvenPolynomialFxP`en de derde, `EvaluateOddPolynomialFxP`, zijn specialisaties voor de gevallen van respectievelijk zelfs en oneven functies. Dat wil zeggen, voor een functie $f (x) $ en $ $ P_ {even} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ is goed geraamd op $P _ {ook} (x) $ of $P _ {oneven} (x): = x\cdot P_ {even} (x) $ respectievelijk.
In Q # kunnen deze twee cases als volgt worden verwerkt:
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], xFxP, yFxP);
```
Hiermee wordt geëvalueerd $P _ {even} (x) = 1 + 2x ^ 2 $, en
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], xFxP, yFxP);
```
Hiermee wordt geëvalueerd $P _ {oneven} (x) = x + 2x ^ 3 $.

## <a name="more-samples"></a>Meer voorbeelden

Meer voor beelden vindt u in de [opslag plaats](https://github.com/Microsoft/Quantum)voor voor beelden.

Als u aan de slag wilt gaan, kloont u de opslag plaats en opent u de `Numerics` submap:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics
```

`cd` vervolgens naar een van de voorbeeld mappen en voer het voor beeld uit via

```bash
dotnet run
```
