---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Bewerking opnieuw instellen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: c89cbbce49e294e56abc11b3b0492d2ed8e980a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707109"
---
# <a name="reset-operation"></a><span data-ttu-id="4bf7e-102">Bewerking opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="4bf7e-102">Reset operation</span></span>

<span data-ttu-id="4bf7e-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="4bf7e-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="4bf7e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4bf7e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4bf7e-105">Op basis van één Qubit wordt deze gemeten en wordt gegarandeerd dat deze zich in de ⟩-status | 0 bevindt, zodat deze veilig kan worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="4bf7e-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="4bf7e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4bf7e-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="4bf7e-107">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4bf7e-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4bf7e-108">De Qubit waarvan de status moet worden ingesteld op $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="4bf7e-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4bf7e-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4bf7e-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

