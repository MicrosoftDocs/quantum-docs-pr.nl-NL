---
uid: Microsoft.Quantum.Synthesis.Extended
title: Uitgebreide functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855477"
---
# <a name="extended-function"></a>Uitgebreide functie

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Breidt een spectrum uit door omgedraaide coëfficiënten

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a>Invoer

### <a name="spectrum--int"></a>spectrum: [int](xref:microsoft.quantum.lang-ref.int)[]

Spectral coëfficiënten



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Coëfficiënten gevolgd door een omgekeerde kopie

## <a name="example"></a>Voorbeeld

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```