---
uid: Microsoft.Quantum.Measurement.MResetY
title: Bewerking MResetY
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 2e41e76a46b68178a8a22b39131d6ca2a8c50b64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854643"
---
# <a name="mresety-operation"></a><span data-ttu-id="665c6-102">Bewerking MResetY</span><span class="sxs-lookup"><span data-stu-id="665c6-102">MResetY operation</span></span>

<span data-ttu-id="665c6-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="665c6-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="665c6-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="665c6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="665c6-105">Hiermee wordt één Qubit in de Y-eenheid gemeten en teruggezet naar een vaste begin status na de meting.</span><span class="sxs-lookup"><span data-stu-id="665c6-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="665c6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="665c6-106">Description</span></span>

<span data-ttu-id="665c6-107">Voert een meting met één Qubit uit in de $Y $-soort_jaar en zorgt ervoor dat de Qubit wordt geretourneerd naar $ \ket {0} $ na de meting.</span><span class="sxs-lookup"><span data-stu-id="665c6-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="665c6-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="665c6-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="665c6-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="665c6-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="665c6-110">Eén Qubit die moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="665c6-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="665c6-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="665c6-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="665c6-112">Het resultaat van het meten van `target` de Pauli-$Y $ soort_jaar.</span><span class="sxs-lookup"><span data-stu-id="665c6-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>