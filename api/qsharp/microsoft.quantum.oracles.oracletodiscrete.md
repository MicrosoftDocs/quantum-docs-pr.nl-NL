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
# <a name="oracletodiscrete-function"></a><span data-ttu-id="fd38e-102">De functie OracleToDiscrete</span><span class="sxs-lookup"><span data-stu-id="fd38e-102">OracleToDiscrete function</span></span>

<span data-ttu-id="fd38e-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="fd38e-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="fd38e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd38e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd38e-105">Op basis van een bewerking die een ' Black-Box ' Oracle vertegenwoordigt, wordt een eenmalige Oracle-waarde geretourneerd waarmee het ' Black-Box ' Oracle meerdere malen wordt herhaald.</span><span class="sxs-lookup"><span data-stu-id="fd38e-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="fd38e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fd38e-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a><span data-ttu-id="fd38e-107">blackBoxOracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="fd38e-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="fd38e-108">De bewerking die moet worden exponentiated.</span><span class="sxs-lookup"><span data-stu-id="fd38e-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="fd38e-109">Uitvoer: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="fd38e-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="fd38e-110">Een bewerking die gedeeltelijk wordt toegepast via de ' Black-Box ' Oracle die de eenmalige Oracle vertegenwoordigt</span><span class="sxs-lookup"><span data-stu-id="fd38e-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>

## <a name="example"></a><span data-ttu-id="fd38e-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fd38e-111">Example</span></span>

<span data-ttu-id="fd38e-112">`OracleToDiscrete(U)(3, target)` komt overeen met `U(target)` drie keer herhaald.</span><span class="sxs-lookup"><span data-stu-id="fd38e-112">`OracleToDiscrete(U)(3, target)` is equivalent to `U(target)` repeated three times.</span></span>