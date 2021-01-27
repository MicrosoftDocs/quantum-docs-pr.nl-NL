---
uid: Microsoft.Quantum.Diagnostics.Fact
title: De functie faculteit
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Fact
qsharp.summary: Declares that a classical condition is true.
ms.openlocfilehash: 8e86000f04c01040d420c2f682fc1b4ccf35cf39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853308"
---
# <a name="fact-function"></a>De functie faculteit

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Declareert dat een klassieke voor waarde waar is.

```qsharp
function Fact (actual : Bool, message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--bool"></a>werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De voor waarde die moet worden gedeclareerd.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Fout bericht teken reeks die moet worden afgedrukt in het geval dat de klassieke voor waarde ONWAAR is.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

De volgende Q #-fragment kan mislukken:

```qsharp
Fact(false, "Expected true.");
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. tegen strijdige](xref:Microsoft.Quantum.Diagnostics.Contradiction)