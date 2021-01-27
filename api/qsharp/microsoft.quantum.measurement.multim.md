---
uid: Microsoft.Quantum.Measurement.MultiM
title: Bewerking MultiM
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: b7f4083bde84c204611ea33746ae351a3e27b946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856997"
---
# <a name="multim-operation"></a><span data-ttu-id="9e060-102">Bewerking MultiM</span><span class="sxs-lookup"><span data-stu-id="9e060-102">MultiM operation</span></span>

<span data-ttu-id="9e060-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="9e060-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="9e060-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e060-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e060-105">Meet elk Qubit in een bepaalde matrix in de standaard basis.</span><span class="sxs-lookup"><span data-stu-id="9e060-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="9e060-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9e060-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="9e060-107">doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9e060-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9e060-108">Een matrix met qubits die moeten worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="9e060-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9e060-109">Uitvoer: __ongeldig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="9e060-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="9e060-110">Een matrix met meet resultaten.</span><span class="sxs-lookup"><span data-stu-id="9e060-110">An array of measurement results.</span></span>