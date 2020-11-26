---
uid: Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
title: Door de gebruiker gedefinieerd MixedStatePreparationRequirements-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparationRequirements
qsharp.summary: Represents the number of qubits required in order to prepare a given mixed state.
ms.openlocfilehash: 3ea4757f6aa5125418b1e81db9f32e7b668eb359
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228692"
---
# <a name="mixedstatepreparationrequirements-user-defined-type"></a><span data-ttu-id="7643f-102">Door de gebruiker gedefinieerd MixedStatePreparationRequirements-type</span><span class="sxs-lookup"><span data-stu-id="7643f-102">MixedStatePreparationRequirements user defined type</span></span>

<span data-ttu-id="7643f-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7643f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7643f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7643f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7643f-105">Hiermee wordt het aantal qubits aangegeven dat is vereist om een bepaalde gemengde status voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="7643f-105">Represents the number of qubits required in order to prepare a given mixed state.</span></span>

```qsharp

newtype MixedStatePreparationRequirements = (NTotalQubits : Int, (NIndexQubits : Int, NGarbageQubits : Int));
```



## <a name="named-items"></a><span data-ttu-id="7643f-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="7643f-106">Named Items</span></span>

### <a name="ntotalqubits--int"></a><span data-ttu-id="7643f-107">NTotalQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7643f-107">NTotalQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="nindexqubits--int"></a><span data-ttu-id="7643f-108">NIndexQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7643f-108">NIndexQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="ngarbagequbits--int"></a><span data-ttu-id="7643f-109">NGarbageQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7643f-109">NGarbageQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="see-also"></a><span data-ttu-id="7643f-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7643f-110">See Also</span></span>

- [<span data-ttu-id="7643f-111">Micro soft. Quantum. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="7643f-111">Microsoft.Quantum.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.PurifiedMixedState)