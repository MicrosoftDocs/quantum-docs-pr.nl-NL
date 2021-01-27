---
uid: Microsoft.Quantum.Optimization.UnivariateOptimizationResult
title: Door de gebruiker gedefinieerd UnivariateOptimizationResult-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: UnivariateOptimizationResult
qsharp.summary: Represents the result of optimizing a univariate function.
ms.openlocfilehash: cc54c0035796aac86482e8a3a6896ceb197c7cfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854572"
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