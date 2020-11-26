---
uid: Microsoft.Quantum.Intrinsic.H
title: H-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: H
qsharp.summary: >-
  Applies the Hadamard transformation to a single qubit.

  \begin{align} H \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}. \end{align}
ms.openlocfilehash: 6f02390588c9de38f69802575429aff749f70ac5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212372"
---
# <a name="h-operation"></a>H-bewerking

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Hiermee wordt de Hadamard-trans formatie toegepast op één Qubit.

\begin{align} H \mathrel{: =} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ &-1 \end{bmatrix}.
\end{align}

```qsharp
operation H (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit waarop de Gate moet worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

