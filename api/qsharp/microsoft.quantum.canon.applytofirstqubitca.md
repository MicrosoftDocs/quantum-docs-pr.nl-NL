---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Bewerking ApplyToFirstQubitCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: ba82199cc7a548d771027141780873c05de71c57
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841432"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="b7fe7-102">Bewerking ApplyToFirstQubitCA</span><span class="sxs-lookup"><span data-stu-id="b7fe7-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="b7fe7-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b7fe7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b7fe7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b7fe7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b7fe7-105">Hiermee wordt de bewerking toegepast op de eerste Qubit in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="b7fe7-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="b7fe7-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="b7fe7-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b7fe7-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="b7fe7-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="b7fe7-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="b7fe7-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="b7fe7-109">Een bewerking die moet worden toegepast op de eerste Qubit</span><span class="sxs-lookup"><span data-stu-id="b7fe7-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="b7fe7-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b7fe7-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b7fe7-111">Qubit-matrix naar de eerste Qubit waarop de bewerking wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="b7fe7-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="b7fe7-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b7fe7-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="b7fe7-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b7fe7-113">See Also</span></span>

- [<span data-ttu-id="b7fe7-114">Micro soft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="b7fe7-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)