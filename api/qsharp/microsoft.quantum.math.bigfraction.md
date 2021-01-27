---
uid: Microsoft.Quantum.Math.BigFraction
title: Door de gebruiker gedefinieerd BigFraction-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: bfbf49e7a3d060417e506a1977c20adc08b81f0e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846901"
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