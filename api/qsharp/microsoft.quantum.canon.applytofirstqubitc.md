---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Bewerking ApplyToFirstQubitC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: a36d20e03ebed82435d1d4136f4ce777eb468926
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850721"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="940ad-102">Bewerking ApplyToFirstQubitC</span><span class="sxs-lookup"><span data-stu-id="940ad-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="940ad-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="940ad-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="940ad-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="940ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="940ad-105">Hiermee wordt de bewerking toegepast op de eerste Qubit in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="940ad-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="940ad-106">De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="940ad-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="940ad-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="940ad-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="940ad-108">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="940ad-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="940ad-109">Een bewerking die moet worden toegepast op de eerste Qubit</span><span class="sxs-lookup"><span data-stu-id="940ad-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="940ad-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="940ad-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="940ad-111">Qubit-matrix naar de eerste Qubit waarop de bewerking wordt toegepast</span><span class="sxs-lookup"><span data-stu-id="940ad-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="940ad-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="940ad-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="940ad-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="940ad-113">See Also</span></span>

- [<span data-ttu-id="940ad-114">Micro soft. Quantum. Canon. ApplyToFirstQubit</span><span class="sxs-lookup"><span data-stu-id="940ad-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)