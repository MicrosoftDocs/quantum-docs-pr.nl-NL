---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Bewerking MeasureIdentity
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 71a103fddb3a27703318975bea94bc7a22a9ce81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703610"
---
# <a name="measureidentity-operation"></a>Bewerking MeasureIdentity

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket [](https://nuget.org/packages/)


Hiermee wordt de identiteits operator in een REGI ster van qubits gemeten.

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a>Invoer

### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Het REGI ster dat moet worden gemeten.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__

De resultaat waarde `Zero` .

## <a name="remarks"></a>Opmerkingen

Aangezien $ \boldone $ alleen de eigenvalue $1 $ heeft en geen negatieve eigenvalue heeft, retourneert deze bewerking altijd `Zero` , die overeenkomt met de eigenvalue $ + 1 = (-1) ^ 0 $, en treedt er geen samen werking van de status van op `register` .

Op zichzelf is deze bewerking niet nuttig, maar is handig in de context van Process tomography, omdat deze informatie bevat over het behoud van de bewaring van een quantum proces.
Met name een doel computer met verlies van metingen moet deze bewerking vervangen door een werkelijke meting van $ \boldone $.