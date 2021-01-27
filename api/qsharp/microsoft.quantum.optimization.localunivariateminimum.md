---
uid: Microsoft.Quantum.Optimization.LocalUnivariateMinimum
title: De functie LocalUnivariateMinimum
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Optimization
qsharp.name: LocalUnivariateMinimum
qsharp.summary: Returns the local minimum for a univariate function over a bounded interval, using a golden interval search.
ms.openlocfilehash: c2d094a6d0e0c7cecb249cd517995e11dff3d3b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854598"
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