---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: De functie OracleToDiscrete
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842544"
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

## <a name="example"></a>Voorbeeld

`OracleToDiscrete(U)(3, target)` komt overeen met `U(target)` drie keer herhaald.