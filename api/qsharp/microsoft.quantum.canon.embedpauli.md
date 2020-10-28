---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: De functie EmbedPauli
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: c78406aa4557834ac2bb40cf1847696d075e5135
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704188"
---
# <a name="embedpauli-function"></a><span data-ttu-id="7965a-102">De functie EmbedPauli</span><span class="sxs-lookup"><span data-stu-id="7965a-102">EmbedPauli function</span></span>

<span data-ttu-id="7965a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7965a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7965a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7965a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7965a-105">Op basis van een Qubit Pauli-operator en de index van een Qubit retourneert een multi-Qubit Pauli-operator met de opgegeven single-Qubit-operator in die index en `PauliI` op elke andere index.</span><span class="sxs-lookup"><span data-stu-id="7965a-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="7965a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7965a-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="7965a-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="7965a-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="7965a-108">Een Pauli-operator met één Qubit die op de opgegeven locatie moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="7965a-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="7965a-109">Locatie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7965a-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7965a-110">Een dergelijke index `output[location] == pauli` , waarbij `output` de uitvoer van deze functie is.</span><span class="sxs-lookup"><span data-stu-id="7965a-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="7965a-111">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7965a-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7965a-112">Lengte van de matrix die moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="7965a-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="7965a-113">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="7965a-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

