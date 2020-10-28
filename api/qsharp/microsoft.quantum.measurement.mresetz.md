---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Bewerking MResetZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 9f084b03504deea9fcf25e4c797c4bde3c97a995
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701931"
---
# <a name="mresetz-operation"></a><span data-ttu-id="319de-102">Bewerking MResetZ</span><span class="sxs-lookup"><span data-stu-id="319de-102">MResetZ operation</span></span>

<span data-ttu-id="319de-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="319de-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="319de-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="319de-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="319de-105">Hiermee wordt één Qubit in de Z-basis gemeten en teruggezet naar een vaste begin status na de meting.</span><span class="sxs-lookup"><span data-stu-id="319de-105">Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="319de-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="319de-106">Description</span></span>

<span data-ttu-id="319de-107">Voert een meting met één Qubit uit in de $Z $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.</span><span class="sxs-lookup"><span data-stu-id="319de-107">Performs a single-qubit measurement in the $Z$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="319de-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="319de-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="319de-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="319de-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="319de-110">Eén Qubit die moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="319de-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="319de-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="319de-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="319de-112">Het resultaat van het meten van `target` de Pauli-$Z $ soort_jaar.</span><span class="sxs-lookup"><span data-stu-id="319de-112">The result of measuring `target` in the Pauli $Z$ basis.</span></span>