---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Bewerking SetToBasisState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: dfa054360a5e82b7ae6ec5a6d52e7d5fe566f42e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854629"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="99dbf-102">Bewerking SetToBasisState</span><span class="sxs-lookup"><span data-stu-id="99dbf-102">SetToBasisState operation</span></span>

<span data-ttu-id="99dbf-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="99dbf-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="99dbf-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="99dbf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="99dbf-105">Hiermee wordt een Qubit ingesteld op basis van de status van de berekening door de Qubit te meten en zo nodig een bit te spie gelen.</span><span class="sxs-lookup"><span data-stu-id="99dbf-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="99dbf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="99dbf-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="99dbf-107">gewenst: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="99dbf-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="99dbf-108">De basis status waarop de Qubit moet worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="99dbf-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="99dbf-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="99dbf-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="99dbf-110">De Qubit waarvan de status moet worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="99dbf-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="99dbf-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="99dbf-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="99dbf-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="99dbf-112">Remarks</span></span>

<span data-ttu-id="99dbf-113">Als een onvariante van deze bewerking, `M(q)` wordt direct na `SetToBasisState(result, q)` geretourneerd `result` .</span><span class="sxs-lookup"><span data-stu-id="99dbf-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>