---
uid: Microsoft.Quantum.Math.Fraction
title: Door de gebruiker gedefinieerd type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a56d28e34938729a8e4ffda5f870e0b6a25be017
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857519"
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