---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: De functie BlockEncodingToReflection
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: bada0dcc54d2a8d67cf7383d7153c7f46a4a8415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847261"
---
# <a name="blockencodingtoreflection-function"></a><span data-ttu-id="b9464-102">De functie BlockEncodingToReflection</span><span class="sxs-lookup"><span data-stu-id="b9464-102">BlockEncodingToReflection function</span></span>

<span data-ttu-id="b9464-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b9464-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b9464-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b9464-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b9464-105">Converteert een `BlockEncoding` in een gelijkwaardige waarde `BLockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="b9464-105">Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.</span></span>

<span data-ttu-id="b9464-106">Op basis van een `BlockEncoding` unitary $U $ die een bepaalde operator $H $ van de rente codeert, wordt deze omgezet in een `BlockEncodingReflection` $U $ die dezelfde operator codeert, maar ook voldoet aan $U ^ \Dagger = U ' $ '.</span><span class="sxs-lookup"><span data-stu-id="b9464-106">That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$.</span></span>
<span data-ttu-id="b9464-107">Dit verhoogt de grootte van het hulp register van $U $ door één Qubit.</span><span class="sxs-lookup"><span data-stu-id="b9464-107">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="b9464-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="b9464-108">Input</span></span>

### <a name="blockencoding--blockencoding"></a><span data-ttu-id="b9464-109">blockEncoding: [blockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span><span class="sxs-lookup"><span data-stu-id="b9464-109">blockEncoding : [BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span></span>

<span data-ttu-id="b9464-110">Een `BlockEncoding` unitary $U $ moet worden geconverteerd naar een reflectie.</span><span class="sxs-lookup"><span data-stu-id="b9464-110">A `BlockEncoding` unitary $U$ to be converted into a reflection.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="b9464-111">Uitvoer: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="b9464-111">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="b9464-112">Een unitary-$U ' $ communiceert gezamenlijk aan registers `a` en `s` die blok-coderings $H $, en voldoet aan $U ^ \Dagger = U ' $.</span><span class="sxs-lookup"><span data-stu-id="b9464-112">A unitary $U'$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^\dagger = U'$.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9464-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b9464-113">Remarks</span></span>

<span data-ttu-id="b9464-114">Dit verhoogt de grootte van het hulp register van $U $ door één Qubit.</span><span class="sxs-lookup"><span data-stu-id="b9464-114">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

## <a name="references"></a><span data-ttu-id="b9464-115">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="b9464-115">References</span></span>

- <span data-ttu-id="b9464-116">Hamiltonian simulatie door Qubitization Guang Hao laag, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="b9464-116">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="b9464-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b9464-117">See Also</span></span>

- [<span data-ttu-id="b9464-118">Micro soft. Quantum. simulatie. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="b9464-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="b9464-119">Micro soft. Quantum. simulatie. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="b9464-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)