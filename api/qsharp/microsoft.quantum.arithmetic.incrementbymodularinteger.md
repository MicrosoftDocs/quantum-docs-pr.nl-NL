---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Bewerking IncrementByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707261"
---
# <a name="incrementbymodularinteger-operation"></a>Bewerking IncrementByModularInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Voert een modulaire verhoging van een Qubit-REGI ster uit met een constante van een geheel getal.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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