---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Gecodeerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855484"
---
# <a name="encoded-function"></a>Gecodeerde functie

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een waarheids tabel coderen in {1,-1} code ring

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a>Invoer

### <a name="table--bool"></a>tabel: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Waarheids tabel als een matrix met waarheids waarden



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Tabel met waarheid als matrix van {1,-1} gehele getallen

## <a name="example"></a>Voorbeeld

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```