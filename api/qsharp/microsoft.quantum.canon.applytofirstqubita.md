---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Bewerking ApplyToFirstQubitA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 2f96c2a8ed31d295bc127c568e0ca24c267638b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841453"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="733a0-102">Bewerking ApplyToFirstQubitA</span><span class="sxs-lookup"><span data-stu-id="733a0-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="733a0-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="733a0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="733a0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="733a0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="733a0-105">Hiermee wordt een bewerking toegepast op de eerste Qubit in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="733a0-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="733a0-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="733a0-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="733a0-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="733a0-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="733a0-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="733a0-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="733a0-109">Een bewerking die moet worden toegepast op de eerste Qubit</span><span class="sxs-lookup"><span data-stu-id="733a0-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="733a0-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="733a0-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="733a0-111">Qubit-matrix naar de eerste Qubit waarop de bewerking wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="733a0-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="733a0-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="733a0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="733a0-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="733a0-113">See Also</span></span>

- [<span data-ttu-id="733a0-114">Micro soft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="733a0-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)