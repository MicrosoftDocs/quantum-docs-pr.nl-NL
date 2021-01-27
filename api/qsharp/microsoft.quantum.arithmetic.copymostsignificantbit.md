---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Bewerking CopyMostSignificantBit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843271"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="1c14b-102">Bewerking CopyMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="1c14b-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="1c14b-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1c14b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1c14b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1c14b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1c14b-105">Hiermee wordt de meest significante bit van een Qubit-REGI ster gekopieerd `from` die een niet-ondertekend geheel getal vertegenwoordigt in de Qubit `target` .</span><span class="sxs-lookup"><span data-stu-id="1c14b-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="1c14b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1c14b-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="1c14b-107">van: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1c14b-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1c14b-108">Het niet-ondertekende integer waarvan de hoogste bit wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="1c14b-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="1c14b-109">het gehele getal is gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="1c14b-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="1c14b-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1c14b-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1c14b-111">De Qubit waarin de hoogste bit wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="1c14b-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="1c14b-112">De bits code ring wordt berekend op basis van de berekening.</span><span class="sxs-lookup"><span data-stu-id="1c14b-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1c14b-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1c14b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1c14b-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1c14b-114">See Also</span></span>

- [<span data-ttu-id="1c14b-115">Micro soft. Quantum. aritmetische. LittleEndian</span><span class="sxs-lookup"><span data-stu-id="1c14b-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)