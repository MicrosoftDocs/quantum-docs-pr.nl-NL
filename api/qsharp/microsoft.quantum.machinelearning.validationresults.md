---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Door de gebruiker gedefinieerd ValidationResults-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 42bfab7fd1f9372d9394f2eaf2d698b39b4307e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211488"
---
# <a name="validationresults-user-defined-type"></a>Door de gebruiker gedefinieerd ValidationResults-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


De resultaten van het valideren van een classificatie op basis van een reeks voor beelden.

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="nmisclassifications--int"></a>NMisclassifications: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal misclassificaties dat tijdens de validatie wordt waargenomen.
### <a name="nvalidationsamples--int"></a>NValidationSamples: [int](xref:microsoft.quantum.lang-ref.int)

