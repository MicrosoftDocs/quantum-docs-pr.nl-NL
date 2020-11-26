---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Bewerking PrepareChoiState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: ced71c4278f42f577760acd54ae53e7f5e6dae4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210570"
---
# <a name="preparechoistate-operation"></a><span data-ttu-id="c73f6-102">Bewerking PrepareChoiState</span><span class="sxs-lookup"><span data-stu-id="c73f6-102">PrepareChoiState operation</span></span>

<span data-ttu-id="c73f6-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="c73f6-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="c73f6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c73f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c73f6-105">Hiermee wordt de status van de Choi-Jamiołkowski voor een bepaalde bewerking voor de opgegeven referentie-en doel registers voor bereid.</span><span class="sxs-lookup"><span data-stu-id="c73f6-105">Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c73f6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c73f6-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="c73f6-107">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c73f6-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c73f6-108">Bewerking $ \Lambda $ waarvan de Choi-Jamiołkowski-status $J (\Lambda)/2 ^ N $ moet worden voor bereid, waarbij $N $ het aantal qubits is waarop wordt `op` gehandeld.</span><span class="sxs-lookup"><span data-stu-id="c73f6-108">Operation $\Lambda$ whose Choi–Jamiołkowski state $J(\Lambda) / 2^N$ is to be prepared, where $N$ is the number of qubits on which `op` acts.</span></span>


### <a name="reference--qubit"></a><span data-ttu-id="c73f6-109">verwijzing: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c73f6-109">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c73f6-110">Een REGI ster van qubits, te beginnen met de status $ \ket{00\cdots 0} $ die moet worden gebruikt als referentie voor de actie van `op` .</span><span class="sxs-lookup"><span data-stu-id="c73f6-110">A register of qubits starting in the $\ket{00\cdots 0}$ state to be used as a reference for the action of `op`.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c73f6-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c73f6-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c73f6-112">Een REGI ster van qubits in eerste instantie in de $ \ket{00\cdots 0} $-status waarop moet `op` worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c73f6-112">A register of qubits initially in the $\ket{00\cdots 0}$ state on which `op` is to be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c73f6-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c73f6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c73f6-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c73f6-114">Remarks</span></span>

<span data-ttu-id="c73f6-115">De Choi – Jamiłkowski State $J (\Lambda) $ van een quantum proces is gedefinieerd als $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ waarbij $ | X\rangle \! \rangle $ is de *vectorization* van een matrix $X $ in de kolom-stacking-Conventie.</span><span class="sxs-lookup"><span data-stu-id="c73f6-115">The Choi–Jamiłkowski state $J(\Lambda)$ of a quantum process is defined as $$ \begin{align} J(\Lambda) \mathrel{:=} (\boldone \otimes \Lambda) (|\boldone\rangle\!\rangle\langle\!\langle\boldone|), \end{align} $$ where $|X\rangle\!\rangle$ is the *vectorization* of a matrix $X$ in the column-stacking convention.</span></span> <span data-ttu-id="c73f6-116">Het leren van een klassieke beschrijving van deze status biedt volledige informatie over het effect van $ \Lambda $ op wille keurige invoer status en vormt de basis van de tomography van het *Quantum proces*.</span><span class="sxs-lookup"><span data-stu-id="c73f6-116">Learning a classical description of this state provides full information about the effect of $\Lambda$ acting on arbitrary input states, and forms the foundation of *quantum process tomography*.</span></span>

## <a name="see-also"></a><span data-ttu-id="c73f6-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c73f6-117">See Also</span></span>

- [<span data-ttu-id="c73f6-118">Micro soft. Quantum. prepare. PrepareChoiStateA</span><span class="sxs-lookup"><span data-stu-id="c73f6-118">Microsoft.Quantum.Preparation.PrepareChoiStateA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [<span data-ttu-id="c73f6-119">Micro soft. Quantum. prepare. PrepareChoiStateC</span><span class="sxs-lookup"><span data-stu-id="c73f6-119">Microsoft.Quantum.Preparation.PrepareChoiStateC</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [<span data-ttu-id="c73f6-120">Micro soft. Quantum. prepare. PrepareChoiStateCA</span><span class="sxs-lookup"><span data-stu-id="c73f6-120">Microsoft.Quantum.Preparation.PrepareChoiStateCA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)