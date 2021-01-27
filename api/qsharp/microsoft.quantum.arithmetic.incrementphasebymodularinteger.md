---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Bewerking IncrementPhaseByModularInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 4ba35010d56ad01c73cb563646dc8150842da12e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846581"
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