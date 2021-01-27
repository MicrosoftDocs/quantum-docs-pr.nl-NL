---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: De functie NearEqualityFactD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: d632a7a12c9ebbebfbc7939f2b8a24de8ae1ba2a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827894"
---
# <a name="nearequalityfactd-function"></a>De functie NearEqualityFactD

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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