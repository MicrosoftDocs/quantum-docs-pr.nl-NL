---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: De functie BoolArrayAsBigInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 75656ba188a1b822eb42e98412365bf5873bf46e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703029"
---
# <a name="boolarrayasbigint-function"></a><span data-ttu-id="06f12-102">De functie BoolArrayAsBigInt</span><span class="sxs-lookup"><span data-stu-id="06f12-102">BoolArrayAsBigInt function</span></span>

<span data-ttu-id="06f12-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="06f12-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="06f12-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06f12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06f12-105">Hiermee wordt een opgegeven matrix met Boole-waarden geconverteerd naar een equivalent Big-geheel getal.</span><span class="sxs-lookup"><span data-stu-id="06f12-105">Converts a given array of Booleans to an equivalent big integer.</span></span>
<span data-ttu-id="06f12-106">Het element 0 van de matrix is de minst significante bit van het grote geheel getal.</span><span class="sxs-lookup"><span data-stu-id="06f12-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a><span data-ttu-id="06f12-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="06f12-107">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="06f12-108">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="06f12-108">a : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>





## <a name="output--bigint"></a><span data-ttu-id="06f12-109">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="06f12-109">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="06f12-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="06f12-110">Remarks</span></span>

<span data-ttu-id="06f12-111">Zie [C# BigInteger-constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="06f12-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>