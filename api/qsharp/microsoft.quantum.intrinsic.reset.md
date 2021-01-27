---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Bewerking opnieuw instellen
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: b4275796b966bfe7f55271f4e92866410a14e830
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818631"
---
# <a name="reset-operation"></a><span data-ttu-id="fa69a-102">Bewerking opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="fa69a-102">Reset operation</span></span>

<span data-ttu-id="fa69a-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="fa69a-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="fa69a-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fa69a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fa69a-105">Op basis van één Qubit wordt deze gemeten en wordt gegarandeerd dat deze zich in de ⟩-status | 0 bevindt, zodat deze veilig kan worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="fa69a-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="fa69a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fa69a-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="fa69a-107">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fa69a-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fa69a-108">De Qubit waarvan de status moet worden ingesteld op $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="fa69a-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fa69a-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa69a-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

