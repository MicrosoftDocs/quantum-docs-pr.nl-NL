---
uid: Microsoft.Quantum.Bitwise.XBits
title: De functie XBits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: 91619803c7efe56e617b16637f5302aa0b7978ec
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705572"
---
# <a name="xbits-function"></a><span data-ttu-id="80ad9-102">De functie XBits</span><span class="sxs-lookup"><span data-stu-id="80ad9-102">XBits function</span></span>

<span data-ttu-id="80ad9-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="80ad9-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="80ad9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80ad9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80ad9-105">Retourneert een geheel getal dat de X-bits van een matrix van Pauli-Opera tors vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="80ad9-105">Returns an integer representing the X bits of an array of Pauli operators.</span></span>

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="80ad9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="80ad9-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="80ad9-107">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="80ad9-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="80ad9-108">Een matrix met Pauli-Opera tors die moeten worden weer gegeven als een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="80ad9-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="80ad9-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="80ad9-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="80ad9-110">Een geheel getal $x $ met binaire weer gave $ (p_ {62} \, p_ {61} \, \dots \, p_0) $, waarbij $p _I = $0 als `paulis[i]` is `PauliI` of en de $p `PauliZ` _I = $1 als dat zo `paulis[i]` is `PauliX` of `PauliY` .</span><span class="sxs-lookup"><span data-stu-id="80ad9-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliZ` and where $p_i = 1$ if `paulis[i]` is `PauliX` or `PauliY`.</span></span>

## <a name="remarks"></a><span data-ttu-id="80ad9-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="80ad9-111">Remarks</span></span>

<span data-ttu-id="80ad9-112">De functie wordt gegenereerd als de lengte van de `paulis` matrix groter is dan 63.</span><span class="sxs-lookup"><span data-stu-id="80ad9-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="80ad9-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="80ad9-113">See Also</span></span>

- [<span data-ttu-id="80ad9-114">Micro soft. Quantum. bitsgewijze. ZBits</span><span class="sxs-lookup"><span data-stu-id="80ad9-114">Microsoft.Quantum.Bitwise.ZBits</span></span>](xref:Microsoft.Quantum.Bitwise.ZBits)