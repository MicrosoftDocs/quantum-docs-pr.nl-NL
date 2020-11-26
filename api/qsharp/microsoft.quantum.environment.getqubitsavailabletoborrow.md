---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Bewerking GetQubitsAvailableToBorrow
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: 30b97c2b6e1353f008d085c3bae6160763557c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201458"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="3ef55-102">Bewerking GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="3ef55-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="3ef55-103">Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="3ef55-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="3ef55-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ef55-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3ef55-105">Retourneert het aantal qubits dat momenteel beschikbaar is om te lenen.</span><span class="sxs-lookup"><span data-stu-id="3ef55-105">Returns the number of qubits currently available to borrow.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="3ef55-106">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ef55-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ef55-107">Het aantal qubits dat kan worden uitgeleend en niet als onderdeel van een instructie wordt toegewezen `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="3ef55-107">The number of qubits that could be borrowed and won't be allocated as part of a `borrowing` statement.</span></span>
<span data-ttu-id="3ef55-108">Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3ef55-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ef55-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3ef55-109">See Also</span></span>

- [<span data-ttu-id="3ef55-110">Micro soft. Quantum. Environment. GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="3ef55-110">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)