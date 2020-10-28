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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="5812c-102">Door de gebruiker gedefinieerd PhaseLittleEndian-type</span><span class="sxs-lookup"><span data-stu-id="5812c-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="5812c-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5812c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5812c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5812c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5812c-105">Niet-ondertekende integers van Little-Endian in QFT.</span><span class="sxs-lookup"><span data-stu-id="5812c-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="5812c-106">Als $ \ket{x} $ bijvoorbeeld de code ring little-endian van het gehele getal $x $ in de berekening is, dan is $ \operatorname{QFTLE} \ket{x} $ de code ring van $x $ in de QFT basis.</span><span class="sxs-lookup"><span data-stu-id="5812c-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="5812c-107">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5812c-107">Remarks</span></span>

<span data-ttu-id="5812c-108">We hebben afkorting `PhaseLittleEndian` als `PhaseLE` in de documentatie.</span><span class="sxs-lookup"><span data-stu-id="5812c-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="5812c-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5812c-109">See Also</span></span>

- [<span data-ttu-id="5812c-110">Micro soft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="5812c-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="5812c-111">Micro soft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="5812c-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)