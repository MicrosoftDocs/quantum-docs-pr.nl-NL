---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: De functie DecomposedOn
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855516"
---
# <a name="decomposedon-function"></a>De functie DecomposedOn

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ontleedt een permutatie op een variabele

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Beschrijving

Met een permutatie $ \pi $ ( `perm` ) en een index $i $ ( `index` ), deze methode retourneert drie permutaties $ ((\ pi_l, \ pi_r), \pi ') $ zo dat de installatie kopieën van $ \ pi_l $ en $ \ pi_r $ geen bits in hun eigen elementen wijzigen op andere indexen dan $i $ en installatie kopieën van $ \pi $ in hun eigen elementen.

## <a name="input"></a>Invoer

### <a name="perm--int"></a>macht: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>index: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])



## <a name="example"></a>Voorbeeld

Stel dat de invoer de volgende macht heeft: [0, 2, 3, 5, 7, 1, 4, 6] en index = 0. deze functie berekent drie permutaties op basis van de onderstaande tabel, waarin de permutatie `perm` in binaire notatie met elementen in groep A en afbeeldingen in groep D wordt weer gegeven.  De kolommen bevatten een lijst met de bits indexen.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 |       |       | 0 0 0 | 0
| 0 0 1 |       |       | 0 1 0 | 2
| 0 1 0 |       |       | 0 1 1 | 3
| 0 1 1 |       |       | 1 0 1 | 5
| 1 0 0 |       |       | 1 1 1 | 7
| 1 0 1 |       |       | 0 0 1 | 1
| 1 1 0 |       |       | 1 0 0 | 4
| 1 1 1 |       |       | 1 1 0 | 6

Alle waarden voor indices die niet gelijk zijn aan 0 (= index) worden gekopieerd van A naar B en van D naar C.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0   | 0 0   | 0 0 0 |
| 0 0 1 | 0 0   | 0 1   | 0 1 0 |
| 0 1 0 | 0 1   | 0 1   | 0 1 1 |
| 0 1 1 | 0 1   | 1 0   | 1 0 1 |
| 1 0 0 | 1 0   | 1 1   | 1 1 1 |
| 1 0 1 | 1 0   | 0 0   | 0 0 1 |
| 1 1 0 | 1 1   | 1 0   | 1 0 0 |
| 1 1 1 | 1 1   | 1 1   | 1 1 0 |

Vervolgens wordt 0 geplaatst voor het eerste element met een lege index op kolom 0 in blok B en wordt er een 1 in B geplaatst waarbij het voor voegsel overeenkomt (in het eerste geval de andere rij met indices 0 0).
Daarna wordt er een 1 toegevoegd aan dezelfde rij in blok C en vervolgens een 0 voor het bijbehorende voor voegsel in blok C.  Dit proces wordt herhaald totdat alle indices in kolom 0 in de blokken B en C zijn geplaatst.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0 0 | 0 0 0 | 0 0 0 |
| 0 0 1 | 0 0 1 | 0 1 1 | 0 1 0 |
| 0 1 0 | 0 1 0 | 0 1 0 | 0 1 1 |
| 0 1 1 | 0 1 1 | 1 0 1 | 1 0 1 |
| 1 0 0 | 1 0 0 | 1 1 0 | 1 1 1 |
| 1 0 1 | 1 0 1 | 0 0 1 | 0 0 1 |
| 1 1 0 | 1 1 0 | 1 0 0 | 1 0 0 |
| 1 1 1 | 1 1 1 | 1 1 1 | 1 1 0 |

We kunnen drie nieuwe permutaties uit de tabel lezen:

- $ \ pi_l $ met elementen in A, afbeeldingen in B (links)
- $ \ pi_r $ met elementen in D, afbeeldingen in C (rechts)
- $ \pi $ met elementen in B, afbeeldingen in C (rest)

Houd er rekening mee dat door de ontwerp-bits waarden niet worden gewijzigd in $ \ pi_l $ en $ \ pi_r $ voor indices 1 en 2, en dat bits-waarden niet worden gewijzigd voor in $ \ pi_ $ voor index 0.  Houd er ook rekening mee dat $ \ pi_l $ en $ \ pi_r $ zelf inverse moet zijn.

De afgeleide en geretourneerde permutaties zijn: Left = [0, 1, 2, 3, 4, 5, 6, 7] rechts = [0, 1, 3, 2, 4, 5, 7, 6] restant = [0, 3, 2, 5, 6, 1, 4, 7]