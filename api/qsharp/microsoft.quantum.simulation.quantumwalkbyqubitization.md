---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: De functie QuantumWalkByQubitization
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ef9740f1867cee3c79a7ec0bf90f2c2f4b39ad28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709325"
---
# <a name="quantumwalkbyqubitization-function"></a>De functie QuantumWalkByQubitization

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een weer spiegeling van blok-encoding omgezet in een Quantum Walk.

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a>Beschrijving

Gezien een `BlockEncodingReflection` vertegenwoordigd door een unitary $U $ waarmee een bepaalde operator $H $ of interest wordt gecodeerd, wordt deze omgezet in een Quantum walk $W $ met het spectrum $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.

## <a name="input"></a>Invoer

### <a name="blockencoding--blockencodingreflection"></a>blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Een `BlockEncodingReflection` unitary $U $ worden geconverteerd naar een Quantum Walk.



## <a name="output--qubitqubit--unit-adj--ctl"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een Quantum Walk $W $ communiceert samen met `a` de registers en `s` de blok code ring $H $, en bevat het spectrum $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.

## <a name="references"></a>Naslaginformatie

- Hamiltonian simulatie door Qubitization Guang Hao laag, Isaac L. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Micro soft. Quantum. simulatie. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)