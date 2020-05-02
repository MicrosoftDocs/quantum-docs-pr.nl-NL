---
title: 'De micro soft Q # Nummerings bibliotheek gebruiken'
description: Meer informatie over de typen en bewerkingen die beschikbaar zijn in de micro soft Quantum Nummerings bibliotheek.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.usage
ms.openlocfilehash: 10d5675e0ef182211a38db4d09347b05afe109c3
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82677115"
---
# <a name="using-the-numerics-library"></a><span data-ttu-id="8b57d-103">De numerieke bibliotheek gebruiken</span><span class="sxs-lookup"><span data-stu-id="8b57d-103">Using the Numerics library</span></span>

## <a name="overview"></a><span data-ttu-id="8b57d-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="8b57d-104">Overview</span></span>

<span data-ttu-id="8b57d-105">De numerieke bibliotheek bestaat uit drie onderdelen</span><span class="sxs-lookup"><span data-stu-id="8b57d-105">The Numerics library consists of three components</span></span>

1. <span data-ttu-id="8b57d-106">**Eenvoudige reken kundige integer** met gehele getallen adders en comparators</span><span class="sxs-lookup"><span data-stu-id="8b57d-106">**Basic integer arithmetic** with integer adders and comparators</span></span>
1. <span data-ttu-id="8b57d-107">**Gehele functionaliteit op hoog niveau** die is gebaseerd op de basis functionaliteit; Dit omvat vermenigvuldiging, deling, inversie, enzovoort.  voor ondertekende en niet-ondertekende gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="8b57d-107">**High-level integer functionality** that is built on top of the basic  functionality; it includes multiplication, division, inversion, etc.  for signed and unsigned integers.</span></span>
1. <span data-ttu-id="8b57d-108">**Reken kundige functionaliteit met vaste komma** met vaste-komma initialisatie, optellen, vermenigvuldigen, reciproque, polynoom-evaluatie en meting.</span><span class="sxs-lookup"><span data-stu-id="8b57d-108">**Fixed-point arithmetic functionality** with fixed-point initialization,  addition, multiplication, reciprocal, polynomial evaluation, and measurement.</span></span>

<span data-ttu-id="8b57d-109">Al deze onderdelen kunnen worden geopend met één `open` instructie:</span><span class="sxs-lookup"><span data-stu-id="8b57d-109">All of these components can be accessed using a single `open` statement:</span></span>
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a><span data-ttu-id="8b57d-110">Typen</span><span class="sxs-lookup"><span data-stu-id="8b57d-110">Types</span></span>

<span data-ttu-id="8b57d-111">De numerieke bibliotheek ondersteunt de volgende typen</span><span class="sxs-lookup"><span data-stu-id="8b57d-111">The numerics library supports the following types</span></span>

1. <span data-ttu-id="8b57d-112">**`LittleEndian`**: Een Qubit- `qArr : Qubit[]` matrix die een geheel getal `qArr[0]` vertegenwoordigt waarbij de minst significante bit wordt aangeduid.</span><span class="sxs-lookup"><span data-stu-id="8b57d-112">**`LittleEndian`**: A qubit array `qArr : Qubit[]` that represents an integer where `qArr[0]` denotes the least significant bit.</span></span>
1. <span data-ttu-id="8b57d-113">**`SignedLittleEndian`**: Zelfde als `LittleEndian` , behalve dat dit staat voor een geheel getal met teken dat is opgeslagen in twee aanvullingen.</span><span class="sxs-lookup"><span data-stu-id="8b57d-113">**`SignedLittleEndian`**: Same as `LittleEndian` except that it represents a signed integer stored in two's complement.</span></span>
1. <span data-ttu-id="8b57d-114">**`FixedPoint`**: Dit is een reëel getal dat bestaat uit een Qubit `qArr2 : Qubit[]` -matrix en een binaire `pos`punt positie, waarmee het aantal binaire cijfers links van het binaire punt wordt geteld.</span><span class="sxs-lookup"><span data-stu-id="8b57d-114">**`FixedPoint`**: Represents a real number consisting of a qubit array `qArr2 : Qubit[]` and a binary point position `pos`, which counts the number of binary digits to the left of the binary point.</span></span> <span data-ttu-id="8b57d-115">`qArr2`wordt op dezelfde manier opgeslagen als `SignedLittleEndian`.</span><span class="sxs-lookup"><span data-stu-id="8b57d-115">`qArr2` is stored in the same way as `SignedLittleEndian`.</span></span>

## <a name="operations"></a><span data-ttu-id="8b57d-116">Bewerkingen</span><span class="sxs-lookup"><span data-stu-id="8b57d-116">Operations</span></span>

<span data-ttu-id="8b57d-117">Voor elk van de volgende drie typen zijn er verschillende bewerkingen beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="8b57d-117">For each of the three types above, a variety of operations is available:</span></span>

1. **`LittleEndian`**
    - <span data-ttu-id="8b57d-118">Optelling</span><span class="sxs-lookup"><span data-stu-id="8b57d-118">Addition</span></span>
    - <span data-ttu-id="8b57d-119">Vergelijking</span><span class="sxs-lookup"><span data-stu-id="8b57d-119">Comparison</span></span>
    - <span data-ttu-id="8b57d-120">Vermenigvuldiging</span><span class="sxs-lookup"><span data-stu-id="8b57d-120">Multiplication</span></span>
    - <span data-ttu-id="8b57d-121">Squaring</span><span class="sxs-lookup"><span data-stu-id="8b57d-121">Squaring</span></span>
    - <span data-ttu-id="8b57d-122">Deling (met rest)</span><span class="sxs-lookup"><span data-stu-id="8b57d-122">Division (with remainder)</span></span>

1. **`SignedLittleEndian`**
    - <span data-ttu-id="8b57d-123">Optelling</span><span class="sxs-lookup"><span data-stu-id="8b57d-123">Addition</span></span>
    - <span data-ttu-id="8b57d-124">Vergelijking</span><span class="sxs-lookup"><span data-stu-id="8b57d-124">Comparison</span></span>
    - <span data-ttu-id="8b57d-125">Aanvulling van inversie modulo 2</span><span class="sxs-lookup"><span data-stu-id="8b57d-125">Inversion modulo 2's complement</span></span>
    - <span data-ttu-id="8b57d-126">Vermenigvuldiging</span><span class="sxs-lookup"><span data-stu-id="8b57d-126">Multiplication</span></span>
    - <span data-ttu-id="8b57d-127">Squaring</span><span class="sxs-lookup"><span data-stu-id="8b57d-127">Squaring</span></span>

1. **`FixedPoint`**
    - <span data-ttu-id="8b57d-128">Voor bereiding/initialisatie naar een klassieke waarde</span><span class="sxs-lookup"><span data-stu-id="8b57d-128">Preparation / initialization to a classical values</span></span>
    - <span data-ttu-id="8b57d-129">Toevoeging (klassieke constante of andere Quantum vaste komma)</span><span class="sxs-lookup"><span data-stu-id="8b57d-129">Addition (classical constant or other quantum fixed-point)</span></span>
    - <span data-ttu-id="8b57d-130">Vergelijking</span><span class="sxs-lookup"><span data-stu-id="8b57d-130">Comparison</span></span>
    - <span data-ttu-id="8b57d-131">Vermenigvuldiging</span><span class="sxs-lookup"><span data-stu-id="8b57d-131">Multiplication</span></span>
    - <span data-ttu-id="8b57d-132">Squaring</span><span class="sxs-lookup"><span data-stu-id="8b57d-132">Squaring</span></span>
    - <span data-ttu-id="8b57d-133">Polynoom-evaluatie met specialisatie voor even en oneven functies</span><span class="sxs-lookup"><span data-stu-id="8b57d-133">Polynomial evaluation with specialization for even and odd functions</span></span>
    - <span data-ttu-id="8b57d-134">Reciproque (1/x)</span><span class="sxs-lookup"><span data-stu-id="8b57d-134">Reciprocal (1/x)</span></span>
    - <span data-ttu-id="8b57d-135">Meting (klassiek dubbel)</span><span class="sxs-lookup"><span data-stu-id="8b57d-135">Measurement (classical Double)</span></span>

<span data-ttu-id="8b57d-136">Zie voor meer informatie en gedetailleerde documentatie voor elk van deze bewerkingen de Q # Library Reference docs op [docs.Microsoft.com](https://docs.microsoft.com/quantum)</span><span class="sxs-lookup"><span data-stu-id="8b57d-136">For more information and detailed documentation for each of these operations, see the Q# library reference docs at [docs.microsoft.com](https://docs.microsoft.com/quantum)</span></span>

## <a name="sample-integer-addition"></a><span data-ttu-id="8b57d-137">Voor beeld: geheel getal toevoegen</span><span class="sxs-lookup"><span data-stu-id="8b57d-137">Sample: Integer addition</span></span>

<span data-ttu-id="8b57d-138">Als basis voorbeeld moet u rekening houden met de bewerking $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $. Dit is een bewerking die een n-Qubit geheel getal $x $ en een n-of (n + 1)-Qubit registreert $y $ als invoer, waarvan deze is toegewezen aan de som $ (x + y) $.</span><span class="sxs-lookup"><span data-stu-id="8b57d-138">As a basic example, consider the operation $$ \ket x\ket y\mapsto \ket x\ket{x+y} $$ that is, an operation that takes an n-qubit integer $x$ and an n- or (n+1)-qubit register $y$ as input, the latter of which it maps to the sum $(x+y)$.</span></span> <span data-ttu-id="8b57d-139">Houd er rekening mee dat de som berekend modulo $2 ^ n $ als $y $ wordt opgeslagen in een $n $-bit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="8b57d-139">Note that the sum is computed modulo $2^n$ if $y$ is stored in an $n$-bit register.</span></span>

<span data-ttu-id="8b57d-140">Met de Quantum Development Kit kan deze bewerking als volgt worden toegepast:</span><span class="sxs-lookup"><span data-stu-id="8b57d-140">Using the Quantum Development Kit, this operation can be applied as follows:</span></span>
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

## <a name="sample-evaluating-smooth-functions"></a><span data-ttu-id="8b57d-141">Voor beeld: vloeiende functies evalueren</span><span class="sxs-lookup"><span data-stu-id="8b57d-141">Sample: Evaluating smooth functions</span></span>

<span data-ttu-id="8b57d-142">Voor het evalueren van vloeiende functies, zoals $ \sin (x) $ op een quantum computer, waarbij $x $ `FixedPoint` een Quantum nummer is, levert de nummer bibliotheek van de Quantum `EvaluatePolynomialFxP` Development `Evaluate[Even/Odd]PolynomialFxP`Kit de bewerkingen en.</span><span class="sxs-lookup"><span data-stu-id="8b57d-142">To evaluate smooth functions such as $\sin(x)$ on a quantum computer, where $x$ is a quantum `FixedPoint` number, the Quantum Development Kit numerics library provides the operations `EvaluatePolynomialFxP` and `Evaluate[Even/Odd]PolynomialFxP`.</span></span>

<span data-ttu-id="8b57d-143">De eerste, `EvaluatePolynomialFxP`, geeft u de mogelijkheid om een polynoom van het formulier $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $ te evalueren waarbij $d $ de *graad*aangeeft.</span><span class="sxs-lookup"><span data-stu-id="8b57d-143">The first, `EvaluatePolynomialFxP`, allows to evaluate a polynomial of the form $$ P(x) = a_0 + a_1x + a_2x^2 + \cdots + a_dx^d, $$ where $d$ denotes the *degree*.</span></span> <span data-ttu-id="8b57d-144">Hiervoor moeten alle benodigde `[a_0,..., a_d]` geoefficienties (van het type `Double[]`), de invoer `x : FixedPoint` en de uitvoer `y : FixedPoint` (aanvankelijk nul) zijn:</span><span class="sxs-lookup"><span data-stu-id="8b57d-144">To do so, all that is needed are the polynomial coefficients `[a_0,..., a_d]` (of type `Double[]`), the input `x : FixedPoint` and the output `y : FixedPoint` (initially zero):</span></span>
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="8b57d-145">Het resultaat, $P (x) = 1 + 2x $, wordt opgeslagen in `yFxP`.</span><span class="sxs-lookup"><span data-stu-id="8b57d-145">The result, $P(x)=1+2x$, will be stored in `yFxP`.</span></span>

<span data-ttu-id="8b57d-146">De tweede, `EvaluateEvenPolynomialFxP`, en de derde, `EvaluateOddPolynomialFxP`zijn specialisaties voor de gevallen van respectievelijk zelfs en oneven functies.</span><span class="sxs-lookup"><span data-stu-id="8b57d-146">The second, `EvaluateEvenPolynomialFxP`, and the third, `EvaluateOddPolynomialFxP`, are specializations for the cases of even and odd functions, respectively.</span></span> <span data-ttu-id="8b57d-147">Dat wil zeggen dat voor een even/oneven-functie $f (x) $ en $ $ P_ {ook} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ is goed geraamd op $P _ {ook} (x) $ of $P _ {oneven} (x): = x\cdot {even} (x) $. P_</span><span class="sxs-lookup"><span data-stu-id="8b57d-147">That is, for an even/odd function $f(x)$ and $$ P_{even}(x)=a_0 + a_1 x^2 + a_2 x^4 + \cdots + a_d x^{2d}, $$ $f(x)$ is approximated well by $P_{even}(x)$ or $P_{odd}(x) := x\cdot P_{even}(x)$, respectively.</span></span>
<span data-ttu-id="8b57d-148">In Q # kunnen deze twee cases als volgt worden verwerkt:</span><span class="sxs-lookup"><span data-stu-id="8b57d-148">In Q#, these two cases can be handled as follows:</span></span>
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="8b57d-149">Hiermee wordt geëvalueerd $P _ {even} (x) = 1 + 2x ^ 2 $, en</span><span class="sxs-lookup"><span data-stu-id="8b57d-149">which evaluates $P_{even}(x) = 1 + 2x^2$, and</span></span>
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="8b57d-150">Hiermee wordt geëvalueerd $P _ {oneven} (x) = x + 2x ^ 3 $.</span><span class="sxs-lookup"><span data-stu-id="8b57d-150">which evaluates $P_{odd}(x) = x + 2x^3$.</span></span>

## <a name="more-samples"></a><span data-ttu-id="8b57d-151">Meer voorbeelden</span><span class="sxs-lookup"><span data-stu-id="8b57d-151">More samples</span></span>

<span data-ttu-id="8b57d-152">Meer voor beelden vindt u in de [opslag plaats](https://github.com/Microsoft/Quantum)voor voor beelden.</span><span class="sxs-lookup"><span data-stu-id="8b57d-152">You can find more samples in the [main samples repository](https://github.com/Microsoft/Quantum).</span></span>

<span data-ttu-id="8b57d-153">Als u aan de slag wilt gaan, kloont `Numerics` u de opslag plaats en opent u de submap:</span><span class="sxs-lookup"><span data-stu-id="8b57d-153">To get started, clone the repo and open the `Numerics` subfolder:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics
```

<span data-ttu-id="8b57d-154">Ga vervolgens `cd` naar een van de voorbeeld mappen en voer het voor beeld uit via</span><span class="sxs-lookup"><span data-stu-id="8b57d-154">Then, `cd` into one of the sample folders and run the sample via</span></span>

```bash
dotnet run
```
