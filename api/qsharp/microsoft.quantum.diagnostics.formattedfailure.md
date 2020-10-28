---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: De functie FormattedFailure
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702627"
---
# <a name="formattedfailure-function"></a>De functie FormattedFailure

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Interne functie die wordt gebruikt om te mislukken met zinvolle fout berichten.

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--t"></a>werkelijk: 'T




### <a name="expected--t"></a>verwacht: ' 'T




### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

Deze functie is bedoeld om te worden geëmuleerd door simulatie runtimes, zodat het door sturen van opgemaakte tegen strijdigheden toestaat.