---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: De functie DumpMachine
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: e7eb2dfce060b61e27deae31e3c1fc6dc3d7655c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202104"
---
# <a name="dumpmachine-function"></a><span data-ttu-id="82949-102">De functie DumpMachine</span><span class="sxs-lookup"><span data-stu-id="82949-102">DumpMachine function</span></span>

<span data-ttu-id="82949-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="82949-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="82949-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="82949-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="82949-105">De huidige status van de doel computer dumpen.</span><span class="sxs-lookup"><span data-stu-id="82949-105">Dumps the current target machine's status.</span></span>

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="82949-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="82949-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="82949-107">Locatie: 'T</span><span class="sxs-lookup"><span data-stu-id="82949-107">location : 'T</span></span>

<span data-ttu-id="82949-108">Bevat informatie over het genereren van de dump van de computer.</span><span class="sxs-lookup"><span data-stu-id="82949-108">Provides information on where to generate the machine's dump.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82949-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82949-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="82949-110">Geen.</span><span class="sxs-lookup"><span data-stu-id="82949-110">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="82949-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="82949-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="82949-112">T</span><span class="sxs-lookup"><span data-stu-id="82949-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="82949-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="82949-113">Remarks</span></span>

<span data-ttu-id="82949-114">Met deze methode kunt u informatie over de huidige status van de doel computer dumpen in een bestand of een andere locatie.</span><span class="sxs-lookup"><span data-stu-id="82949-114">This method allows you to dump information about the current status of the target machine into a file or some other location.</span></span>
<span data-ttu-id="82949-115">De werkelijke gegevens die worden gegenereerd en de semantiek van `location` zijn specifiek voor elke doel computer.</span><span class="sxs-lookup"><span data-stu-id="82949-115">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="82949-116">Het leveren van een lege tuple als locatie ( `()` ) of het weglaten van de `location` para meter betekent meestal dat de uitvoer naar de-console wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="82949-116">However, providing an empty tuple as a location (`()`) or just omitting the `location` parameter typically means to generate the output to the console.</span></span>

<span data-ttu-id="82949-117">Voor de lokale volledige status Simulator die is gedistribueerd als onderdeel van de Quantum Development Kit, verwacht deze methode een teken reeks met het pad naar een bestand waarin de functie Wave wordt geschreven als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitudes vertegenwoordigt van de kans op het meten van de bijbehorende status.</span><span class="sxs-lookup"><span data-stu-id="82949-117">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the wave function as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>