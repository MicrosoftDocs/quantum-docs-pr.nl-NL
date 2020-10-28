---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: De functie IntegerBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706428"
---
# <a name="integerbits-function"></a>De functie IntegerBits

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket [](https://nuget.org/packages/)


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