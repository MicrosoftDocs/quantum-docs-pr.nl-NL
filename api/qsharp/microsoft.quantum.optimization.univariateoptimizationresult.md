---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Door de gebruiker gedefinieerd UnivariateOptimizationResult-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: c8aa91bbdc9e9e9bb4d110b470ff2041f9460a38
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708790"
---
# <a name="univariateoptimizationresult-user-defined-type"></a>Door de gebruiker gedefinieerd UnivariateOptimizationResult-type

Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Pakket [](https://nuget.org/packages/)


Hiermee wordt het resultaat van het optimaliseren van een univariate-functie aangeduid.

```qsharp

newtype UnivariateOptimizationResult = (Coordinate : Double, Value : Double);
```



## <a name="named-items"></a>Benoemde items

### <a name="coordinate--double"></a>Coördinaat: [dubbel](xref:microsoft.quantum.lang-ref.double)

Invoer waarbij een optimale bevinding is gevonden.
### <a name="value--double"></a>Waarde: [Double](xref:microsoft.quantum.lang-ref.double)

De waarde die is geretourneerd door de functie is optimaal.