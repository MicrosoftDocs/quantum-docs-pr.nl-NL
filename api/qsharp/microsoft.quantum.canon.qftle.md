---
uid: Microsoft.Quantum.Canon.QFTLE
title: Bewerking QFTLE
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: 460e43bc7997e9efad06c58ad14822e28cc45cdd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205572"
---
# <a name="qftle-operation"></a><span data-ttu-id="81b3a-102">Bewerking QFTLE</span><span class="sxs-lookup"><span data-stu-id="81b3a-102">QFTLE operation</span></span>

<span data-ttu-id="81b3a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="81b3a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="81b3a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81b3a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81b3a-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de indeling van Little Endian bevat.</span><span class="sxs-lookup"><span data-stu-id="81b3a-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="81b3a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="81b3a-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="81b3a-107">qs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="81b3a-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="81b3a-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="81b3a-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="81b3a-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81b3a-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="81b3a-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="81b3a-110">Remarks</span></span>

<span data-ttu-id="81b3a-111">De invoer en uitvoer worden gezien als little endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="81b3a-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="81b3a-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="81b3a-112">See Also</span></span>

- [<span data-ttu-id="81b3a-113">Micro soft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="81b3a-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)