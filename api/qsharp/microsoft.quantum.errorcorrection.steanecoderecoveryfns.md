---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: De functie SteaneCodeRecoveryFns
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 8dc715042f98b90b8cea7e2d6ecb5d02a78d297f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853032"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="388da-102">De functie SteaneCodeRecoveryFns</span><span class="sxs-lookup"><span data-stu-id="388da-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="388da-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="388da-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="388da-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="388da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="388da-105">Decoder voor gecombineerde X-en Z-onderdelen van de stabilisatoren groep van de ⟦-⟧ Steane Quantum-code.</span><span class="sxs-lookup"><span data-stu-id="388da-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="388da-106">Uitvoer: ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="388da-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="388da-107">De tuple van de functies van `RecoveryFn` het type dat een Syndrome meting afneemt `Result[]` en de `Pauli[]` bewerkingen retourneert die de gedetecteerde fout corrigeren.</span><span class="sxs-lookup"><span data-stu-id="388da-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="388da-108">Zie ook</span><span class="sxs-lookup"><span data-stu-id="388da-108">See Also</span></span>

- [<span data-ttu-id="388da-109">Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="388da-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="388da-110">Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryZ</span><span class="sxs-lookup"><span data-stu-id="388da-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)