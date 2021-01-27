---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Bewerking RippleCarryAdderCDKM
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: df9b62b649af532a4202aacc3e8dd4613eb8665d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846365"
---
# <a name="ripplecarryaddercdkm-operation"></a>Bewerking RippleCarryAdderCDKM

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Omkeerbaar, in-place rimpels, toevoeging van twee gehele getallen.

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als er twee $n $-bitsinteger-waarden zijn gecodeerd in LittleEndian-registers `xs` en `ys` , en een Qubit-overdracht, berekent de bewerking de som van de twee gehele getallen waarbij de $n $ minst significante bits van het resultaat worden vastgehouden in en de verwerkings- `ys` bit is xored aan de Qubit `carry` .

## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit registreert de eerste integer summand.


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian Qubit registreren code ring de tweede integer summand, wordt aangepast om de n minst significante bits van de som op te slaan.


### <a name="carry--qubit"></a>overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, is xored met de meest significante bit van de som.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Deze bewerking heeft dezelfde functionaliteit als RippleCarryAdderD, maar gebruikt slechts één hulp Qubit in plaats van $n $.

## <a name="references"></a>Verwijzingen

- Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1