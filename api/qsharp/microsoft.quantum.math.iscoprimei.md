---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: De functie IsCoprimeI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 2c110f9abf18ee81bd72a68601d5c41ff756290a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851354"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="0e551-102">De functie IsCoprimeI</span><span class="sxs-lookup"><span data-stu-id="0e551-102">IsCoprimeI function</span></span>

<span data-ttu-id="0e551-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="0e551-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="0e551-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0e551-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0e551-105">Retourneert waar als $a $ en $b $ co-Prime en ONWAAR anders zijn.</span><span class="sxs-lookup"><span data-stu-id="0e551-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="0e551-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0e551-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="0e551-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0e551-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0e551-108">het eerste getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="0e551-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="0e551-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0e551-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0e551-110">het tweede getal waarvan co-primality wordt getest</span><span class="sxs-lookup"><span data-stu-id="0e551-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="0e551-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0e551-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0e551-112">Waar, als $a $ en $b $ co-Prime zijn (bijvoorbeeld de grootste gemene deler is 1) en ONWAAR, anders</span><span class="sxs-lookup"><span data-stu-id="0e551-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>