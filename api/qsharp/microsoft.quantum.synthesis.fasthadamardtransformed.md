---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: De functie FastHadamardTransformed
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 3e48701f22ddf154721355866e15a85fca0bc7df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203090"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="f7557-102">De functie FastHadamardTransformed</span><span class="sxs-lookup"><span data-stu-id="f7557-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="f7557-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f7557-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f7557-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7557-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f7557-105">Hiermee wordt de Hadamard-trans formatie van een Boole-functie in {-1,1} code ring berekend met behulp van de methode van Yates</span><span class="sxs-lookup"><span data-stu-id="f7557-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="f7557-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f7557-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="f7557-107">FUNC: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f7557-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f7557-108">Waarheids tabel in {-1,1} code ring</span><span class="sxs-lookup"><span data-stu-id="f7557-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="f7557-109">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f7557-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f7557-110">Spectral coëfficiënten van de functie</span><span class="sxs-lookup"><span data-stu-id="f7557-110">Spectral coefficients of the function</span></span>