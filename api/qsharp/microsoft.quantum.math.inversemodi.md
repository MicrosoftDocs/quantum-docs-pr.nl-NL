---
uid: Microsoft.Quantum.Math.InverseModI
title: De functie InverseModI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 474146e644bcd042e85b917bc43135a674bedce1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846888"
---
# <a name="inversemodi-function"></a><span data-ttu-id="639a6-102">De functie InverseModI</span><span class="sxs-lookup"><span data-stu-id="639a6-102">InverseModI function</span></span>

<span data-ttu-id="639a6-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="639a6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="639a6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="639a6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="639a6-105">Retourneert $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="639a6-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="639a6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="639a6-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="639a6-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="639a6-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="639a6-108">Het getal wordt omgekeerd</span><span class="sxs-lookup"><span data-stu-id="639a6-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="639a6-109">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="639a6-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="639a6-110">De modulus op basis waarvan de getallen worden omgekeerd</span><span class="sxs-lookup"><span data-stu-id="639a6-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="639a6-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="639a6-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="639a6-112">Geheel getal $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="639a6-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>