---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Bewerking ApplyQuantumFourierTransformBE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: a1f4a0a5e94465fc8bf3af344e2e19ee0d1d15e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841569"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="e4379-102">Bewerking ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="e4379-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="e4379-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e4379-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e4379-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e4379-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e4379-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de weer gave big endian bevat.</span><span class="sxs-lookup"><span data-stu-id="e4379-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e4379-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e4379-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="e4379-107">qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="e4379-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="e4379-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="e4379-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="e4379-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e4379-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e4379-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e4379-110">Remarks</span></span>

<span data-ttu-id="e4379-111">De invoer en uitvoer worden gezien als big endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="e4379-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4379-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e4379-112">See Also</span></span>

- [<span data-ttu-id="e4379-113">Micro soft. Quantum. Canon. ApproximateQFT</span><span class="sxs-lookup"><span data-stu-id="e4379-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="e4379-114">Micro soft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="e4379-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)