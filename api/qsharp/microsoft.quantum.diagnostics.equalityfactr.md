---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: De functie EqualityFactR
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 86d2ddff79f0bca7badd95a2fe2156c558fa7f86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853334"
---
# <a name="equalityfactr-function"></a>De functie EqualityFactR

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bevestiging dat een klassieke resultaat variabele de verwachte waarde heeft.

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--__invalidresult__"></a>werkelijk: __ongeldig <Result>__

De variabele die moet worden gecontroleerd.


### <a name="expected--__invalidresult__"></a>verwacht: __ongeldig <Result>__

De verwachte waarde.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Fout bericht teken reeks die moet worden gebruikt wanneer de bevestiging wordt geactiveerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

