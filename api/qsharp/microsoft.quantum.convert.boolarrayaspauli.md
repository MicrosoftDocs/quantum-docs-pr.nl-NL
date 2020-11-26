---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: De functie BoolArrayAsPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: 8e7088ec3918165d7b2afb1056a8319c6fb17796
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214276"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="cd935-102">De functie BoolArrayAsPauli</span><span class="sxs-lookup"><span data-stu-id="cd935-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="cd935-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="cd935-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="cd935-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd935-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd935-105">Op basis van een bit string retourneert een multi-Qubit Pauli-operator die wordt weer gegeven als een matrix van Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="cd935-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="cd935-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd935-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="cd935-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="cd935-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="cd935-108">De operator Pauli die moet worden toegepast op qubits WHERE `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="cd935-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="cd935-109">bitApply: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cd935-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cd935-110">pas Pauli toe als bit deze waarde is.</span><span class="sxs-lookup"><span data-stu-id="cd935-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="cd935-111">bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="cd935-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="cd935-112">Boole-matrix.</span><span class="sxs-lookup"><span data-stu-id="cd935-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="cd935-113">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="cd935-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="cd935-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cd935-114">Remarks</span></span>

<span data-ttu-id="cd935-115">De Boole-matrix en het Quantum register moeten even lang zijn.</span><span class="sxs-lookup"><span data-stu-id="cd935-115">The Boolean array and the quantum register must be of equal length.</span></span>