---
uid: Microsoft.Quantum.Canon.QFT
title: Bewerking QFT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 8f1aa8c3680a068e500503ca25afa9a49e4ef5bf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205525"
---
# <a name="qft-operation"></a><span data-ttu-id="f200c-102">Bewerking QFT</span><span class="sxs-lookup"><span data-stu-id="f200c-102">QFT operation</span></span>

<span data-ttu-id="f200c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f200c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f200c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f200c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f200c-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de weer gave big endian bevat.</span><span class="sxs-lookup"><span data-stu-id="f200c-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f200c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f200c-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="f200c-107">qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="f200c-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="f200c-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="f200c-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="f200c-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f200c-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f200c-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f200c-110">Remarks</span></span>

<span data-ttu-id="f200c-111">De invoer en uitvoer worden gezien als big endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="f200c-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="f200c-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f200c-112">See Also</span></span>

- [<span data-ttu-id="f200c-113">Micro soft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="f200c-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)