---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Bewerking MultiplyAndAddPhaseByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: be7df50f040697329c2fe8bbc319c8cebb8b2687
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706397"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a>Bewerking MultiplyAndAddPhaseByModularInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Hetzelfde als MultiplyAndAddByModularInteger, maar er wordt van uitgegaan dat de summand integers codeert in QFT.

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a>Invoer

### <a name="constmultiplier--int"></a>constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal $a $ dat moet worden toegevoegd aan elk basis status label.


### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)

De modulus $N $ die optellen en vermenigvuldigen met betrekking tot.


### <a name="multiplier--littleendian"></a>vermenigvuldiger: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt waarvan de waarde moet worden toegevoegd aan elk basis status label van `summand` .


### <a name="phasesummand--phaselittleendian"></a>phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt dat moet worden gebruikt als doel voor deze bewerking.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Er wordt van uitgegaan dat `phaseSummand` de hoogste bit is ingesteld op 0.
Er wordt ook van uitgegaan dat de waarde van `phaseSummand` kleiner is dan $N $.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. MultiplyAndAddByModularInteger](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)