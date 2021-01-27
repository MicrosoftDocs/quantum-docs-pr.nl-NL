---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Functie tegen strijdigheid
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: 7d62c9341b768dfdfbfbf8e73e64748f04317595
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829369"
---
# <a name="contradiction-function"></a>Functie tegen strijdigheid

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Declareert dat een klassieke voor waarde ONWAAR is.

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="actual--bool"></a>werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De voor waarde die moet worden gedeclareerd.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Fout bericht teken reeks die moet worden afgedrukt in het geval dat de klassieke voor waarde waar is.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

Met de volgende Q #-code wordt "Hallo, wereld" afgedrukt:

```qsharp
Contradiction(2 == 3, "2 is not equal to 3.");
Message("Hello, world.");
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. fact](xref:Microsoft.Quantum.Diagnostics.Fact)