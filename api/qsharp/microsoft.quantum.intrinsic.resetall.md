---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: Bewerking ResetAll
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 2b8e7fc0e7881d8c1bd6f14c150476262b7a2b19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849325"
---
# <a name="resetall-operation"></a><span data-ttu-id="777df-102">Bewerking ResetAll</span><span class="sxs-lookup"><span data-stu-id="777df-102">ResetAll operation</span></span>

<span data-ttu-id="777df-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="777df-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="777df-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="777df-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="777df-105">Geef ze op in een matrix met qubits en zorg ervoor dat deze zich in de ⟩-status | 0 bevinden, zodat ze veilig kunnen worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="777df-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="777df-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="777df-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="777df-107">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="777df-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="777df-108">Een matrix met qubits waarvan de status moet worden ingesteld op $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="777df-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="777df-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="777df-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

