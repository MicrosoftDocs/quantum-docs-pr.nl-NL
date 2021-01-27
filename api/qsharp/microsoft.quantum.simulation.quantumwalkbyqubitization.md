---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: De functie QuantumWalkByQubitization
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: 8ffb6eb77a3f910d3064c4a3c90215d5d9a694aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851061"
---
# <a name="quantumwalkbyqubitization-function"></a>De functie QuantumWalkByQubitization

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een weer spiegeling van blok-encoding omgezet in een Quantum Walk.

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a>Beschrijving

Gezien een `BlockEncodingReflection` vertegenwoordigd door een unitary $U $ waarmee een bepaalde operator $H $ of interest wordt gecodeerd, wordt deze omgezet in een Quantum walk $W $ met het spectrum $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.

## <a name="input"></a>Invoer

### <a name="blockencoding--blockencodingreflection"></a>blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Een `BlockEncodingReflection` unitary $U $ worden geconverteerd naar een Quantum Walk.



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een Quantum Walk $W $ communiceert samen met `a` de registers en `s` de blok code ring $H $, en bevat het spectrum $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.

## <a name="references"></a>Verwijzingen

- Hamiltonian simulatie door Qubitization Guang Hao laag, Isaac L. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Micro soft. Quantum. simulatie. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)