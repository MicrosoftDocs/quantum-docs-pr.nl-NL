---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Sum-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: e659c77a876e10df75f28ca1798fb0335e1bfb22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847759"
---
# <a name="sum-operation"></a>Sum-bewerking

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementeert een onomkeerbaare Sum-poort. Een door Voer in Qubit `carryIn` en twee summand bits `summand1` die zijn gecodeerd in en `summand2` , berekent de Bitsgewijze XOR van en `carryIn` `summand1` `summand2` in de Qubit `summand2` .

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="carryin--qubit"></a>carryIn: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit uitvoeren.


### <a name="summand1--qubit"></a>summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eerste summand Qubit.


### <a name="summand2--qubit"></a>summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Tweede summand Qubit wordt vervangen door de laagste bit van de som van `summand1` en `summand2` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

In tegens telling tot de `Carry` bewerking, wordt de verwerkings bit niet berekend.