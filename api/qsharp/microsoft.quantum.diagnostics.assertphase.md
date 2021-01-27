---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Bewerking AssertPhase
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830085"
---
# <a name="assertphase-operation"></a>Bewerking AssertPhase

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Voorbeeld

De volgende assert is geslaagd: `qubit` heeft de status $ \ket{\psi} = e ^ {i 0.5} \ SQRT {1/2} \ Ket {0} + e ^ {i 0.5} \ SQRT {1/2} \ Ket {1} $;

- `AssertPhase(0.0,qubit,10e-10);`

`qubit` heeft de status $ \ket{\psi} = e ^ {i 0.5} \ SQRT {1/2} \ Ket {0} + e ^ {-i 0.5} \ SQRT {1/2} \ Ket {1} $;

- `AssertPhase(0.5,qubit,10e-10);`

`qubit` heeft de status $ \ket{\psi} = e ^ {-i 2,2} \ SQRT {1/2} \ Ket {0} + e ^ {i 0,2} \ SQRT {1/2} \ Ket {1} $;

- `AssertPhase(-1.2,qubit,10e-10);`