---
uid: Microsoft.Quantum.Measurement.MResetY
title: Bewerking MResetY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 48aba7317d0e48d089ec6c4814efdee51bb8e2ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709084"
---
# <a name="mresety-operation"></a><span data-ttu-id="8f1ca-102">Bewerking MResetY</span><span class="sxs-lookup"><span data-stu-id="8f1ca-102">MResetY operation</span></span>

<span data-ttu-id="8f1ca-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="8f1ca-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="8f1ca-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8f1ca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8f1ca-105">Hiermee wordt één Qubit in de Y-eenheid gemeten en teruggezet naar een vaste begin status na de meting.</span><span class="sxs-lookup"><span data-stu-id="8f1ca-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="8f1ca-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8f1ca-106">Description</span></span>

<span data-ttu-id="8f1ca-107">Voert een meting met één Qubit uit in de $Y $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.</span><span class="sxs-lookup"><span data-stu-id="8f1ca-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="8f1ca-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="8f1ca-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="8f1ca-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f1ca-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f1ca-110">Eén Qubit die moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="8f1ca-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="8f1ca-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="8f1ca-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="8f1ca-112">Het resultaat van het meten van `target` de Pauli-$Y $ soort_jaar.</span><span class="sxs-lookup"><span data-stu-id="8f1ca-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>