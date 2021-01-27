---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Door de gebruiker gedefinieerd ComplexPolar-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 174e75b82a3ee740cd4d07e5bcd091de65bbc6b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847348"
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