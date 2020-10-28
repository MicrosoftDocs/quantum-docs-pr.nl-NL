---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Bewerking CarryOutCoreCDKM
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 6a292e66f6d9911d2a9075f6397f4f5ba97ec64d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707397"
---
# <a name="carryoutcorecdkm-operation"></a>Bewerking CarryOutCoreCDKM

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


De kern bewerking in de RippleCarryAdderCDKM die wordt gebruikt met de bovenstaande ApplyOuterCDKMAdder-bewerking, dat wil zeggen met deze bewerking, om de binnenste bewerking van de RippleCarryAdderCDKM te verkrijgen. Met deze bewerking wordt het uitvoeren van Qubit berekend en wordt een reeks van niet-poorten toegepast op een deel van de invoer `ys` .

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Eerste Qubit-REGI ster.


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Tweede Qubit-REGI ster.


### <a name="ancilla--qubit"></a>ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De ancilla-Qubit die wordt gebruikt in RippleCarryAdderCDKM die is door gegeven aan deze bewerking.


### <a name="carry--qubit"></a>overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Voer Qubit uit in de RippleCarryAdderCDKM-bewerking.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

- Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1