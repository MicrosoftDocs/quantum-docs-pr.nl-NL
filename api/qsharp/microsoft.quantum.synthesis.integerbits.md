---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: De functie IntegerBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855407"
---
# <a name="integerbits-function"></a>De functie IntegerBits

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert alle posities waarin bits van een geheel getal zijn ingesteld.

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a>Invoer

### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)

Een niet-negatief getal.


### <a name="length--int"></a>lengte: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits in de binaire uitbrei ding van `value` .



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix met alle bits-posities (vanaf 0) die 1 zijn in de binaire uitbrei ding van het `value` overwegen van alle bits tot stand te brengen `length - 1` .  Alle posities worden in de matrix gesorteerd op positie in een oplopende volg orde.

## <a name="example"></a>Voorbeeld

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```