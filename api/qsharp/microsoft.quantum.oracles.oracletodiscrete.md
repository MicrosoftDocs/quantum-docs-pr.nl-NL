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
# <a name="oracletodiscrete-function"></a><span data-ttu-id="04b22-102">De functie OracleToDiscrete</span><span class="sxs-lookup"><span data-stu-id="04b22-102">OracleToDiscrete function</span></span>

<span data-ttu-id="04b22-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="04b22-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="04b22-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="04b22-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="04b22-105">Op basis van een bewerking die een ' Black-Box ' Oracle vertegenwoordigt, wordt een eenmalige Oracle-waarde geretourneerd waarmee het ' Black-Box ' Oracle meerdere malen wordt herhaald.</span><span class="sxs-lookup"><span data-stu-id="04b22-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="04b22-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="04b22-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a><span data-ttu-id="04b22-107">blackBoxOracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="04b22-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="04b22-108">De bewerking die moet worden exponentiated.</span><span class="sxs-lookup"><span data-stu-id="04b22-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="04b22-109">Uitvoer: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="04b22-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="04b22-110">Een bewerking die gedeeltelijk wordt toegepast via de ' Black-Box ' Oracle die de eenmalige Oracle vertegenwoordigt</span><span class="sxs-lookup"><span data-stu-id="04b22-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>