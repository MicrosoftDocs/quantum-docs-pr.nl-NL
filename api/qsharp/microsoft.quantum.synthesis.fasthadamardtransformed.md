---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: De functie FastHadamardTransformed
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 2b84e92d08a3baad2552780cae91f447830cac82
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709157"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="c380a-102">De functie FastHadamardTransformed</span><span class="sxs-lookup"><span data-stu-id="c380a-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="c380a-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c380a-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c380a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c380a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c380a-105">Hiermee wordt de Hadamard-trans formatie van een Boole-functie in {-1,1} code ring berekend met behulp van de methode van Yates</span><span class="sxs-lookup"><span data-stu-id="c380a-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="c380a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c380a-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="c380a-107">FUNC: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c380a-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c380a-108">Waarheids tabel in {-1,1} code ring</span><span class="sxs-lookup"><span data-stu-id="c380a-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="c380a-109">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c380a-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c380a-110">Spectral coëfficiënten van de functie</span><span class="sxs-lookup"><span data-stu-id="c380a-110">Spectral coefficients of the function</span></span>