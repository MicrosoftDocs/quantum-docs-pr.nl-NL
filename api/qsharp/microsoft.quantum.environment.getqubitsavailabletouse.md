---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Bewerking GetQubitsAvailableToUse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702585"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="b8952-102">Bewerking GetQubitsAvailableToUse</span><span class="sxs-lookup"><span data-stu-id="b8952-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="b8952-103">Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="b8952-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="b8952-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b8952-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b8952-105">Retourneert het aantal qubits dat momenteel beschikbaar is voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="b8952-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="b8952-106">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b8952-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b8952-107">Het aantal qubits dat in een instructie kan worden toegewezen `using` .</span><span class="sxs-lookup"><span data-stu-id="b8952-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="b8952-108">Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="b8952-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8952-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b8952-109">See Also</span></span>

- [<span data-ttu-id="b8952-110">Micro soft. Quantum. Environment. GetQubitsAvailableToBorrow</span><span class="sxs-lookup"><span data-stu-id="b8952-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)