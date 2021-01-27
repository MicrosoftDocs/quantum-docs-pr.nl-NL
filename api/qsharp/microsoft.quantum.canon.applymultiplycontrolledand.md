---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Bewerking ApplyMultiplyControlledAnd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: ac3972287d55ed2df85e1d88510918cc5202c711
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844843"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="cd2f0-102">Bewerking ApplyMultiplyControlledAnd</span><span class="sxs-lookup"><span data-stu-id="cd2f0-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="cd2f0-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cd2f0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cd2f0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd2f0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd2f0-105">Implementeert een multi-beheerde Toffoli-Gate, ervan uitgaande dat de doel-Qubit 0 is geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="cd2f0-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="cd2f0-106">Bij de bewerking adjoint wordt ervan uitgegaan dat de doel-Qubit opnieuw wordt ingesteld op 0.</span><span class="sxs-lookup"><span data-stu-id="cd2f0-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="cd2f0-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd2f0-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="cd2f0-108">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cd2f0-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cd2f0-109">Qubits beheren</span><span class="sxs-lookup"><span data-stu-id="cd2f0-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="cd2f0-110">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cd2f0-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cd2f0-111">Doel-Qubit</span><span class="sxs-lookup"><span data-stu-id="cd2f0-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="cd2f0-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd2f0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

