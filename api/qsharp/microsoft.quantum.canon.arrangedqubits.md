---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: De functie ArrangedQubits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704500"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="c4202-102">De functie ArrangedQubits</span><span class="sxs-lookup"><span data-stu-id="c4202-102">ArrangedQubits function</span></span>

<span data-ttu-id="c4202-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c4202-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c4202-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4202-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4202-105">Besturings element, doel en helper qubits rangschikken op basis van een index</span><span class="sxs-lookup"><span data-stu-id="c4202-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="c4202-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c4202-106">Description</span></span>

<span data-ttu-id="c4202-107">Retourneert een Qubit-matrix met het doel bij index 0 en Control i op index 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="c4202-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="c4202-108">De helper qubits worden ingevoegd op alle andere posities in de matrix.</span><span class="sxs-lookup"><span data-stu-id="c4202-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="c4202-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="c4202-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="c4202-110">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c4202-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="c4202-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c4202-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="c4202-112">Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c4202-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="c4202-113">Uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c4202-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

