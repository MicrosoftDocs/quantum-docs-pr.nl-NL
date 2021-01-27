---
uid: Microsoft.Quantum.Bitwise.ZBits
title: De functie ZBits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: d1ddc2a4cdbdfd3945885de856456b3108592594
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842061"
---
# <a name="zbits-function"></a><span data-ttu-id="caab4-102">De functie ZBits</span><span class="sxs-lookup"><span data-stu-id="caab4-102">ZBits function</span></span>

<span data-ttu-id="caab4-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="caab4-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="caab4-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="caab4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="caab4-105">Retourneert een geheel getal dat de Z-bits van een matrix van Pauli-Opera tors vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="caab4-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="caab4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="caab4-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="caab4-107">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="caab4-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="caab4-108">Een matrix met Pauli-Opera tors die moeten worden weer gegeven als een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="caab4-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="caab4-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="caab4-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="caab4-110">Een geheel getal $x $ met binaire weer gave $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, waarbij $p _I = $0 als `paulis[i]` is `PauliI` of en de $p `PauliX` _I = $1 als dat zo `paulis[i]` is `PauliY` of `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="caab4-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="caab4-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="caab4-111">Remarks</span></span>

<span data-ttu-id="caab4-112">De functie wordt gegenereerd als de lengte van de `paulis` matrix groter is dan 63.</span><span class="sxs-lookup"><span data-stu-id="caab4-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="caab4-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="caab4-113">See Also</span></span>

- [<span data-ttu-id="caab4-114">Micro soft. Quantum. bitsgewijze. XBits</span><span class="sxs-lookup"><span data-stu-id="caab4-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)