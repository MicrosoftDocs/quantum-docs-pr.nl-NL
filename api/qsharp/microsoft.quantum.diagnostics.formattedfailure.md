---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: De functie FormattedFailure
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 6b1202c8897d67e3089a88a0855c8008b3a8c2ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828278"
---
# <a name="formattedfailure-function"></a>De functie FormattedFailure

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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