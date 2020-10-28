---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: De functie EqualityWithinToleranceFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702657"
---
# <a name="equalitywithintolerancefact-function"></a>De functie EqualityWithinToleranceFact

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt de claim die een klassieke drijvende-komma waarde de verwachte waarde heeft tot een gegeven absolute tolerantie.

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--double"></a>werkelijk: [dubbel](xref:microsoft.quantum.lang-ref.double)

Het getal dat moet worden gecontroleerd.


### <a name="expected--double"></a>verwacht: [Double](xref:microsoft.quantum.lang-ref.double)

De verwachte waarde.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Absolute tolerantie voor het verschil tussen werkelijk en verwacht.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

