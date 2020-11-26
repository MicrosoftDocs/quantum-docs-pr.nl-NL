---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Bewerking ApplyXorInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210108"
---
# <a name="applyxorinplace-operation"></a><span data-ttu-id="c3b9c-102">Bewerking ApplyXorInPlace</span><span class="sxs-lookup"><span data-stu-id="c3b9c-102">ApplyXorInPlace operation</span></span>

<span data-ttu-id="c3b9c-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c3b9c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c3b9c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c3b9c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c3b9c-105">Past een Bitsgewijze-XOR-bewerking toe tussen een klassiek geheel getal en een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits.</span><span class="sxs-lookup"><span data-stu-id="c3b9c-105">Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.</span></span>

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c3b9c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c3b9c-106">Description</span></span>

<span data-ttu-id="c3b9c-107">Hiermee `X` worden bewerkingen toegepast op qubits in een little-endian-REGI ster op basis van 1 bits in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="c3b9c-107">Applies `X` operations to qubits in a little-endian register based on 1 bits in an integer.</span></span>

<span data-ttu-id="c3b9c-108">Laat het ons weten `value` en laat y een niet-ondertekend geheel getal dat is gecodeerd in en `target` `InPlaceXorLE` voert een bewerking uit die wordt gegeven door de volgende kaart: $ \ket{y}\rightarrow \ket{y\oplus a} $, waarbij $ \oplus $ de bitsgewijze exclusieve OR-operator is.</span><span class="sxs-lookup"><span data-stu-id="c3b9c-108">Let us denote `value` by a and let y be an unsigned integer encoded in `target`, then `InPlaceXorLE` performs an operation given by the following map: $\ket{y}\rightarrow \ket{y\oplus a}$ , where $\oplus$ is the bitwise exclusive OR operator.</span></span>

## <a name="input"></a><span data-ttu-id="c3b9c-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="c3b9c-109">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="c3b9c-110">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3b9c-110">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c3b9c-111">Een geheel getal dat wordt beschouwd als niet-negatief.</span><span class="sxs-lookup"><span data-stu-id="c3b9c-111">An integer which is assumed to be non-negative.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="c3b9c-112">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c3b9c-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c3b9c-113">Een Quantum register dat wordt gebruikt voor het opslaan `value` van de code ring met little endian.</span><span class="sxs-lookup"><span data-stu-id="c3b9c-113">A quantum register which is used to store `value` in little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3b9c-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3b9c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

