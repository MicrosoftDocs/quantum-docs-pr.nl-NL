---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: De functie IsCoprimeL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: c78e995801f67822cf98104a7319093d853b6afe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228131"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="bf170-102">De functie IsCoprimeL</span><span class="sxs-lookup"><span data-stu-id="bf170-102">IsCoprimeL function</span></span>

<span data-ttu-id="bf170-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="bf170-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="bf170-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bf170-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bf170-105">Retourneert waar als $a $ en $b $ co-Prime en ONWAAR anders zijn.</span><span class="sxs-lookup"><span data-stu-id="bf170-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="bf170-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bf170-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="bf170-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="bf170-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="bf170-108">het eerste getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="bf170-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="bf170-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="bf170-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="bf170-110">het tweede getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="bf170-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="bf170-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bf170-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bf170-112">Waar, als $a $ en $b $ co-Prime zijn (bijvoorbeeld de grootste gemene deler is 1) en ONWAAR, anders</span><span class="sxs-lookup"><span data-stu-id="bf170-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>