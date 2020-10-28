---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Bewerking ApplyPermutationUsingDecompositionWithVariableOrder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709205"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>Bewerking ApplyPermutationUsingDecompositionWithVariableOrder

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket [](https://nuget.org/packages/)


Permutaties de amplitudes in een Quantum status op basis van een permutatie met behulp van op ontleding gebaseerde synthese.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Beschrijving

Deze bewerking is een meer algemene versie van waarin @"microsoft.quantum.synthesis.applypermutationusingdecomposition" de variabele volgorde kan worden opgegeven. Een andere variabele order wijzigt de ontledings reeks en de waarheids tabellen die worden gebruikt voor de bewaakte @"microsoft.quantum.intrinsic.x" poorten.  Daarom wijzigt de volg orde van de variabele het aantal gebruikte poorten om de permutatie te realiseren.

## <a name="input"></a>Invoer

### <a name="perm--int"></a>macht: [int](xref:microsoft.quantum.lang-ref.int)[]

Een permutatie van $2 ^ n $ elementen vanaf 0.


### <a name="variableorder--int"></a>variableOrder: [int](xref:microsoft.quantum.lang-ref.int)[]

Een permutatie van $n $ Elements vanaf 0.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een lijst met $n $ qubits waarop de permutatie wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. synthese. ApplyPermutationUsingDecomposition](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [Micro soft. Quantum. synthese. ApplyPermutationUsingTransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)