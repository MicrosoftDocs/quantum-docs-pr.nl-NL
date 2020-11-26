---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Bewerking IncrementByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 8a02d22facce8f58180752b6d063ac55d75ca537
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222946"
---
# <a name="incrementbymodularinteger-operation"></a>Bewerking IncrementByModularInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert een modulaire verhoging van een Qubit-REGI ster uit met een constante van een geheel getal.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Laat het ons weten door `increment` $a $ `modulus` door $N $ en een geheel getal dat is gecodeerd in `target` $y $.
De bewerking voert vervolgens de volgende trans formatie uit: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} gehele getallen worden gecodeerd in de indeling little-endian.

## <a name="input"></a>Invoer

### <a name="increment--int"></a>interval: [int](xref:microsoft.quantum.lang-ref.int)

Geheel getal $a $ dat moet worden toegevoegd aan $y $.


### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)

Geheel getal $N $ dat modules $y + a $.


### <a name="target--littleendian"></a>doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Geheel getal $y $ in `LittleEndian` indeling waaraan `increment` $a $ is toegevoegd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Er wordt van uitgegaan dat de aanvankelijke waarde van target kleiner is dan $N $ en dat de verhoging $a $ kleiner is dan $N $.
Houd er rekening mee dat <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> dezelfde bewerking in de `PhaseLittleEndian` basis wordt geïmplementeerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. IncrementPhaseByModularInteger](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)