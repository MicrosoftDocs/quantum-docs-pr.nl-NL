---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Bewerking PrepareIdentity
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: a3f96fbdafb19c90fb2b563243600cca60841566
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709031"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="03666-102">Bewerking PrepareIdentity</span><span class="sxs-lookup"><span data-stu-id="03666-102">PrepareIdentity operation</span></span>

<span data-ttu-id="03666-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="03666-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="03666-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03666-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03666-105">Op basis van een REGI ster, bereidt dat registratie voor op de gemengde status maximally.</span><span class="sxs-lookup"><span data-stu-id="03666-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="03666-106">De kassa wordt voor bereid in de status $ \boldone/2 ^ N $ door het volledige depolarizing-kanaal toe te passen op elke qubit, waarbij $N $ de lengte van het REGI ster is.</span><span class="sxs-lookup"><span data-stu-id="03666-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="03666-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="03666-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="03666-108">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="03666-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="03666-109">Een REGI ster waarvan de status moet worden ontpolair op de manier die hierboven wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="03666-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03666-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03666-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="03666-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="03666-111">See Also</span></span>

- [<span data-ttu-id="03666-112">Micro soft. Quantum. prepare. PrepareSingleQubitIdentity</span><span class="sxs-lookup"><span data-stu-id="03666-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)