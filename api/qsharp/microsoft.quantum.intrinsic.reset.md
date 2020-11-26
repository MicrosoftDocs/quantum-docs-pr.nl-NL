---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Bewerking opnieuw instellen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: 61b5e4ccdf009dcb6c639e3d8e23bc73a6e475b5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198670"
---
# <a name="reset-operation"></a><span data-ttu-id="0beb7-102">Bewerking opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="0beb7-102">Reset operation</span></span>

<span data-ttu-id="0beb7-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="0beb7-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="0beb7-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0beb7-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0beb7-105">Op basis van één Qubit wordt deze gemeten en wordt gegarandeerd dat deze zich in de ⟩-status | 0 bevindt, zodat deze veilig kan worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="0beb7-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0beb7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0beb7-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="0beb7-107">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0beb7-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0beb7-108">De Qubit waarvan de status moet worden ingesteld op $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="0beb7-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0beb7-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0beb7-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

