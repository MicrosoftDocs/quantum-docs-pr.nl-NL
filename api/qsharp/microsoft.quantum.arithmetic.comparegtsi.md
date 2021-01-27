---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Bewerking CompareGTSI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: f725bdbaa945a4f87e90fc71930c37642113c21a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846694"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="13a81-102">Bewerking CompareGTSI</span><span class="sxs-lookup"><span data-stu-id="13a81-102">CompareGTSI operation</span></span>

<span data-ttu-id="13a81-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="13a81-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="13a81-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="13a81-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="13a81-105">Wrapper voor ondertekende integer-vergelijking: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="13a81-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="13a81-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="13a81-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="13a81-107">XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="13a81-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="13a81-108">Eerste $n $-bits nummer</span><span class="sxs-lookup"><span data-stu-id="13a81-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="13a81-109">kalenderda: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="13a81-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="13a81-110">Tweede $n $-bits nummer</span><span class="sxs-lookup"><span data-stu-id="13a81-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="13a81-111">resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="13a81-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="13a81-112">Wordt gespiegeld als $xs > kalenderda $</span><span class="sxs-lookup"><span data-stu-id="13a81-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="13a81-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13a81-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

