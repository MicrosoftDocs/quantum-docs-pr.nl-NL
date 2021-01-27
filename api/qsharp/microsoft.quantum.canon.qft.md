---
uid: Microsoft.Quantum.Canon.QFT
title: Bewerking QFT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 30f475c3850c248b5af58db1e4aac3638c4c0471
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852296"
---
# <a name="qft-operation"></a><span data-ttu-id="46d34-102">Bewerking QFT</span><span class="sxs-lookup"><span data-stu-id="46d34-102">QFT operation</span></span>

<span data-ttu-id="46d34-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="46d34-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="46d34-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="46d34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="46d34-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de weer gave big endian bevat.</span><span class="sxs-lookup"><span data-stu-id="46d34-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="46d34-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="46d34-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="46d34-107">qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="46d34-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="46d34-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="46d34-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="46d34-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46d34-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="46d34-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="46d34-110">Remarks</span></span>

<span data-ttu-id="46d34-111">De invoer en uitvoer worden gezien als big endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="46d34-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="46d34-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="46d34-112">See Also</span></span>

- [<span data-ttu-id="46d34-113">Micro soft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="46d34-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)