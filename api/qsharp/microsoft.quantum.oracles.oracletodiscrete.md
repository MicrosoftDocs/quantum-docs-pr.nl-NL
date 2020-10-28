---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: De functie OracleToDiscrete
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708755"
---
# <a name="oracletodiscrete-function"></a>De functie OracleToDiscrete

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


Op basis van een bewerking die een ' Black-Box ' Oracle vertegenwoordigt, wordt een eenmalige Oracle-waarde geretourneerd waarmee het ' Black-Box ' Oracle meerdere malen wordt herhaald.

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a>Invoer

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a>blackBoxOracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

De bewerking die moet worden exponentiated.



## <a name="output--discreteoracle"></a>Uitvoer: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Een bewerking die gedeeltelijk wordt toegepast via de ' Black-Box ' Oracle die de eenmalige Oracle vertegenwoordigt