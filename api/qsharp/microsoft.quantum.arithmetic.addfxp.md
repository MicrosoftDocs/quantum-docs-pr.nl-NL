---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Bewerking AddFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: cf1f1379b7e1c32aefb0fccb55f4d13c95c78d8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707661"
---
# <a name="addfxp-operation"></a>Bewerking AddFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Telt twee vaste-komma nummers op die zijn opgeslagen in Quantum registers.

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="description"></a>Beschrijving

In de Staten $ \ket{f_1} $ en $ \ket{f_2} $, voert de bewerking $ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $ uit op twee vaste-punt registreren.

## <a name="input"></a>Invoer

### <a name="fp1--fixedpoint"></a>FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Eerste getal met vaste komma


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Het tweede getal met vaste komma wordt bijgewerkt met de som van de twee invoer waarden.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De huidige implementatie vereist dat de twee vaste-komma waarden dezelfde punt positie hebben ten opzichte van de minst significante bit, d.w.z. $n _i $ en $p _i $ gelijk moet zijn.