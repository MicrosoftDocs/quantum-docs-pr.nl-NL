---
uid: Microsoft.Quantum.Convert.MaybeBigIntAsInt
title: De functie MaybeBigIntAsInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: MaybeBigIntAsInt
qsharp.summary: Converts a given big integer to an equivalent integer, if possible. The function returns a pair of the resulting integer and a Boolean flag which is true, if and only if the conversion was possible.
ms.openlocfilehash: 1f10ac027f8f289e5ea554a7804abeb33def4df8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832768"
---
# <a name="maybebigintasint-function"></a><span data-ttu-id="6aa83-102">De functie MaybeBigIntAsInt</span><span class="sxs-lookup"><span data-stu-id="6aa83-102">MaybeBigIntAsInt function</span></span>

<span data-ttu-id="6aa83-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="6aa83-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="6aa83-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6aa83-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6aa83-105">Converteert een gegeven groot geheel getal naar een gelijkwaardig geheel getal, indien mogelijk.</span><span class="sxs-lookup"><span data-stu-id="6aa83-105">Converts a given big integer to an equivalent integer, if possible.</span></span>
<span data-ttu-id="6aa83-106">De functie retourneert een paar van het resulterende geheel getal en een Booleaanse vlag die waar en alleen als de conversie mogelijk was.</span><span class="sxs-lookup"><span data-stu-id="6aa83-106">The function returns a pair of the resulting integer and a Boolean flag which is true, if and only if the conversion was possible.</span></span>

```qsharp
function MaybeBigIntAsInt (a : BigInt) : (Int, Bool)
```


## <a name="input"></a><span data-ttu-id="6aa83-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="6aa83-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="6aa83-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6aa83-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--intbool"></a><span data-ttu-id="6aa83-109">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[BOOL](xref:microsoft.quantum.lang-ref.bool))</span><span class="sxs-lookup"><span data-stu-id="6aa83-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool))</span></span>



## <a name="remarks"></a><span data-ttu-id="6aa83-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6aa83-110">Remarks</span></span>

<span data-ttu-id="6aa83-111">Zie [C# BigInteger-constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6aa83-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>