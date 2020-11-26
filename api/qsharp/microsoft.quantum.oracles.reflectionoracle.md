---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Door de gebruiker gedefinieerd ReflectionOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226652"
---
# <a name="reflectionoracle-user-defined-type"></a>Door de gebruiker gedefinieerd ReflectionOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een weer spiegeling van Oracle.

Een reflectie-Oracle, $O $, heeft invoer:

- De fase $ \phi $ waarmee de doorgevoerde subruimte wordt gedraaid.
- Het Qubit-REGI ster waarop de opgegeven reflectie moet worden uitgevoerd.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benoemde items

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a>ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL



## <a name="remarks"></a>Opmerkingen

Deze Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ voert een gedeeltelijke reflectie uit op basis van een fase $ \phi $ over één zuivere status $ \ket{\psi} $.