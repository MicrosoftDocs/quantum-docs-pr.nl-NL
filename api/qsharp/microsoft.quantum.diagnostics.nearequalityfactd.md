---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: De functie NearEqualityFactD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702615"
---
# <a name="nearequalityfactd-function"></a>De functie NearEqualityFactD

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Hierbij wordt bevestigd dat een klassieke drijvende-komma waarde de verwachte waarde heeft tot een kleine tolerantie van 1e-10.

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--double"></a>werkelijk: [dubbel](xref:microsoft.quantum.lang-ref.double)

Het getal dat moet worden gecontroleerd.


### <a name="expected--double"></a>verwacht: [Double](xref:microsoft.quantum.lang-ref.double)

De verwachte waarde.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Dit komt overeen <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> met een hardcoded tolerantie van $10 ^ {-10} $.