---
uid: Microsoft.Quantum.Math.BigFraction
title: Door de gebruiker gedefinieerd BigFraction-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1c9b9e350c4fa3664b2c66da05149005b1170ec3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211080"
---
# <a name="bigfraction-user-defined-type"></a>Door de gebruiker gedefinieerd BigFraction-type

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een rationeel nummer van het formulier `p/q` . Geheel getal `p` is het eerste element van de tuple en `q` is het tweede element van de tuple.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Benoemde items

### <a name="numerator--bigint"></a>Teller: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De teller van de Fractie.
### <a name="denominator--bigint"></a>Noemer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Noemer van de Fractie/