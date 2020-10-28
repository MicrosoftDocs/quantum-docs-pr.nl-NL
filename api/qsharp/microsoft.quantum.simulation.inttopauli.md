---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: De functie IntToPauli
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: f0f1186f14a0dc30bb34bd29f148cdc830fd1337
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709013"
---
# <a name="inttopauli-function"></a><span data-ttu-id="c75ea-102">De functie IntToPauli</span><span class="sxs-lookup"><span data-stu-id="c75ea-102">IntToPauli function</span></span>

<span data-ttu-id="c75ea-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c75ea-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c75ea-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c75ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c75ea-105">Converteert een geheel getal naar een Pauli-operator met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="c75ea-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="c75ea-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c75ea-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="c75ea-107">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c75ea-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c75ea-108">Geheel getal in het bereik `0..3` dat moet worden geconverteerd naar Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="c75ea-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="c75ea-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="c75ea-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="c75ea-110">Een `Pauli` operator die wordt gegeven door `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="c75ea-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>