---
uid: Microsoft.Quantum.Measurement.MResetX
title: Bewerking MResetX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: a16d7405388b560edcdb6c36b6668791f7ba1398
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709079"
---
# <a name="mresetx-operation"></a><span data-ttu-id="4d594-102">Bewerking MResetX</span><span class="sxs-lookup"><span data-stu-id="4d594-102">MResetX operation</span></span>

<span data-ttu-id="4d594-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="4d594-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="4d594-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4d594-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4d594-105">Hiermee wordt één Qubit in de X-eenheid gemeten en teruggezet naar een vaste begin status na de meting.</span><span class="sxs-lookup"><span data-stu-id="4d594-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="4d594-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4d594-106">Description</span></span>

<span data-ttu-id="4d594-107">Voert een meting met één Qubit uit in de $X $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.</span><span class="sxs-lookup"><span data-stu-id="4d594-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="4d594-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="4d594-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="4d594-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4d594-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4d594-110">Eén Qubit die moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="4d594-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="4d594-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="4d594-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="4d594-112">Het resultaat van het meten van `target` de Pauli-$X $ soort_jaar.</span><span class="sxs-lookup"><span data-stu-id="4d594-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>