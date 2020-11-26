---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: Bewerking ApplyXorInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210108"
---
# <a name="applyxorinplace-operation"></a>Bewerking ApplyXorInPlace

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een Bitsgewijze-XOR-bewerking toe tussen een klassiek geheel getal en een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
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

