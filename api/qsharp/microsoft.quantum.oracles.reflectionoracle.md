---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Door de gebruiker gedefinieerd ReflectionOracle-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 8e35e7e508ea7e0c30ea2a70633f71a6c87d4be1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708742"
---
# <a name="reflectionoracle-user-defined-type"></a>Door de gebruiker gedefinieerd ReflectionOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een weer spiegeling van Oracle.

Een reflectie-Oracle, $O $, heeft invoer:

- De fase $ \phi $ waarmee de doorgevoerde subruimte wordt gedraaid.
- Het Qubit-REGI ster waarop de opgegeven reflectie moet worden uitgevoerd.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Benoemde items

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a>ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL



## <a name="remarks"></a>Opmerkingen

Deze Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ voert een gedeeltelijke reflectie uit op basis van een fase $ \phi $ over één zuivere status $ \ket{\psi} $.