---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Bewerking TrotterArbitraryImplCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 2abfbb9d51a98d8ede1b0835875a3771ffda0691
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204722"
---
# <a name="trotterarbitraryimplca-operation"></a><span data-ttu-id="14334-102">Bewerking TrotterArbitraryImplCA</span><span class="sxs-lookup"><span data-stu-id="14334-102">TrotterArbitraryImplCA operation</span></span>

<span data-ttu-id="14334-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="14334-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="14334-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14334-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14334-105">Recursieve implementatie van even Trotter – Suzuki integrator.</span><span class="sxs-lookup"><span data-stu-id="14334-105">Recursive implementation of even-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="14334-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="14334-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="14334-107">Volg orde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14334-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14334-108">Volg orde van Trotter-Suzuki integrator.</span><span class="sxs-lookup"><span data-stu-id="14334-108">Order of Trotter-Suzuki integrator.</span></span>


### <a name="nsteps--int"></a><span data-ttu-id="14334-109">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="14334-109">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="14334-110">Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.</span><span class="sxs-lookup"><span data-stu-id="14334-110">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="14334-111">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="14334-111">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="14334-112">Een bewerking die een index-invoer (type `Int` ) en een tijd-invoer (type `Double` ) en een Quantum register (type `'T` ) voor de ontleding accepteert.</span><span class="sxs-lookup"><span data-stu-id="14334-112">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="14334-113">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="14334-113">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="14334-114">Vermenigvuldiger op grootte van elke stap van de simulatie.</span><span class="sxs-lookup"><span data-stu-id="14334-114">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="14334-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="14334-115">target : 'T</span></span>

<span data-ttu-id="14334-116">Een Quantum registratie waarop de bewerkingen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="14334-116">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="14334-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14334-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="14334-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="14334-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="14334-119">T</span><span class="sxs-lookup"><span data-stu-id="14334-119">'T</span></span>

<span data-ttu-id="14334-120">Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="14334-120">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>