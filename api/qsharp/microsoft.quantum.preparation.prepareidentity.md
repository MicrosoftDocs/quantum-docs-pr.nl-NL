---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Bewerking PrepareIdentity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: ec7e813110ccd9e6d499fc469fa27249a182b870
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855875"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="e1604-102">Bewerking PrepareIdentity</span><span class="sxs-lookup"><span data-stu-id="e1604-102">PrepareIdentity operation</span></span>

<span data-ttu-id="e1604-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="e1604-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="e1604-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e1604-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e1604-105">Op basis van een REGI ster, bereidt dat registratie voor op de gemengde status maximally.</span><span class="sxs-lookup"><span data-stu-id="e1604-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="e1604-106">De kassa wordt voor bereid in de status $ \boldone/2 ^ N $ door het volledige depolarizing-kanaal toe te passen op elke qubit, waarbij $N $ de lengte van het REGI ster is.</span><span class="sxs-lookup"><span data-stu-id="e1604-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e1604-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="e1604-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="e1604-108">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e1604-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e1604-109">Een REGI ster waarvan de status moet worden ontpolair op de manier die hierboven wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="e1604-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1604-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1604-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="e1604-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e1604-111">See Also</span></span>

- [<span data-ttu-id="e1604-112">Micro soft. Quantum. prepare. PrepareSingleQubitIdentity</span><span class="sxs-lookup"><span data-stu-id="e1604-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)