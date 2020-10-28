---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: De functie RMEncoding
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: ef9be0f0628c8ba8c5f131cc558bdcda6bb6ea55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709283"
---
# <a name="rmencoding-function"></a><span data-ttu-id="930a4-102">De functie RMEncoding</span><span class="sxs-lookup"><span data-stu-id="930a4-102">RMEncoding function</span></span>

<span data-ttu-id="930a4-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="930a4-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="930a4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="930a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="930a4-105">{-1,1} code ring van een waarheids waarde voor Booleaanse waarden</span><span class="sxs-lookup"><span data-stu-id="930a4-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="930a4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="930a4-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="930a4-107">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="930a4-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="930a4-108">Booleaanse waarde</span><span class="sxs-lookup"><span data-stu-id="930a4-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="930a4-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="930a4-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="930a4-110">1, indien `b` Onwaar, anders-1</span><span class="sxs-lookup"><span data-stu-id="930a4-110">1, if `b` is false, otherwise -1</span></span>