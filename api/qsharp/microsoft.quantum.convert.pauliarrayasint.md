---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: De functie PauliArrayAsInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702926"
---
# <a name="pauliarrayasint-function"></a><span data-ttu-id="d0333-102">De functie PauliArrayAsInt</span><span class="sxs-lookup"><span data-stu-id="d0333-102">PauliArrayAsInt function</span></span>

<span data-ttu-id="d0333-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="d0333-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="d0333-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0333-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0333-105">Codeert een multi-Qubit Pauli-operator die wordt weer gegeven als een matrix van Pauli Opera tors met één Qubit in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="d0333-105">Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.</span></span>

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="d0333-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d0333-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="d0333-107">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d0333-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d0333-108">Een matrix van Maxi maal 31 Opera tors met één Qubit Pauli.</span><span class="sxs-lookup"><span data-stu-id="d0333-108">An array of at most 31 single-qubit Pauli operators.</span></span>



## <a name="output--int"></a><span data-ttu-id="d0333-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d0333-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d0333-110">Een unieke identificatie van een geheel getal `paulis` , zoals hieronder wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="d0333-110">An integer uniquely identifying `paulis`, as described below.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0333-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d0333-111">Remarks</span></span>

<span data-ttu-id="d0333-112">Elke Pauli-operator kan worden versleuteld met twee bits: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span><span class="sxs-lookup"><span data-stu-id="d0333-112">Each Pauli operator can be encoded using two bits: $$ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span></span>
<span data-ttu-id="d0333-113">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="d0333-113">\end{align} $$</span></span>

<span data-ttu-id="d0333-114">Met een matrix van Pauli-Opera tors `[P0, ..., Pn]` retourneert deze functie een geheel getal met een binaire expansie die is gevormd door het samen voegen van de toewijzingen van elke Pauli-operator in een big-endian-volg orde `bits(Pn) ... bits(P0)` .</span><span class="sxs-lookup"><span data-stu-id="d0333-114">Given an array of Pauli operators `[P0, ..., Pn]`, this function returns an integer with binary expansion formed by concatenating the mappings of each Pauli operator in big-endian order `bits(Pn) ... bits(P0)`.</span></span>