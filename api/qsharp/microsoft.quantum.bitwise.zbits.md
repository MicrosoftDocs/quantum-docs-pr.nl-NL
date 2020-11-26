---
uid: Microsoft.Quantum.Bitwise.ZBits
title: De functie ZBits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: 3ded981dc53236a48f1fb8f6ae12e39c17469447
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219444"
---
# <a name="zbits-function"></a><span data-ttu-id="ece36-102">De functie ZBits</span><span class="sxs-lookup"><span data-stu-id="ece36-102">ZBits function</span></span>

<span data-ttu-id="ece36-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="ece36-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="ece36-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ece36-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ece36-105">Retourneert een geheel getal dat de Z-bits van een matrix van Pauli-Opera tors vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="ece36-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="ece36-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ece36-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="ece36-107">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="ece36-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="ece36-108">Een matrix met Pauli-Opera tors die moeten worden weer gegeven als een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="ece36-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="ece36-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ece36-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ece36-110">Een geheel getal $x $ met binaire weer gave $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, waarbij $p _I = $0 als `paulis[i]` is `PauliI` of en de $p `PauliX` _I = $1 als dat zo `paulis[i]` is `PauliY` of `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="ece36-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece36-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ece36-111">Remarks</span></span>

<span data-ttu-id="ece36-112">De functie wordt gegenereerd als de lengte van de `paulis` matrix groter is dan 63.</span><span class="sxs-lookup"><span data-stu-id="ece36-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="ece36-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ece36-113">See Also</span></span>

- [<span data-ttu-id="ece36-114">Micro soft. Quantum. bitsgewijze. XBits</span><span class="sxs-lookup"><span data-stu-id="ece36-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)