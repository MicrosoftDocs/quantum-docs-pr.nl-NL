---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: De functie ArrangedQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841078"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="8df8d-102">De functie ArrangedQubits</span><span class="sxs-lookup"><span data-stu-id="8df8d-102">ArrangedQubits function</span></span>

<span data-ttu-id="8df8d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8df8d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8df8d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8df8d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8df8d-105">Besturings element, doel en helper qubits rangschikken op basis van een index</span><span class="sxs-lookup"><span data-stu-id="8df8d-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="8df8d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8df8d-106">Description</span></span>

<span data-ttu-id="8df8d-107">Retourneert een Qubit-matrix met het doel bij index 0 en Control i op index 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="8df8d-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="8df8d-108">De helper qubits worden ingevoegd op alle andere posities in de matrix.</span><span class="sxs-lookup"><span data-stu-id="8df8d-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="8df8d-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="8df8d-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="8df8d-110">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8df8d-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="8df8d-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8df8d-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="8df8d-112">Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8df8d-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="8df8d-113">Uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8df8d-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

