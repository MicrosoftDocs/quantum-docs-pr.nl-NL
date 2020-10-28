---
uid: Microsoft.Quantum.Math.Fraction
title: Door de gebruiker gedefinieerd type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708503"
---
# <a name="fraction-user-defined-type"></a>Door de gebruiker gedefinieerd type

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een rationeel nummer van het formulier `p/q` . Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="numerator--int"></a>Teller: [int](xref:microsoft.quantum.lang-ref.int)

De teller van de Fractie.
### <a name="denominator--int"></a>Noemer: [int](xref:microsoft.quantum.lang-ref.int)

Noemer van de Fractie/