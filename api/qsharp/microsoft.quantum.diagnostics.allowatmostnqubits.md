---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Bewerking AllowAtMostNQubits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: ddbed96df0d95cfd78730c091a6a81ee6e49c349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702789"
---
# <a name="allowatmostnqubits-operation"></a>Bewerking AllowAtMostNQubits

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Tussen een aanroep van deze bewerking en de adjoint, wordt met behulp van-instructies gecontroleerd of er Maxi maal een gegeven aantal extra qubits is toegewezen.

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het maximum aantal qubits dat kan worden toegewezen.


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.