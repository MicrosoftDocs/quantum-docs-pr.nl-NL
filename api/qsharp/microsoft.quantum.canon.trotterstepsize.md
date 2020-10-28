---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: De functie TrotterStepSize
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: fabfbff74572b3c96c701de5443e4265a0468d78
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703719"
---
# <a name="trotterstepsize-function"></a>De functie TrotterStepSize

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Berekent Trotter-stap grootte in recursieve implementatie van Trotter simulatie algoritme.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="order--int"></a>Volg orde: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Opmerkingen

Deze bewerking maakt gebruik van een andere indexerings Conventie dan die van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139). `DecomposedIntoTimeStepsCA(_, 4)`Met name overeenkomt met het scalaire $p _2 (\lambda) $ in Quant-pH/0508139.