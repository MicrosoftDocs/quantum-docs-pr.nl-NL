---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Bewerking MeasureIdentity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: f8cf5975ac9407e8c532ace08455a41d3c08d6f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851814"
---
# <a name="measureidentity-operation"></a>Bewerking MeasureIdentity

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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