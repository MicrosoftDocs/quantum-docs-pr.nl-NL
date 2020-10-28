---
uid: Microsoft.Quantum.Canon.QFT
title: Bewerking QFT
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: e5b40be6c86647205fe1c764b6b043272296a354
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703904"
---
# <a name="qft-operation"></a><span data-ttu-id="6bce7-102">Bewerking QFT</span><span class="sxs-lookup"><span data-stu-id="6bce7-102">QFT operation</span></span>

<span data-ttu-id="6bce7-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6bce7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6bce7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6bce7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6bce7-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de weer gave big endian bevat.</span><span class="sxs-lookup"><span data-stu-id="6bce7-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="6bce7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6bce7-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="6bce7-107">qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="6bce7-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="6bce7-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="6bce7-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="6bce7-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6bce7-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6bce7-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6bce7-110">Remarks</span></span>

<span data-ttu-id="6bce7-111">De invoer en uitvoer worden gezien als big endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="6bce7-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="6bce7-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6bce7-112">See Also</span></span>

- [<span data-ttu-id="6bce7-113">Micro soft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="6bce7-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)