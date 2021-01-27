---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: De functie EmbedPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: 0e6a93e22ee495abcc44bdf522e7c72c0981308b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840536"
---
# <a name="embedpauli-function"></a><span data-ttu-id="680c5-102">De functie EmbedPauli</span><span class="sxs-lookup"><span data-stu-id="680c5-102">EmbedPauli function</span></span>

<span data-ttu-id="680c5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="680c5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="680c5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="680c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="680c5-105">Op basis van een Qubit Pauli-operator en de index van een Qubit retourneert een multi-Qubit Pauli-operator met de opgegeven single-Qubit-operator in die index en `PauliI` op elke andere index.</span><span class="sxs-lookup"><span data-stu-id="680c5-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="680c5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="680c5-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="680c5-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="680c5-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="680c5-108">Een Pauli-operator met één Qubit die op de opgegeven locatie moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="680c5-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="680c5-109">Locatie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="680c5-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="680c5-110">Een dergelijke index `output[location] == pauli` , waarbij `output` de uitvoer van deze functie is.</span><span class="sxs-lookup"><span data-stu-id="680c5-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="680c5-111">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="680c5-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="680c5-112">Lengte van de matrix die moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="680c5-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="680c5-113">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="680c5-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="example"></a><span data-ttu-id="680c5-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="680c5-114">Example</span></span>

<span data-ttu-id="680c5-115">De matrix verkrijgen `[PauliI, PauliI, PauliX, PauliI]` :</span><span class="sxs-lookup"><span data-stu-id="680c5-115">To obtain the array `[PauliI, PauliI, PauliX, PauliI]`:</span></span>

```qsharp
EmbedPauli(PauliX, 2, 3);
```