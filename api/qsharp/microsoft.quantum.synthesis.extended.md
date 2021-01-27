---
uid: Microsoft.Quantum.Synthesis.Extended
title: Uitgebreide functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855477"
---
# <a name="extended-function"></a><span data-ttu-id="ccca7-102">Uitgebreide functie</span><span class="sxs-lookup"><span data-stu-id="ccca7-102">Extended function</span></span>

<span data-ttu-id="ccca7-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ccca7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ccca7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ccca7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ccca7-105">Breidt een spectrum uit door omgedraaide coëfficiënten</span><span class="sxs-lookup"><span data-stu-id="ccca7-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="ccca7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ccca7-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="ccca7-107">spectrum: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ccca7-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ccca7-108">Spectral coëfficiënten</span><span class="sxs-lookup"><span data-stu-id="ccca7-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="ccca7-109">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ccca7-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ccca7-110">Coëfficiënten gevolgd door een omgekeerde kopie</span><span class="sxs-lookup"><span data-stu-id="ccca7-110">Coefficients followed by inverted copy</span></span>

## <a name="example"></a><span data-ttu-id="ccca7-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ccca7-111">Example</span></span>

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```