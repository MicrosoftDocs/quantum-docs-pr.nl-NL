---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Bewerking MultiplyI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 96922f0147788b37cc9bace5154288a722d4ba95
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222504"
---
# <a name="multiplyi-operation"></a>Bewerking MultiplyI

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Vermenigvuldig het geheel getal `xs` met een geheel getal `ys` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bits multiplicand (LittleEndian)


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bits vermenigvuldiger (LittleEndian)


### <a name="result--littleendian"></a>resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Maakt gebruik van een standaard methode voor Shift en toevoegen om de vermenigvuldiging te implementeren.
De gecontroleerde versie is verbeterd door $x _i $ te kopiëren naar een ancilla Qubit die is voor bereid op het besturings element qubits en vervolgens de toevoeging van de ancilla Qubit te beheren.