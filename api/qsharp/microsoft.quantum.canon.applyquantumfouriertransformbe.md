---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Bewerking ApplyQuantumFourierTransformBE
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 39db7b4c69f7f06418ec257c013837c65b9cc67a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209040"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="695ec-102">Bewerking ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="695ec-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="695ec-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="695ec-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="695ec-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="695ec-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="695ec-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de weer gave big endian bevat.</span><span class="sxs-lookup"><span data-stu-id="695ec-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="695ec-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="695ec-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="695ec-107">qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="695ec-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="695ec-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="695ec-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="695ec-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="695ec-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="695ec-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="695ec-110">Remarks</span></span>

<span data-ttu-id="695ec-111">De invoer en uitvoer worden gezien als big endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="695ec-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="695ec-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="695ec-112">See Also</span></span>

- [<span data-ttu-id="695ec-113">Micro soft. Quantum. Canon. ApproximateQFT</span><span class="sxs-lookup"><span data-stu-id="695ec-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="695ec-114">Micro soft. Quantum. Canon. QFTLE</span><span class="sxs-lookup"><span data-stu-id="695ec-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)