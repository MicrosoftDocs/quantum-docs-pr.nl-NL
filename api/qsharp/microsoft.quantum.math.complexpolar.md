---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Door de gebruiker gedefinieerd ComplexPolar-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: a4f3a7b6ffa73271d7ac9674d8c718f6f09c0291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210978"
---
# <a name="complexpolar-user-defined-type"></a>Door de gebruiker gedefinieerd ComplexPolar-type

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een complex getal in polaire vorm.

De polaire weer gave van een complex getal is $c = r e ^ {i t} $.

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a>Benoemde items

### <a name="magnitude--double"></a>Grootte: [dubbel](xref:microsoft.quantum.lang-ref.double)

De absolute waarde $r \ge $0 van $c $.
### <a name="argument--double"></a>Argument: [Double](xref:microsoft.quantum.lang-ref.double)

De fase $t \in \mathbb R $ van $c $.