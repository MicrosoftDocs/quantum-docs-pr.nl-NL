---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: Bewerking ResetAll
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 00b7c0f508d76fb0f5b46c7ec00c0718469365a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702086"
---
# <a name="resetall-operation"></a><span data-ttu-id="27e19-102">Bewerking ResetAll</span><span class="sxs-lookup"><span data-stu-id="27e19-102">ResetAll operation</span></span>

<span data-ttu-id="27e19-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="27e19-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="27e19-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="27e19-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="27e19-105">Geef ze op in een matrix met qubits en zorg ervoor dat deze zich in de ⟩-status | 0 bevinden, zodat ze veilig kunnen worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="27e19-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="27e19-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="27e19-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="27e19-107">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="27e19-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="27e19-108">Een matrix met qubits waarvan de status moet worden ingesteld op $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="27e19-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="27e19-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27e19-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
