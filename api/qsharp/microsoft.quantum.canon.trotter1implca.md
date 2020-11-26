---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Bewerking Trotter1ImplCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1b4e0a9597f4f30b8e92ef91ff0780e7c7ecdc9b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204790"
---
# <a name="trotter1implca-operation"></a><span data-ttu-id="fc63a-102">Bewerking Trotter1ImplCA</span><span class="sxs-lookup"><span data-stu-id="fc63a-102">Trotter1ImplCA operation</span></span>

<span data-ttu-id="fc63a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fc63a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fc63a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc63a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc63a-105">Implementatie van de first-order Trotter – Suzuki integrator.</span><span class="sxs-lookup"><span data-stu-id="fc63a-105">Implementation of the first-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fc63a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fc63a-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="fc63a-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fc63a-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fc63a-108">Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.</span><span class="sxs-lookup"><span data-stu-id="fc63a-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="fc63a-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="fc63a-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="fc63a-110">Een bewerking die een index-invoer (type `Int` ) en een tijd-invoer (type `Double` ) en een Quantum register (type `'T` ) voor de ontleding accepteert.</span><span class="sxs-lookup"><span data-stu-id="fc63a-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="fc63a-111">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fc63a-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fc63a-112">Vermenigvuldiger op grootte van elke stap van de simulatie.</span><span class="sxs-lookup"><span data-stu-id="fc63a-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="fc63a-113">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="fc63a-113">target : 'T</span></span>

<span data-ttu-id="fc63a-114">Een Quantum registratie waarop de bewerkingen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fc63a-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fc63a-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fc63a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fc63a-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="fc63a-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fc63a-117">T</span><span class="sxs-lookup"><span data-stu-id="fc63a-117">'T</span></span>

<span data-ttu-id="fc63a-118">Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="fc63a-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>