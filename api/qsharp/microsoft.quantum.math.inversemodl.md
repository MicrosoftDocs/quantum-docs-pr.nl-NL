---
uid: Microsoft.Quantum.Math.InverseModL
title: De functie InverseModL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e7cb9e98cb0635c50162611f6a52c56027d4a5eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708491"
---
# <a name="inversemodl-function"></a><span data-ttu-id="40a05-102">De functie InverseModL</span><span class="sxs-lookup"><span data-stu-id="40a05-102">InverseModL function</span></span>

<span data-ttu-id="40a05-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="40a05-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="40a05-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40a05-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40a05-105">Retourneert $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="40a05-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="40a05-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="40a05-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="40a05-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="40a05-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="40a05-108">Het getal wordt omgekeerd</span><span class="sxs-lookup"><span data-stu-id="40a05-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="40a05-109">modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="40a05-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="40a05-110">De modulus op basis waarvan de getallen worden omgekeerd</span><span class="sxs-lookup"><span data-stu-id="40a05-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="40a05-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="40a05-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="40a05-112">Geheel getal $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="40a05-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>