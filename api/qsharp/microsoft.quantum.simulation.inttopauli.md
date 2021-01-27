---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: De functie IntToPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842255"
---
# <a name="inttopauli-function"></a><span data-ttu-id="e7c96-102">De functie IntToPauli</span><span class="sxs-lookup"><span data-stu-id="e7c96-102">IntToPauli function</span></span>

<span data-ttu-id="e7c96-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e7c96-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e7c96-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7c96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7c96-105">Converteert een geheel getal naar een Pauli-operator met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="e7c96-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="e7c96-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e7c96-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="e7c96-107">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e7c96-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e7c96-108">Geheel getal in het bereik `0..3` dat moet worden geconverteerd naar Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="e7c96-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="e7c96-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e7c96-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e7c96-110">Een `Pauli` operator die wordt gegeven door `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="e7c96-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>