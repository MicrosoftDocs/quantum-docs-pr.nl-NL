---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Functie _ComputeJordanWignerBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839532"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="f59a7-102">Functie _ComputeJordanWignerBitString</span><span class="sxs-lookup"><span data-stu-id="f59a7-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="f59a7-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="f59a7-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="f59a7-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f59a7-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f59a7-105">Berekent Z-onderdeel van Jordanië – Wigner teken reeks tussen fermion indices in een fermionic-operator met een even aantal aanmaak/Annihilation-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="f59a7-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="f59a7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f59a7-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="f59a7-107">nFermions: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f59a7-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f59a7-108">Het aantal fermions in het systeem.</span><span class="sxs-lookup"><span data-stu-id="f59a7-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="f59a7-109">idxFermions: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f59a7-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f59a7-110">indices van fermionic-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="f59a7-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f59a7-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f59a7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f59a7-112">Bitstring `Bool[]` waarop `true` een `PauliZ` moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f59a7-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>

## <a name="example"></a><span data-ttu-id="f59a7-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f59a7-113">Example</span></span>

<span data-ttu-id="f59a7-114">laat bitString = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); bitString is [False, False, False, True, True, True, False].</span><span class="sxs-lookup"><span data-stu-id="f59a7-114">let bitString = _ComputeJordanWignerBitString(6, [0,1,2,6]) ; // bitString is [false, false, false ,true, true, true, false].</span></span>