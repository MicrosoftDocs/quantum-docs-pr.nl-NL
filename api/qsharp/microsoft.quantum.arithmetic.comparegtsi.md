---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: Bewerking CompareGTSI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: a0e8ef66f1e1a62d4f6a78364135376810507534
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223490"
---
# <a name="comparegtsi-operation"></a><span data-ttu-id="7cf74-102">Bewerking CompareGTSI</span><span class="sxs-lookup"><span data-stu-id="7cf74-102">CompareGTSI operation</span></span>

<span data-ttu-id="7cf74-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7cf74-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7cf74-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="7cf74-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="7cf74-105">Wrapper voor ondertekende integer-vergelijking: `result = xs > ys` .</span><span class="sxs-lookup"><span data-stu-id="7cf74-105">Wrapper for signed integer comparison: `result = xs > ys`.</span></span>

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7cf74-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7cf74-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="7cf74-107">XS: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7cf74-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="7cf74-108">Eerste $n $-bits nummer</span><span class="sxs-lookup"><span data-stu-id="7cf74-108">First $n$-bit number</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="7cf74-109">kalenderda: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7cf74-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="7cf74-110">Tweede $n $-bits nummer</span><span class="sxs-lookup"><span data-stu-id="7cf74-110">Second $n$-bit number</span></span>


### <a name="result--qubit"></a><span data-ttu-id="7cf74-111">resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7cf74-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7cf74-112">Wordt gespiegeld als $xs > kalenderda $</span><span class="sxs-lookup"><span data-stu-id="7cf74-112">Will be flipped if $xs > ys$</span></span>



## <a name="output--unit"></a><span data-ttu-id="7cf74-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7cf74-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

