---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Bewerking ApplyToFirstQubitA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 4f0b209988c01076bdd0429d36d98c8060141618
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208836"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="cd730-102">Bewerking ApplyToFirstQubitA</span><span class="sxs-lookup"><span data-stu-id="cd730-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="cd730-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cd730-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cd730-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd730-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd730-105">Hiermee wordt een bewerking toegepast op de eerste Qubit in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="cd730-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="cd730-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="cd730-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="cd730-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd730-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="cd730-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="cd730-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cd730-109">Een bewerking die moet worden toegepast op de eerste Qubit</span><span class="sxs-lookup"><span data-stu-id="cd730-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="cd730-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cd730-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cd730-111">Qubit-matrix naar de eerste Qubit waarop de bewerking wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="cd730-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="cd730-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd730-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="cd730-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cd730-113">See Also</span></span>

- [<span data-ttu-id="cd730-114">Micro soft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="cd730-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)