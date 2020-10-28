---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Functie _ComputeJordanWignerBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 31b957a435c3f578bc03d432609cde14c2ef5ced
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703496"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="bd9f4-102">Functie _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="bd9f4-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="bd9f4-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="bd9f4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bd9f4-105">Berekent Z-onderdeel van Jordanië – Wigner teken reeks tussen fermion indices in een fermionic-operator met een even aantal aanmaak/Annihilation-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="bd9f4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bd9f4-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="bd9f4-107">nFermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bd9f4-108">Het aantal fermions in het systeem.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="bd9f4-109">idxFermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="bd9f4-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="bd9f4-110">indices van fermionic-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bd9f4-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="bd9f4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="bd9f4-112">Bitstring `Bool[]` waarop `true` een `PauliZ` moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>