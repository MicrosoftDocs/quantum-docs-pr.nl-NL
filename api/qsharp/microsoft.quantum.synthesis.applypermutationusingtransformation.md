---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Bewerking ApplyPermutationUsingTransformation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: 79913bec44514d477b7ee0668b43396b297b9ab8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858986"
---
# <a name="applypermutationusingtransformation-operation"></a>Bewerking ApplyPermutationUsingTransformation

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Permutaties de amplitudes in een Quantum status op basis van op trans formatie gebaseerde synthese.

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze procedure implementeert u de methode voor het op één richting gebaseerde synthese van een trans formatie.  De invoer is een permutatie $ \pi $ boven $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, die een $n variabele met een onomkeerbaare Boole-functie vertegenwoordigt.
De algoritme voert iteratieve uitvoering van de volgende stappen uit:

1. Zoek de kleinste $x $ zodat $x \ne \pi (x) = y $.
2. Zoek met meerdere beheerde Toffoli-bewerkingen, die worden toegepast op de uitvoer, maken $ \pi (x) = x $ en wijzig $ \pi (x ') $ niet voor alle $x < x $

## <a name="input"></a>Invoer

### <a name="perm--int"></a>macht: [int](xref:microsoft.quantum.lang-ref.int)[]

Een permutatie van $2 ^ n $ elementen vanaf 0.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een lijst met $n $ qubits waarop de permutatie wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

Een `SWAP` bewerking verwerken:

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingTransformation([0, 2, 1, 3], LittleEndian(qubits));
}
```

## <a name="references"></a>Verwijzingen

- [*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, proc. DAC 2003, IEEE, pp. 318-323, 2003](https://doi.org/10.1145/775832.775915)
- [*Mathias soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, proc. rc 2016, Springer, pp. 307-321, 2016](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. synthese. ApplyPermutationUsingDecomposition](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)