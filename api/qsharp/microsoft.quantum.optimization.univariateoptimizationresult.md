---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Door de gebruiker gedefinieerd UnivariateOptimizationResult-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: 0bcdbda5586181f965297cb2a398d766f9c6fabb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194029"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Door de gebruiker gedefinieerd UnivariateOptimizationResult-type

Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt het resultaat van het optimaliseren van een univariate-functie aangeduid.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Benoemde items

### <a name="coordinate--double"></a>Coördinaat: [dubbel](xref:microsoft.quantum.lang-ref.double)

Invoer waarbij een optimale bevinding is gevonden.
### <a name="value--double"></a>Waarde: [Double](xref:microsoft.quantum.lang-ref.double)

De waarde die is geretourneerd door de functie is optimaal.