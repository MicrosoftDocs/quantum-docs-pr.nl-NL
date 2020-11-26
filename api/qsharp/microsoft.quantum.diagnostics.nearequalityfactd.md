---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: De functie NearEqualityFactD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5acfe5043342fd88276910a9fd0347f7d2f6960f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201509"
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