---
uid: Microsoft.Quantum.Measurement.MultiM
title: Bewerking MultiM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: c39601f3e8b272b9341f1789b4c8e7230cb4182c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226992"
---
# <a name="multim-operation"></a><span data-ttu-id="bbf8e-102">Bewerking MultiM</span><span class="sxs-lookup"><span data-stu-id="bbf8e-102">MultiM operation</span></span>

<span data-ttu-id="bbf8e-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="bbf8e-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="bbf8e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bbf8e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bbf8e-105">Meet elk Qubit in een bepaalde matrix in de standaard basis.</span><span class="sxs-lookup"><span data-stu-id="bbf8e-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="bbf8e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bbf8e-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="bbf8e-107">doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bbf8e-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bbf8e-108">Een matrix met qubits die moeten worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="bbf8e-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="bbf8e-109">Uitvoer: __ongeldig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="bbf8e-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="bbf8e-110">Een matrix met meet resultaten.</span><span class="sxs-lookup"><span data-stu-id="bbf8e-110">An array of measurement results.</span></span>