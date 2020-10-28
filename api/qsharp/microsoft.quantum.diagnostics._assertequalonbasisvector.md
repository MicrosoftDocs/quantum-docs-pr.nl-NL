---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702831"
---
# <a name="_assertequalonbasisvector-operation"></a>_assertEqualOnBasisVector bewerking

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Hiermee wordt gecontroleerd of het resultaat van het Toep assen van twee bewerkingen `givenU` en `expectedU` de basis status hetzelfde is. De basis status wordt beschreven met de `basis` para meter.
Zie <xref:microsoft.quantum.extensions.fliptobasis> functie voor meer informatie over deze beschrijving.

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Invoer

### <a name="basis--int"></a>soort_jaar: [int](xref:microsoft.quantum.lang-ref.int)[]

Basis status opgegeven door een basis status-ID van één Qubit (0 <= id <= 3) voor elk van $n $ qubits.


### <a name="givenu--qubit--unit"></a>givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Bewerking op $n $ qubits moet worden gecontroleerd.


### <a name="expectedu--qubit--unit-adj"></a>expectedU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Verwijzings bewerking op $n $ qubits dat givenU moet worden vergeleken.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

