---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Bewerking MultiplyAndAddByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706404"
---
# <a name="multiplyandaddbymodularinteger-operation"></a>Bewerking MultiplyAndAddByModularInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Voert een modulaire vermenigvuldiging en toevoegen door gehele getallen in een Qubit-REGI ster.

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Beschrijving

Implementeert de kaart $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $ $ voor een gegeven modulus $N $, constante multiplier $a $ en summand $y $.

## <a name="input"></a>Invoer

### <a name="constmultiplier--int"></a>constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal $a $ dat moet worden toegevoegd aan elk basis status label.


### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)

De modulus $N $ die optellen en vermenigvuldigen met betrekking tot.


### <a name="multiplier--littleendian"></a>vermenigvuldiger: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt waarvan de waarde moet worden toegevoegd aan elk basis status label van `summand` .


### <a name="summand--littleendian"></a>summand: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt dat moet worden gebruikt als doel voor deze bewerking.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

- Zie afbeelding 6 op [pagina 7 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7) voor het circuit diagram en de uitleg.
- Deze bewerking komt overeen met CMULT (a) MOD (N) in [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. MultiplyAndAddPhaseByModularInteger](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)