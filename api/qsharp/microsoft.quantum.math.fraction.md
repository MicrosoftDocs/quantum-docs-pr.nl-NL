---
uid: Microsoft.Quantum.Math.Fraction
title: Door de gebruiker gedefinieerd type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210672"
---
# <a name="fraction-user-defined-type"></a>Door de gebruiker gedefinieerd type

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een rationeel nummer van het formulier `p/q` . Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="numerator--int"></a>Teller: [int](xref:microsoft.quantum.lang-ref.int)

De teller van de Fractie.
### <a name="denominator--int"></a>Noemer: [int](xref:microsoft.quantum.lang-ref.int)

Noemer van de Fractie/