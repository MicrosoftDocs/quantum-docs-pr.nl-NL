---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: De functie OracleToDiscrete
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: 158a90bbd0c68406e0a8507ae99fc08fad3b6d19
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193842"
---
# <a name="oracletodiscrete-function"></a>De functie OracleToDiscrete

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een bewerking die een ' Black-Box ' Oracle vertegenwoordigt, wordt een eenmalige Oracle-waarde geretourneerd waarmee het ' Black-Box ' Oracle meerdere malen wordt herhaald.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Invoer

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a>blackBoxOracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De bewerking die moet worden exponentiated.



## <a name="output--discreteoracle"></a>Uitvoer: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Een bewerking die gedeeltelijk wordt toegepast via de ' Black-Box ' Oracle die de eenmalige Oracle vertegenwoordigt