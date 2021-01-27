---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC
title: Bewerking ApplyToFirstThreeQubitsC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsC
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 2c4fe7c645913cb0703982d78f65645f141fdcae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841392"
---
# <a name="applytofirstthreequbitsc-operation"></a><span data-ttu-id="6ed49-102">Bewerking ApplyToFirstThreeQubitsC</span><span class="sxs-lookup"><span data-stu-id="6ed49-102">ApplyToFirstThreeQubitsC operation</span></span>

<span data-ttu-id="6ed49-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6ed49-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6ed49-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6ed49-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6ed49-105">Hiermee wordt een bewerking toegepast op de eerste drie qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="6ed49-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="6ed49-106">De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="6ed49-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsC (op : ((Qubit, Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="6ed49-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="6ed49-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-ctl"></a><span data-ttu-id="6ed49-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="6ed49-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="6ed49-109">Een bewerking die moet worden toegepast op de eerste drie qubits</span><span class="sxs-lookup"><span data-stu-id="6ed49-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="6ed49-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6ed49-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6ed49-111">Qubit-matrix naar de eerste drie qubits waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="6ed49-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6ed49-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6ed49-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6ed49-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6ed49-113">Remarks</span></span>

<span data-ttu-id="6ed49-114">Dit komt overeen met:</span><span class="sxs-lookup"><span data-stu-id="6ed49-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="6ed49-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6ed49-115">See Also</span></span>

- [<span data-ttu-id="6ed49-116">Micro soft. Quantum. Canon. ApplyToFirstThreeQubits</span><span class="sxs-lookup"><span data-stu-id="6ed49-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)