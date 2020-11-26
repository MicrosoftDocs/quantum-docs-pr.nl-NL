---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: De functie SizeAdjustedTruthTable
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202920"
---
# <a name="sizeadjustedtruthtable-function"></a>De functie SizeAdjustedTruthTable

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de waarheids tabel van een matrix met Booleaanse waarden aangepast op basis van het aantal variabelen

Een nieuwe matrix wordt geretourneerd met een lengte `2^numVars` , waardoor de grootte kan worden uitgebreid `table` met `false` vermeldingen of worden afgekapt op `2^numVars` elementen.

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a>Invoer

### <a name="table--bool"></a>tabel: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Waarheids tabel als een matrix met waarheids waarden


### <a name="numvars--int"></a>numVars: [int](xref:microsoft.quantum.lang-ref.int)

Aantal variabelen



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Tabel met gecorrigeerde grootte