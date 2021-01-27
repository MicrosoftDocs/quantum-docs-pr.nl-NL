---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Bewerking GetQubitsAvailableToBorrow
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: f2294fadb9c10d800b7a743fbfe0810f36f18516
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853253"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="eab73-102">Bewerking GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="eab73-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="eab73-103">Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="eab73-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="eab73-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="eab73-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="eab73-105">Retourneert het aantal qubits dat momenteel beschikbaar is om te lenen.</span><span class="sxs-lookup"><span data-stu-id="eab73-105">Returns the number of qubits currently available to borrow.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="eab73-106">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eab73-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eab73-107">Het aantal qubits dat kan worden uitgeleend en niet als onderdeel van een instructie wordt toegewezen `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="eab73-107">The number of qubits that could be borrowed and won't be allocated as part of a `borrowing` statement.</span></span>
<span data-ttu-id="eab73-108">Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="eab73-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="eab73-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="eab73-109">See Also</span></span>

- [<span data-ttu-id="eab73-110">Micro soft. Quantum. Environment. GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="eab73-110">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)