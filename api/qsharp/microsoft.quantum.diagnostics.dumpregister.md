---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: De functie DumpRegister
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: a6d29dbf0525077fd804563f85f189740fdc0429
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702698"
---
# <a name="dumpregister-function"></a><span data-ttu-id="284ed-102">De functie DumpRegister</span><span class="sxs-lookup"><span data-stu-id="284ed-102">DumpRegister function</span></span>

<span data-ttu-id="284ed-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="284ed-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="284ed-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="284ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="284ed-105">De huidige status van de doel computer die aan de opgegeven qubits is gekoppeld, wordt gedumpt.</span><span class="sxs-lookup"><span data-stu-id="284ed-105">Dumps the current target machine's status associated with the given qubits.</span></span>

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="284ed-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="284ed-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="284ed-107">Locatie: 'T</span><span class="sxs-lookup"><span data-stu-id="284ed-107">location : 'T</span></span>

<span data-ttu-id="284ed-108">Bevat informatie over waar de dump van de status moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="284ed-108">Provides information on where to generate the state's dump.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="284ed-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="284ed-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="284ed-110">De lijst met qubits die moeten worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="284ed-110">The list of qubits to report.</span></span>



## <a name="output--unit"></a><span data-ttu-id="284ed-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="284ed-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="284ed-112">Geen.</span><span class="sxs-lookup"><span data-stu-id="284ed-112">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="284ed-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="284ed-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="284ed-114">T</span><span class="sxs-lookup"><span data-stu-id="284ed-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="284ed-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="284ed-115">Remarks</span></span>

<span data-ttu-id="284ed-116">Met deze methode kunt u de gegevens die zijn gekoppeld aan de status van de opgegeven qubits, in een bestand of een andere locatie dumpen.</span><span class="sxs-lookup"><span data-stu-id="284ed-116">This method allows you to dump the information associated with the state of the given qubits into a file or some other location.</span></span>
<span data-ttu-id="284ed-117">De werkelijke gegevens die worden gegenereerd en de semantiek van `location` zijn specifiek voor elke doel computer.</span><span class="sxs-lookup"><span data-stu-id="284ed-117">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="284ed-118">Het leveren van een lege tuple als locatie ( `()` ) betekent meestal dat de uitvoer naar de-console wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="284ed-118">However, providing an empty tuple as a location (`()`) typically means to generate the output to the console.</span></span>

<span data-ttu-id="284ed-119">Voor de lokale volledige status Simulator die is gedistribueerd als onderdeel van de Quantum Development Kit, verwacht deze methode een teken reeks met het pad naar een bestand waarin de status van de opgegeven qubits (bijvoorbeeld de functie Wave van het bijbehorende subsysteem) wordt geschreven als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitudes van de kans van het meten van de bijbehorende status vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="284ed-119">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the state of the given qubits (i.e. the wave function of the corresponding  subsystem) as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>
<span data-ttu-id="284ed-120">Als de opgegeven qubits Entangled zijn met andere Qubit en de status ervan niet kan worden gescheiden, wordt alleen gerapporteerd dat de qubits Entangled zijn.</span><span class="sxs-lookup"><span data-stu-id="284ed-120">If the given qubits are entangled with some other qubit and their state can't be separated, it just reports that the qubits are entangled.</span></span>