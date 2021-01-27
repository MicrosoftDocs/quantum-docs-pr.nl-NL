---
uid: Microsoft.Quantum.Math.InverseModL
title: De functie InverseModL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e09c9da500889dfcb514d0a02dec957bfaa70e1c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851393"
---
# <a name="inversemodl-function"></a><span data-ttu-id="f0d6c-102">De functie InverseModL</span><span class="sxs-lookup"><span data-stu-id="f0d6c-102">InverseModL function</span></span>

<span data-ttu-id="f0d6c-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f0d6c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f0d6c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0d6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0d6c-105">Retourneert $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="f0d6c-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="f0d6c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f0d6c-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="f0d6c-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f0d6c-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f0d6c-108">Het getal wordt omgekeerd</span><span class="sxs-lookup"><span data-stu-id="f0d6c-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="f0d6c-109">modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f0d6c-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f0d6c-110">De modulus op basis waarvan de getallen worden omgekeerd</span><span class="sxs-lookup"><span data-stu-id="f0d6c-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="f0d6c-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f0d6c-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f0d6c-112">Geheel getal $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="f0d6c-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>