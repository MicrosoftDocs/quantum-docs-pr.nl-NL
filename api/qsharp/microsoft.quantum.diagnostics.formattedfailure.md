---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: De functie FormattedFailure
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: da809c04059d4fd0f0ec92412a3094f5b582fd91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201696"
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