---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Bewerking PrepareUniformSuperposition
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230086"
---
# <a name="prepareuniformsuperposition-operation"></a>Bewerking PrepareUniformSuperposition

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee maakt u een uniforme superpositie op status die 0 t/m-codeert `nIndices - 1` .

Dat wil zeggen dat deze unitary $U $ een uniforme superpositie maakt boven alle nummer Staten $0 $ tot $M-$1, op basis van een invoer status $ \ket{0\cdots 0} $. Met andere woorden, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.
\end{align} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="nindices--int"></a>nIndices: [int](xref:microsoft.quantum.lang-ref.int)

Het gewenste aantal statussen $M $ in de uniforme superpositie.


### <a name="indexregister--littleendian"></a>indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het Qubit-REGI ster waarin de nummer Staten worden opgeslagen in de `LittleEndian` indeling.
In dit REGI ster moet het getal $M-$1 worden opgeslagen en wordt ervan uitgegaan dat het is geïnitialiseerd in de status $ \ket{0\cdots 0} $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De bewerking is adjointable, maar vereist dat `indexRegister` zich in een uniforme superpositie bevindt `nIndices` in de eerste basis status in dat geval.