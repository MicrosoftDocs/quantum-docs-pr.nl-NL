---
uid: Microsoft.Quantum.Measurement.MResetY
title: Bewerking MResetY
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 36c6f227135b5ccaf1146fd7afdc8205d416c5dd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227026"
---
# <a name="mresety-operation"></a><span data-ttu-id="a9884-102">Bewerking MResetY</span><span class="sxs-lookup"><span data-stu-id="a9884-102">MResetY operation</span></span>

<span data-ttu-id="a9884-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="a9884-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="a9884-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a9884-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a9884-105">Hiermee wordt één Qubit in de Y-eenheid gemeten en teruggezet naar een vaste begin status na de meting.</span><span class="sxs-lookup"><span data-stu-id="a9884-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="a9884-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9884-106">Description</span></span>

<span data-ttu-id="a9884-107">Voert een meting met één Qubit uit in de $Y $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.</span><span class="sxs-lookup"><span data-stu-id="a9884-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="a9884-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="a9884-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="a9884-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a9884-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a9884-110">Eén Qubit die moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="a9884-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a9884-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a9884-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="a9884-112">Het resultaat van het meten van `target` de Pauli-$Y $ soort_jaar.</span><span class="sxs-lookup"><span data-stu-id="a9884-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>