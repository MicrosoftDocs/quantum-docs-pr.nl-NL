---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: Bewerking R1Frac
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfae01d11524f64ceebd53aa8544d7ea48c40f31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818688"
---
# <a name="r1frac-operation"></a>Bewerking R1Frac

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Past een rotatie over de $ \ket {1} $-status toe met een hoek die is opgegeven als een dyadic-Fractie.

\begin{align} R_1 (n, k) \mathrel{: =} \operatorname{diag} (1, e ^ {i \pi k/2 ^ n}).
\end{align}

> [!WARNING]
> Deze bewerking maakt gebruik van de **tegenovergestelde** teken Conventie van en bevat @"microsoft.quantum.intrinsic.r" niet de factor $1/2 $, opgenomen door @"microsoft.quantum.intrinsic.r1" .

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="numerator--int"></a>teller: [int](xref:microsoft.quantum.lang-ref.int)

De teller in de dyadic-weer gave van de hoek waarmee de Qubit moet worden gedraaid.


### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Kracht van twee opgeven van de noemer van de hoek waarmee de Qubit moet worden gedraaid.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit waarop de Gate moet worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Gelijk aan:

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```