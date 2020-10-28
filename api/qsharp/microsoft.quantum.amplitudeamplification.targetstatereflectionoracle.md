---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: De functie TargetStateReflectionOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: a6ed0397be57ef6f14a712749cc416e1fd98b71c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707675"
---
# <a name="targetstatereflectionoracle-function"></a>De functie TargetStateReflectionOracle

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Bouwt `ReflectionOracle` over de doel status die uniek is gemarkeerd door de vlag Qubit.

Voor de doel status is één Qubit ingesteld op 1 en alle andere 0: $ \ket {1} _f $.

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a>Invoer

### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

Index om Qubit $f $ van Oracle te markeren.



## <a name="output--reflectionoracle"></a>Uitvoer: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Een `ReflectionOracle` die overeenkomt met de status die is gemarkeerd door $ \ket {1} _f $.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ReflectionOracle](xref:Microsoft.Quantum.Canon.ReflectionOracle)