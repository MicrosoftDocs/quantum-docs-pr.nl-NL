---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: De functie FiveQubitCodeRecoveryFn
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 94b6c12f31b0e6367151d0ebb225cff5f82915e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853132"
---
# <a name="fivequbitcoderecoveryfn-function"></a><span data-ttu-id="5c7db-102">De functie FiveQubitCodeRecoveryFn</span><span class="sxs-lookup"><span data-stu-id="5c7db-102">FiveQubitCodeRecoveryFn function</span></span>

<span data-ttu-id="5c7db-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="5c7db-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="5c7db-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5c7db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5c7db-105">Retourneert een functie die fout Syndrome-metingen toewijst aan de juiste fout: Pauli Opera tors worden door de zoek opdracht voor de ⟦ 5, 1, 3 ⟧ Quantum code toegewezen.</span><span class="sxs-lookup"><span data-stu-id="5c7db-105">Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="5c7db-106">Uitvoer: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="5c7db-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="5c7db-107">Functie van `RecoveryFn` het type dat een Syndrome meting afneemt `Result[]` en de `Pauli[]` Opera tors retourneert die de gedetecteerde fout corrigeert.</span><span class="sxs-lookup"><span data-stu-id="5c7db-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operators that corrects the detected error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c7db-108">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5c7db-108">Remarks</span></span>

<span data-ttu-id="5c7db-109">Door alle fouten van gewicht $1 $ te herhalen, krijgen we $3 \ Times 5 = 15 $ mogelijk niet-trivial Syndromes.</span><span class="sxs-lookup"><span data-stu-id="5c7db-109">By iterating over all errors of weight $1$, we obtain a total of $3\times 5=15$ possible non-trivial syndromes.</span></span>
<span data-ttu-id="5c7db-110">Samen met de identiteit wordt een tabel met fouten en bijbehorende Syndrome gebouwd.</span><span class="sxs-lookup"><span data-stu-id="5c7db-110">Together with the identity, a table of error and corresponding syndrome is built up.</span></span> <span data-ttu-id="5c7db-111">Voor de 5 Qubit-code wordt deze tabel gegeven door: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ met $Y _I $ verkregen door de $X _I $ en $Z _I $ Syndromes toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5c7db-111">For the 5 qubit code this table is given by: $X\_1: (0,0,0,1); X\_2: (1,0,0,0); X\_3: (1,1,0,0); X\_4: (0,1,1,0); X\_5: (0,0,1,1)$, $Z\_1: (1,0,1,0); Z\_2: (0,1,0,1); Z\_3: (0,0,1,0); Z\_4: (1,0,0,1); Z\_5: (0,1,0,0)$ with $Y_i$ obtained by adding the $X_i$ and $Z_i$ syndromes.</span></span> <span data-ttu-id="5c7db-112">Houd er rekening mee dat de volg orde in het herstel van de tabel zoek opdracht wordt gegeven door de bitvectors te converteren naar gehele getallen (met behulp van little endian).</span><span class="sxs-lookup"><span data-stu-id="5c7db-112">Note that the ordering in the table lookup recovery is given by converting the bitvectors to integers (using little endian).</span></span>

## <a name="see-also"></a><span data-ttu-id="5c7db-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5c7db-113">See Also</span></span>

- [<span data-ttu-id="5c7db-114">Micro soft. Quantum. ErrorCorrection. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="5c7db-114">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)