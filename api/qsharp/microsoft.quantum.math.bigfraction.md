---
uid: Microsoft.Quantum.Math.BigFraction
title: Door de gebruiker gedefinieerd BigFraction-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708311"
---
# <a name="bigfraction-user-defined-type"></a>Door de gebruiker gedefinieerd BigFraction-type

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een rationeel nummer van het formulier `p/q` . Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Benoemde items

### <a name="numerator--bigint"></a>Teller: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De teller van de Fractie.
### <a name="denominator--bigint"></a>Noemer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Noemer van de Fractie/