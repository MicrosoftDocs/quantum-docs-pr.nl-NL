---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Bewerking IncrementPhaseByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 6a39ce49dfa28c1f1cbe6b29e526144c3ac19e53
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222878"
---
# <a name="incrementphasebymodularinteger-operation"></a>Bewerking IncrementPhaseByModularInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert een modulaire verhoging van een Qubit-REGI ster uit met een constante van een geheel getal.

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Laat het ons weten door `increment` $a $ `modulus` door $N $ en een geheel getal dat is gecodeerd in `target` $y $.
De bewerking voert vervolgens de volgende trans formatie uit: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} gehele getallen worden in QFT gebaseerd in de indeling little endian.

## <a name="input"></a>Invoer

### <a name="increment--int"></a>interval: [int](xref:microsoft.quantum.lang-ref.int)

Geheel getal $a $ dat moet worden toegevoegd aan $y $.


### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)

Geheel getal $N $ dat modules $y + a $.


### <a name="target--phaselittleendian"></a>doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Geheel getal $y $ in een indeling die uit een Phase-code is versleuteld `increment` en waaraan $a $ is toegevoegd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Er wordt van uitgegaan dat `target` de hoogste bit is ingesteld op 0.
Er wordt ook van uitgegaan dat de waarde van target kleiner is dan $N $.

Zie afbeelding 5 op [pagina 5 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5)voor het circuit diagram en de uitleg.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. IncrementByModularInteger](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)