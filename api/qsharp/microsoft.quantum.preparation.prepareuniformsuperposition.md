---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Bewerking PrepareUniformSuperposition
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 8b57a7a02e9f704cf9677574824dfdc93fff25b0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701247"
---
# <a name="prepareuniformsuperposition-operation"></a>Bewerking PrepareUniformSuperposition

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket [](https://nuget.org/packages/)


Hiermee maakt u een uniforme superpositie op status die 0 t/m-codeert `nIndices - 1` .

Dat wil zeggen dat deze unitary $U $ een uniforme superpositie maakt boven alle nummer Staten $0 $ tot $M-$1, op basis van een invoer status $ \ket{0\cdots 0} $. Met andere woorden, $ $ \begin{align} U\ket {0} = \frac {1} {\sqrt{m}}\ sum_ {j = 0} ^ {M-1} \ket{j}.
\end{align} $ $.

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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