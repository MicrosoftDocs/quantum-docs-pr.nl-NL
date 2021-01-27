---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: De functie MultiplyGeneratorIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: b53a483a0c2b8c99b733c9c87289fb212b5ffc89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848019"
---
# <a name="multiplygeneratorindex-function"></a>De functie MultiplyGeneratorIndex

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vermenigvuldigt de coëfficiënt in een `GeneratorIndex` .

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Invoer

### <a name="multiplier--double"></a>vermenigvuldiger: [dubbel](xref:microsoft.quantum.lang-ref.double)

De vermenigvuldiger op de coëfficiënt.


### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

De `GeneratorIndex` te vermenigvuldigen.



## <a name="output--generatorindex"></a>Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Een waarde `GeneratorIndex` die een term met een coëfficiënt heeft die groter is dan een `multiplier` grotere factor.

## <a name="example"></a>Voorbeeld

```qsharp
let gen = GeneratorIndex(([1,2,3],[coeff]),[1,2,3]);
let ((idxPaulis, idxDoubles), idxQubits) = MultiplyGeneratorIndex(multiplier, gen);
// idxDoubles[0] == multiplier * coeff;
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)