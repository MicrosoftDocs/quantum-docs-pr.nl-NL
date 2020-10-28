---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Bewerking AssertPhase
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702746"
---
# <a name="assertphase-operation"></a>Bewerking AssertPhase

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Er wordt bevestigd dat de fase van een gelijke superpositie status de verwachte waarde heeft.

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt in de fase $ \phi $ van een Quantum status aangegeven dat kan worden uitgedrukt als $ \frac{e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket {1} ) $ voor een wille keurig Real $t $ de verwachte waarde heeft.

## <a name="input"></a>Invoer

### <a name="expected--double"></a>verwacht: [Double](xref:microsoft.quantum.lang-ref.double)

De verwachte waarde van $ \phi \in (-\pi, \pi] $.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De Qubit waarin de verwachte status wordt opgeslagen.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Absolute tolerantie voor het verschil tussen werkelijk en verwacht.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

