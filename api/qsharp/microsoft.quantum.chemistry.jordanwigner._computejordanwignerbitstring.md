---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Functie _ComputeJordanWignerBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 8121421a77174ef3e894381b281964b448e00a18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203940"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="99076-102">Functie _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="99076-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="99076-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="99076-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="99076-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="99076-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="99076-105">Berekent Z-onderdeel van Jordanië – Wigner teken reeks tussen fermion indices in een fermionic-operator met een even aantal aanmaak/Annihilation-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="99076-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="99076-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="99076-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="99076-107">nFermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99076-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99076-108">Het aantal fermions in het systeem.</span><span class="sxs-lookup"><span data-stu-id="99076-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="99076-109">idxFermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="99076-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="99076-110">indices van fermionic-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="99076-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="99076-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="99076-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="99076-112">Bitstring `Bool[]` waarop `true` een `PauliZ` moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="99076-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>