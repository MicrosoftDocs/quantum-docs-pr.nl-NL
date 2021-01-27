---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: De functie SizeAdjustedTruthTable
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 8d69aa119c25a0f64743fec36c00ecdef2450c44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855325"
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