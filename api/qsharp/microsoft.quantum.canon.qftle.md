---
uid: Microsoft.Quantum.Canon.QFTLE
title: Bewerking QFTLE
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: f28f74d34fb4688739646da3dc12ae6734eb4ad4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703898"
---
# <a name="qftle-operation"></a><span data-ttu-id="317bb-102">Bewerking QFTLE</span><span class="sxs-lookup"><span data-stu-id="317bb-102">QFTLE operation</span></span>

<span data-ttu-id="317bb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="317bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="317bb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="317bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="317bb-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de indeling van Little Endian bevat.</span><span class="sxs-lookup"><span data-stu-id="317bb-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="317bb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="317bb-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="317bb-107">qs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="317bb-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="317bb-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="317bb-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="317bb-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="317bb-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="317bb-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="317bb-110">Remarks</span></span>

<span data-ttu-id="317bb-111">De invoer en uitvoer worden gezien als little endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="317bb-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="317bb-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="317bb-112">See Also</span></span>

- [<span data-ttu-id="317bb-113">Micro soft. Quantum. Canon. QFT</span><span class="sxs-lookup"><span data-stu-id="317bb-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)