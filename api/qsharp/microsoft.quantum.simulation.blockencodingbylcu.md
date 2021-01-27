---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: De functie BlockEncodingByLCU
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 1d7890e96513817c127ef768f49c0b915ea22fa1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858164"
---
# <a name="blockencodingbylcu-function"></a>De functie BlockEncodingByLCU

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codeert een operator van belang in een `BlockEncoding` .

Hiermee wordt een `BlockEncoding` unitary $U = P\cdot V\cdot P ^ \dagger $ waarmee een bepaalde operator wordt gecodeerd $H = \ sum_ {j} | \ alpha_j | U_j $ van belang dat een lineaire combi natie is van unitaries. Normaal gesp roken is $P $ een status voorbereiding unitary, zodat $P \ket {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ en $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="statepreparation--t--unit--is-adj--ctl"></a>statePreparation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een unitary $P $ die een bepaalde doel status voorbereidt.


### <a name="selector--ts--unit--is-adj--ctl"></a>kiezer: ('T) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een unitary $V $ waarmee het onderdeel unitaries van $H $ wordt gecodeerd.



## <a name="output--ts--unit--is-adj--ctl"></a>Output: ('T) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een unitary $U $ communiceert gezamenlijk aan registers `a` en `s` die blok-coderingen $H $, en voldoet aan $U ^ \Dagger = U $.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="s"></a>Maatschappij



## <a name="remarks"></a>Opmerkingen

Deze `BlockEncoding` implementatie geeft de eigenschappen van een `BlockEncodingReflection` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Micro soft. Quantum. simulatie. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)