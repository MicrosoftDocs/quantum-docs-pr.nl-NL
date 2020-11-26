---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateCA
title: Bewerking PrepareChoiStateCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateCA
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.
ms.openlocfilehash: abe75865149c985426a5eaf69cf41433829e1916
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210485"
---
# <a name="preparechoistateca-operation"></a><span data-ttu-id="a24b1-102">Bewerking PrepareChoiStateCA</span><span class="sxs-lookup"><span data-stu-id="a24b1-102">PrepareChoiStateCA operation</span></span>

<span data-ttu-id="a24b1-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="a24b1-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="a24b1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a24b1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a24b1-105">Hiermee wordt de status van de Choi-Jamiołkowski voor een bepaalde bewerking voorbereidt met zowel beheerde als adjoint varianten op gegeven referentie-en doel registers.</span><span class="sxs-lookup"><span data-stu-id="a24b1-105">Prepares the Choi–Jamiołkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiStateCA (op : (Qubit[] => Unit is Adj + Ctl), reference : Qubit[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a24b1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a24b1-106">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="a24b1-107">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="a24b1-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="reference--qubit"></a><span data-ttu-id="a24b1-108">verwijzing: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a24b1-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="a24b1-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a24b1-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="a24b1-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a24b1-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="a24b1-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a24b1-111">See Also</span></span>

- [<span data-ttu-id="a24b1-112">Micro soft. Quantum. prepare. PrepareChoiState</span><span class="sxs-lookup"><span data-stu-id="a24b1-112">Microsoft.Quantum.Preparation.PrepareChoiState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiState)