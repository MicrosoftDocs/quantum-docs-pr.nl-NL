---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Bewerking RippleCarryAdderNoCarryTTK
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 0e131204d3eaff7f99aa9ff7c3c1ae93a1bf611b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846348"
---
# <a name="ripplecarryaddernocarryttk-operation"></a>Bewerking RippleCarryAdderNoCarryTTK

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Omkeerbaar, in-place rimpels, waarbij twee gehele getallen worden toegevoegd zonder dat ze worden uitgevoerd.

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , berekent de bewerking de som van de twee gehele getallen modulo $2 ^ n $, waarbij $n $ de bitlengte is van de invoer `xs` en `ys` . De verwerkings bit wordt niet berekend.

## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit registreert de eerste integer summand.


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit registreren code ring de tweede integer summand is gewijzigd in de $n $ minst significante bits van de som.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderTTK, maar retourneert niet de draag bit.

## <a name="references"></a>Verwijzingen

- Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.
  https://arxiv.org/abs/0910.2530