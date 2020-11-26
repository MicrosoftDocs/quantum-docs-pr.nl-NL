---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Bewerking GetQubitsAvailableToUse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201407"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="770ad-102">Bewerking GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="770ad-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="770ad-103">Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="770ad-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="770ad-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="770ad-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="770ad-105">Retourneert het aantal qubits dat momenteel beschikbaar is voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="770ad-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="770ad-106">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="770ad-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="770ad-107">Het aantal qubits dat in een instructie kan worden toegewezen `using` .</span><span class="sxs-lookup"><span data-stu-id="770ad-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="770ad-108">Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="770ad-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="770ad-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="770ad-109">See Also</span></span>

- [<span data-ttu-id="770ad-110">Micro soft. Quantum. Environment. GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="770ad-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)