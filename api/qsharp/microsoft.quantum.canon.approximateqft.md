---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Bewerking ApproximateQFT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 31fd87c0f61292142c7493cc29cad1082a9a2d67
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850326"
---
# <a name="approximateqft-operation"></a>Bewerking ApproximateQFT

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


De benadering van de Quantum Fourier-trans formatie (AQFT) Toep assen op een Quantum register.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

een benaderingen-para meter waarmee wordt bepaald op welk niveau de bewaakte Z-rotaties die zich in het QFT-circuit bevinden, worden verwijderd.

Met de benaderings parameter a wordt het Pruning-niveau van de Z-rotaties bepaald, d.w.z. een ∈ {0.. n} en alle Z-rotaties 2π/2.000 waarbij k>a worden verwijderd uit het QFT-circuit. Het is bekend dat voor k >= log ₂ (n) en log ₂ (1/ε) + 3 een kan worden gebonden | | QFT-AQFT | |<ε.


### <a name="qs--bigendian"></a>qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Quantum register van n qubits waarmee de benadering van de Quantum Fourier-trans formatie wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

AQFT vereist Z-rotatie poorten van de vorm 2π/2.000 en Hadamard-Gates.

Er wordt van uitgegaan dat de invoer en uitvoer worden gecodeerd in big endian-code ring.

## <a name="references"></a>Verwijzingen

- [*M. Roetteler, th. Beth*, Vereffeningsnr. algebra eng. commun. Comput. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. Coppersmith* arXiv: Quant-pH/0201067v1](https://arxiv.org/abs/quant-ph/0201067)