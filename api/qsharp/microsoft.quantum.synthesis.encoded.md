---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Gecodeerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 803f35b9e7af547bc34f21de74684fba885bfda9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203175"
---
# <a name="encoded-function"></a><span data-ttu-id="34600-102">Gecodeerde functie</span><span class="sxs-lookup"><span data-stu-id="34600-102">Encoded function</span></span>

<span data-ttu-id="34600-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="34600-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="34600-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34600-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34600-105">Een waarheids tabel coderen in {1,-1} code ring</span><span class="sxs-lookup"><span data-stu-id="34600-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="34600-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="34600-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="34600-107">tabel: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="34600-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="34600-108">Waarheids tabel als een matrix met waarheids waarden</span><span class="sxs-lookup"><span data-stu-id="34600-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="34600-109">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="34600-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="34600-110">Tabel met waarheid als matrix van {1,-1} gehele getallen</span><span class="sxs-lookup"><span data-stu-id="34600-110">Truth table as array of {1,-1} integers</span></span>