---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Bewerking Trotter2ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 34b60934b67c19b2d1d718d68b85a2f0fffeab5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852020"
---
# <a name="trotter2implca-operation"></a><span data-ttu-id="74583-102">Bewerking Trotter2ImplCA</span><span class="sxs-lookup"><span data-stu-id="74583-102">Trotter2ImplCA operation</span></span>

<span data-ttu-id="74583-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="74583-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="74583-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="74583-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="74583-105">Implementatie van de tweede order Trotter – Suzuki integrator.</span><span class="sxs-lookup"><span data-stu-id="74583-105">Implementation of the second-order Trotter–Suzuki integrator.</span></span>

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="74583-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="74583-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="74583-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="74583-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="74583-108">Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.</span><span class="sxs-lookup"><span data-stu-id="74583-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="74583-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="74583-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="74583-110">Een bewerking die een index-invoer (type `Int` ) en een tijd-invoer (type `Double` ) en een Quantum register (type `'T` ) voor de ontleding accepteert.</span><span class="sxs-lookup"><span data-stu-id="74583-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) and a quantum register (type `'T`) for decomposition.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="74583-111">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="74583-111">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="74583-112">Vermenigvuldiger op grootte van elke stap van de simulatie.</span><span class="sxs-lookup"><span data-stu-id="74583-112">Multiplier on size of each step of the simulation.</span></span>


### <a name="target--t"></a><span data-ttu-id="74583-113">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="74583-113">target : 'T</span></span>

<span data-ttu-id="74583-114">Een Quantum registratie waarop de bewerkingen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="74583-114">A quantum register on which the operations act.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74583-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74583-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="74583-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="74583-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="74583-117">T</span><span class="sxs-lookup"><span data-stu-id="74583-117">'T</span></span>

<span data-ttu-id="74583-118">Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="74583-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="example"></a><span data-ttu-id="74583-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="74583-119">Example</span></span>

<span data-ttu-id="74583-120">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="74583-120">The following are equivalent:</span></span>

```qsharp
op(0, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(0, deltaT / 2.0, target);
```

<span data-ttu-id="74583-121">en</span><span class="sxs-lookup"><span data-stu-id="74583-121">and</span></span>

```qsharp
Trotter2ImplCA((2, op), deltaT, target);
```