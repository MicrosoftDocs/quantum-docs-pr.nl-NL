---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Door de gebruiker gedefinieerd PhaseLittleEndian-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: f1f792d62004a2765d4e63870f5a41a4377b0d34
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706349"
---
# <a name="phaselittleendian-user-defined-type"></a>Door de gebruiker gedefinieerd PhaseLittleEndian-type

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Niet-ondertekende integers van Little-Endian in QFT.

Als $ \ket{x} $ bijvoorbeeld de code ring little-endian van het gehele getal $x $ in de berekening is, dan is $ \operatorname{QFTLE} \ket{x} $ de code ring van $x $ in de QFT basis.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Opmerkingen

We hebben afkorting `PhaseLittleEndian` als `PhaseLE` in de documentatie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. QFT](xref:Microsoft.Quantum.Canon.QFT)
- [Micro soft. Quantum. Canon. QFTLE](xref:Microsoft.Quantum.Canon.QFTLE)