---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Door de gebruiker gedefinieerd ComplexPolar-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701330"
---
# <a name="complexpolar-user-defined-type"></a>Door de gebruiker gedefinieerd ComplexPolar-type

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


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