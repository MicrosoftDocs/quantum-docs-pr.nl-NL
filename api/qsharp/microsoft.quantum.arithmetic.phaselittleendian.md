---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Door de gebruiker gedefinieerd PhaseLittleEndian-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 45b824a74d664df0d5707264a3c616fb27c477b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222419"
---
# <a name="phaselittleendian-user-defined-type"></a>Door de gebruiker gedefinieerd PhaseLittleEndian-type

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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