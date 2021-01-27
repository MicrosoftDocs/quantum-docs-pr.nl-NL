---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: Door de gebruiker gedefinieerd RecoveryFn-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: 7e8afa37e6225239ae7cafa1f48377a97c43297d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825091"
---
# <a name="recoveryfn-user-defined-type"></a><span data-ttu-id="95f9d-102">Door de gebruiker gedefinieerd RecoveryFn-type</span><span class="sxs-lookup"><span data-stu-id="95f9d-102">RecoveryFn user defined type</span></span>

<span data-ttu-id="95f9d-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="95f9d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="95f9d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95f9d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95f9d-105">Type voor functie waarmee een fout Syndrome wordt toegewezen aan een reeks `Pauli[]` bewerkingen die de gedetecteerde fout corrigeert.</span><span class="sxs-lookup"><span data-stu-id="95f9d-105">Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.</span></span>

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

