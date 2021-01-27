---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Bewerking ApplyQuantumFourierTransform
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: d99000c21c79d2ca97b1fe92ad331c7ba8599700
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844760"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="0ff07-102">Bewerking ApplyQuantumFourierTransform</span><span class="sxs-lookup"><span data-stu-id="0ff07-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="0ff07-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0ff07-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0ff07-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0ff07-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0ff07-105">Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de indeling van Little Endian bevat.</span><span class="sxs-lookup"><span data-stu-id="0ff07-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0ff07-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0ff07-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="0ff07-107">qs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0ff07-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0ff07-108">Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="0ff07-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ff07-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ff07-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0ff07-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0ff07-110">Remarks</span></span>

<span data-ttu-id="0ff07-111">De invoer en uitvoer worden gezien als little endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="0ff07-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ff07-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0ff07-112">See Also</span></span>

- [<span data-ttu-id="0ff07-113">Micro soft. Quantum. Canon. ApplyQuantumFourierTransformBE</span><span class="sxs-lookup"><span data-stu-id="0ff07-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)