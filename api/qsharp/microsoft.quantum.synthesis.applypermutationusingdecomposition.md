---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Bewerking ApplyPermutationUsingDecomposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 40b51807da155c57c3fa8d740eff28ceef0a0ffc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709216"
---
# <a name="applypermutationusingdecomposition-operation"></a>Bewerking ApplyPermutationUsingDecomposition

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket [](https://nuget.org/packages/)


Permutaties de amplitudes in een Quantum status op basis van een permutatie met behulp van op ontleding gebaseerde synthese.

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Beschrijving

Met deze procedure wordt de methode voor het samen stellen op basis van een synthese geïmplementeerd.  De invoer is een permutatie $ \pi $ boven $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, waarmee een $n variabele van $-variable omkeerbaar Booleaanse waarde wordt aangeduid.
Het algoritme voert iteraties de volgende stappen uit voor elke variabele index $i $:

1. Compute $ ((\ pi_l, \ pi_r), \pi ') $ zo is dat de installatie kopieën van $ \ pi_l $ en $ \ pi_r $ geen bits in hun eigen elementen wijzigen op andere indexen dan $i $ en installatie kopieën van $ \pi $ in hun eigen elementen.
2. Stel $ \pi \leftarrow \pi $ in en pas waarheids tabellen af van $ \ pi_l $ en $ \ pi_r $ op basis van elementen die geen vaste punten zijn.

Nadat u deze stappen voor alle variabelen indexen hebt toegepast, is de resterende permutatie $ \pi $ de identiteit en op basis van de verzamelde waarheids tabellen en-indexen, een @"microsoft.quantum.intrinsic.x" met behulp van de @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" bewerking.

De variabele bestelling is $0, \dots, n-$1.  U kunt een aangepaste variabele volgorde opgeven in de bewerking @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .

## <a name="input"></a>Invoer

### <a name="perm--int"></a>macht: [int](xref:microsoft.quantum.lang-ref.int)[]

Een permutatie van $2 ^ n $ elementen vanaf 0.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een lijst met $n $ qubits waarop de permutatie wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

- [*Alexis de Vos* , *Yvan van Rentergem* , adv. in math. van comm. 2 (2), 2008, pp. 183--200](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [*Mathias soeken* , *Laura Tague* , *Gerhard W. Dueck* , *Rolf Drechsler* , Journal of symbolische berekening 73 (2016), pp. 1--26](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. synthese. ApplyPermutationUsingDecompositionWithVariableOrder](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [Micro soft. Quantum. synthese. ApplyPermutationUsingTransformation](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)