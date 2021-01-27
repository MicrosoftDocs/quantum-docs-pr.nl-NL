---
uid: Microsoft.Quantum.Preparation.MixedStatePreparation
title: Door de gebruiker gedefinieerd MixedStatePreparation-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparation
qsharp.summary: Represents a particular mixed state that can be prepared on an index and a garbage register.
ms.openlocfilehash: 7e5b6ca755aac19a31b7e27e32e934bb823b128e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842409"
---
# <a name="mixedstatepreparation-user-defined-type"></a><span data-ttu-id="069fa-102">Door de gebruiker gedefinieerd MixedStatePreparation-type</span><span class="sxs-lookup"><span data-stu-id="069fa-102">MixedStatePreparation user defined type</span></span>

<span data-ttu-id="069fa-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="069fa-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="069fa-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="069fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="069fa-105">Dit object vertegenwoordigt een bepaalde gemengde status die kan worden voor bereid op een index en een garbagecollection-registratie.</span><span class="sxs-lookup"><span data-stu-id="069fa-105">Represents a particular mixed state that can be prepared on an index and a garbage register.</span></span>

```qsharp

newtype MixedStatePreparation = (Requirements : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements, Norm : Double, Prepare : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="069fa-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="069fa-106">Named Items</span></span>

### <a name="requirements--mixedstatepreparationrequirements"></a><span data-ttu-id="069fa-107">Vereisten: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="069fa-107">Requirements : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>


### <a name="norm--double"></a><span data-ttu-id="069fa-108">Norm: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="069fa-108">Norm : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>


### <a name="prepare--littleendianqubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="069fa-109">Voorbereiden: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="069fa-109">Prepare : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="069fa-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="069fa-110">See Also</span></span>

- [<span data-ttu-id="069fa-111">Micro soft. Quantum. PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="069fa-111">Microsoft.Quantum.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.PurifiedMixedState)