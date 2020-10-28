---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: De functie AllEqualityFactB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 100aacccbfd5b45ac9f859cd89424b0ed4007f72
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702800"
---
# <a name="allequalityfactb-function"></a>De functie AllEqualityFactB

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Hierbij wordt bevestigd dat twee matrices van Boole-waarden gelijk zijn.

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--bool"></a>werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

De matrix die wordt geproduceerd door een test case.


### <a name="expected--bool"></a>verwacht: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

De matrix die wordt verwacht van een test geval van belang.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat moet worden afgedrukt als de matrices niet gelijk zijn.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

