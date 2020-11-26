---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: De functie LocalUnivariateMinimum
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: e804e6a6ed82f14dcc9b8f721ad503d77922dc0f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194080"
---
# <a name="localunivariateminimum-function"></a>De functie LocalUnivariateMinimum

Naam ruimte: [micro soft. Quantum. Optimization](xref:Microsoft.Quantum.Optimization)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert het lokale minimum voor een univariate-functie gedurende een beperkt interval, met behulp van een gouden interval zoekactie.

```qsharp
function LocalUnivariateMinimum (fn : (Double -> Double), bounds : (Double, Double), tolerance : Double) : Microsoft.Quantum.Optimization.UnivariateOptimizationResult
```


## <a name="input"></a>Invoer

### <a name="fn--double---double"></a>FN: [dubbele](xref:microsoft.quantum.lang-ref.double) -> [dubbele precisie](xref:microsoft.quantum.lang-ref.double)

De functie univariate die moet worden geminimaliseerd.


### <a name="bounds--doubledouble"></a>grenzen: ([dubbel](xref:microsoft.quantum.lang-ref.double),[dubbel](xref:microsoft.quantum.lang-ref.double))

Het interval waarin het lokale minimum moet worden gevonden.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De nauw keurigheid van de functie-invoer die moet worden toegestaan.
De zoek actie naar lokale Optima by wordt voortgezet totdat het interval kleiner is dan deze tolerantie.



## <a name="output--univariateoptimizationresult"></a>Uitvoer: [UnivariateOptimizationResult](xref:Microsoft.Quantum.Optimization.UnivariateOptimizationResult)

Een lokale optimais van de opgegeven functie, die zich binnen de opgegeven grenzen bevindt.