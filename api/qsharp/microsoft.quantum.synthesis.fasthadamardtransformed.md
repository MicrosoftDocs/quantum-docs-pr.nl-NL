---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: De functie FastHadamardTransformed
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855456"
---
# <a name="fasthadamardtransformed-function"></a>De functie FastHadamardTransformed

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de Hadamard-trans formatie van een Boole-functie in {-1,1} code ring berekend met behulp van de methode van Yates

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a>Invoer

### <a name="func--int"></a>FUNC: [int](xref:microsoft.quantum.lang-ref.int)[]

Waarheids tabel in {-1,1} code ring



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Spectral coëfficiënten van de functie

## <a name="example"></a>Voorbeeld

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```