---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: Door de gebruiker gedefinieerd RecoveryFn-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: ac3c17da172a8f906643091745e9278bb17d02eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200506"
---
# <a name="recoveryfn-user-defined-type"></a><span data-ttu-id="d6a93-102">Door de gebruiker gedefinieerd RecoveryFn-type</span><span class="sxs-lookup"><span data-stu-id="d6a93-102">RecoveryFn user defined type</span></span>

<span data-ttu-id="d6a93-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d6a93-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d6a93-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6a93-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6a93-105">Type voor functie waarmee een fout Syndrome wordt toegewezen aan een reeks `Pauli[]` bewerkingen die de gedetecteerde fout corrigeert.</span><span class="sxs-lookup"><span data-stu-id="d6a93-105">Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.</span></span>

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

