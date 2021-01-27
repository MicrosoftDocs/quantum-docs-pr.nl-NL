---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: De functie TrotterStepSize
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840079"
---
# <a name="trotterstepsize-function"></a>De functie TrotterStepSize

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berekent Trotter-stap grootte in recursieve implementatie van Trotter simulatie algoritme.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="order--int"></a>Volg orde: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Opmerkingen

Deze bewerking maakt gebruik van een andere indexerings Conventie dan die van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139). `DecomposedIntoTimeStepsCA(_, 4)`Met name overeenkomt met het scalaire $p _2 (\lambda) $ in Quant-pH/0508139.