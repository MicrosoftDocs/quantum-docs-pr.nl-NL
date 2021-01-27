---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Bewerking Trotter1ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 6de4b6e7a34d66037d83a6e2bd5821402207c743
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840110"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="68c4d-102">Bewerking Trotter1ImplCA</span><span class="sxs-lookup"><span data-stu-id="68c4d-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="68c4d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="68c4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="68c4d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="68c4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="68c4d-105">Implementatie van de first-order Trotter – Suzuki integrator.</span><span class="sxs-lookup"><span data-stu-id="68c4d-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="68c4d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="68c4d-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="68c4d-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="68c4d-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="68c4d-108">Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.</span><span class="sxs-lookup"><span data-stu-id="68c4d-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="68c4d-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="68c4d-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="68c4d-110">Een bewerking die een index-invoer (type `Int` ) en een tijd-invoer (type `Double` ) en een Quantum register (type `'T` ) voor de ontleding accepteert.</span><span class="sxs-lookup"><span data-stu-id="68c4d-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="68c4d-111">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="68c4d-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="68c4d-112">Vermenigvuldiger op grootte van elke stap van de simulatie.</span><span class="sxs-lookup"><span data-stu-id="68c4d-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="68c4d-113">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="68c4d-113">target : 'T</span></span>

<span data-ttu-id="68c4d-114">Een Quantum registratie waarop de bewerkingen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="68c4d-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="68c4d-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="68c4d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="68c4d-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="68c4d-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="68c4d-117">T</span><span class="sxs-lookup"><span data-stu-id="68c4d-117">'T</span></span>

<span data-ttu-id="68c4d-118">Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="68c4d-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="68c4d-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="68c4d-119">Example</span></span>

<span data-ttu-id="68c4d-120">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="68c4d-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT, target);
op(1, deltaT, target);
```

<span data-ttu-id="68c4d-121">en</span><span class="sxs-lookup"><span data-stu-id="68c4d-121">and</span></span>

```qsharp
Trotter1ImplCA((2, op), deltaT, target);
```