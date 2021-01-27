---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Door de gebruiker gedefinieerd PhaseLittleEndian-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 59df1db31090f875ccd261fe6cc43995ba57b963
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843002"
---
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="29160-102">Door de gebruiker gedefinieerd PhaseLittleEndian-type</span><span class="sxs-lookup"><span data-stu-id="29160-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="29160-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="29160-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="29160-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="29160-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="29160-105">Niet-ondertekende integers van Little-Endian in QFT.</span><span class="sxs-lookup"><span data-stu-id="29160-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="29160-106">Als $ \ket{x} $ bijvoorbeeld de code ring little-endian van het gehele getal $x $ in de berekening is, dan is $ \operatorname{QFTLE} \ket{x} $ de code ring van $x $ in de QFT basis.</span><span class="sxs-lookup"><span data-stu-id="29160-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="29160-107">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="29160-107">Remarks</span></span>

<span data-ttu-id="29160-108">We hebben afkorting `PhaseLittleEndian` als `PhaseLE` in de documentatie.</span><span class="sxs-lookup"><span data-stu-id="29160-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="29160-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="29160-109">See Also</span></span>

- [<span data-ttu-id="29160-110">Micro soft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="29160-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="29160-111">Micro soft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="29160-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)