---
uid: Microsoft.Quantum.Intrinsic.R
title: R-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 1df4b1197e885e479339e542e8c1ffaeb392543d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818721"
---
# <a name="r-operation"></a><span data-ttu-id="115bb-102">R-bewerking</span><span class="sxs-lookup"><span data-stu-id="115bb-102">R operation</span></span>

<span data-ttu-id="115bb-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="115bb-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="115bb-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="115bb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="115bb-105">Past een rotatie over de opgegeven Pauli-as toe.</span><span class="sxs-lookup"><span data-stu-id="115bb-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="115bb-106">\begin{align} R_ {\mu} (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_ {\mu}/2}, \end{align} waarbij $ \mu \in \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="115bb-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="115bb-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="115bb-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="115bb-108">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="115bb-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="115bb-109">De Pauli-operator ($ \mu $) moet worden exponentiated om de draaiing te vormen.</span><span class="sxs-lookup"><span data-stu-id="115bb-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="115bb-110">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="115bb-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="115bb-111">De hoek waarover de Qubit wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="115bb-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="115bb-112">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="115bb-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="115bb-113">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="115bb-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="115bb-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="115bb-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="115bb-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="115bb-115">Remarks</span></span>

<span data-ttu-id="115bb-116">Als deze bewerking wordt aangeroepen met `pauli = PauliI` , wordt een *globale fase* toegepast.</span><span class="sxs-lookup"><span data-stu-id="115bb-116">When called with `pauli = PauliI`, this operation applies a *global phase*.</span></span> <span data-ttu-id="115bb-117">Deze fase kan aanzienlijk zijn wanneer deze wordt gebruikt in combi natie met de `Controlled` functor.</span><span class="sxs-lookup"><span data-stu-id="115bb-117">This phase can be significant when used with the `Controlled` functor.</span></span>