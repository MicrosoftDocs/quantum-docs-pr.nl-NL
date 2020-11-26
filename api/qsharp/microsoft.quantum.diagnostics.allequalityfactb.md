---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: De functie AllEqualityFactB
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 79dcf65956ba9436fb6fdd452f22f35d4852d6f8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213698"
---
# <a name="allequalityfactb-function"></a>De functie AllEqualityFactB

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

