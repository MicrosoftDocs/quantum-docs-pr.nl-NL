---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Bewerking GetQubitsAvailableToBorrow
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702590"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="6dbb7-102">Bewerking GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="6dbb7-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="6dbb7-103">Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="6dbb7-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="6dbb7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6dbb7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6dbb7-105">Retourneert het aantal qubits dat momenteel beschikbaar is om te lenen.</span><span class="sxs-lookup"><span data-stu-id="6dbb7-105">Returns the number of qubits currently available to borrow.</span></span>
<span data-ttu-id="6dbb7-106">Dit omvat niet-gebruikte qubits; dat wil zeggen dat de qubits die wordt geretourneerd door `GetQubitsAvailableToUse` .</span><span class="sxs-lookup"><span data-stu-id="6dbb7-106">This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="6dbb7-107">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6dbb7-107">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6dbb7-108">Het aantal qubits dat in een instructie kan worden toegewezen `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="6dbb7-108">The number of qubits that could be allocated in a `borrowing` statement.</span></span>
<span data-ttu-id="6dbb7-109">Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="6dbb7-109">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dbb7-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6dbb7-110">See Also</span></span>

- [<span data-ttu-id="6dbb7-111">Micro soft. Quantum. Environment. GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="6dbb7-111">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)