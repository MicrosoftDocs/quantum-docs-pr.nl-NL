---
uid: Microsoft.Quantum.Convert.MaybeBigIntAsInt
title: De functie MaybeBigIntAsInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: MaybeBigIntAsInt
qsharp.summary: Converts a given big integer to an equivalent integer, if possible. The function returns a pair of the resulting integer and a Boolean flag which is true, if and only if the conversion was possible.
ms.openlocfilehash: b91912f6f669afad888e71174fef6e2e6f8e7156
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702951"
---
# <a name="maybebigintasint-function"></a>De functie MaybeBigIntAsInt

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket [](https://nuget.org/packages/)


Converteert een gegeven groot geheel getal naar een gelijkwaardig geheel getal, indien mogelijk.
De functie retourneert een paar van het resulterende geheel getal en een Booleaanse vlag die waar en alleen als de conversie mogelijk was.

```qsharp
function MaybeBigIntAsInt (a : BigInt) : (Int, Bool)
```


## <a name="input"></a>Invoer

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--intbool"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[BOOL](xref:microsoft.quantum.lang-ref.bool))



## <a name="remarks"></a>Opmerkingen

Zie [C# BigInteger-constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) voor meer informatie.