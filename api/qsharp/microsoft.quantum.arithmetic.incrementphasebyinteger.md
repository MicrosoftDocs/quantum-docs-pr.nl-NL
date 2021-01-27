---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Bewerking IncrementPhaseByInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843150"
---
# <a name="incrementphasebyinteger-operation"></a>Bewerking IncrementPhaseByInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Verhoogt een niet-ondertekend Quantum register met een klassiek geheel getal, met behulp van fase rotaties.

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Stel dat `target` een niet-ondertekend geheel getal $x $ in een code ring van little-endian wordt gecodeerd en `increment` gelijk is aan $a $.
Deze bewerking implementeert vervolgens de unitary $ \ket{x} \mapsto \ket{x + a} $, waarbij de aanvulling wordt uitgevoerd modulo $2 ^ n $, waarbij $n = \texttt{Length (doel!)} $.

## <a name="input"></a>Invoer

### <a name="increment--int"></a>interval: [int](xref:microsoft.quantum.lang-ref.int)

Het gehele getal waarmee de `target` wordt verhoogd.


### <a name="target--phaselittleendian"></a>doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Een Quantum register codeert een niet-ondertekend geheel getal met behulp van code ring van Little Endian in de Dual (QFT) basis.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Houd er rekening mee dat het circuit is vereenvoudigd omdat de verhoging een klassieke constante is, geen Quantum registratie.

Zie de afbeelding op [ pagina 6 van arXiv: Quant-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) voor het circuit diagram en de uitleg.

## <a name="references"></a>Verwijzingen

- [*Thomas G. Draper*, arXiv: Quant-pH/0008033](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. IncrementByInteger](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)