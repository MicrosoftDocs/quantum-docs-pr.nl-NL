---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: De functie NearlyEqualD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: fbbf1f7a59600ecc4a0a59d1c08cd0e1310d2d20
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814375"
---
# <a name="nearlyequald-function"></a>De functie NearlyEqualD

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als twee invoer bijna gelijk is (dat wil zeggen, binnen een tolerantie van 1e-12).

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--double"></a>a: [dubbel](xref:microsoft.quantum.lang-ref.double)

De eerste waarde die moet worden vergeleken.


### <a name="b--double"></a>b: [dubbel](xref:microsoft.quantum.lang-ref.double)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als `a` bijna gelijk is aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```