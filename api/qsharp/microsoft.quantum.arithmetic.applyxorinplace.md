---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Bewerking ApplyXorInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 5a35abc16a967e64c84466a47844ed7beeb618dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707460"
---
# <a name="applyxorinplace-operation"></a>Bewerking ApplyXorInPlace

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Past een Bitsgewijze-XOR-bewerking toe tussen een klassiek geheel getal en een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Beschrijving

Hiermee `X` worden bewerkingen toegepast op qubits in een little-endian-REGI ster op basis van 1 bits in een geheel getal.

Laat het ons weten `value` en laat y een niet-ondertekend geheel getal dat is gecodeerd in en `target` `InPlaceXorLE` voert een bewerking uit die wordt gegeven door de volgende kaart: $ \ket{y}\rightarrow \ket{y\oplus a} $, waarbij $ \oplus $ de bitsgewijze exclusieve OR-operator is.

## <a name="input"></a>Invoer

### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal dat wordt beschouwd als niet-negatief.


### <a name="target--littleendian"></a>doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een Quantum register dat wordt gebruikt voor het opslaan `value` van de code ring met little endian.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

