---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Door de gebruiker gedefinieerd RequiresCapability-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 63b1952d402f1bcb81a8f9d0afc3cdf7aa7e5ed8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709138"
---
# <a name="requirescapability-user-defined-type"></a><span data-ttu-id="31bcc-102">Door de gebruiker gedefinieerd RequiresCapability-type</span><span class="sxs-lookup"><span data-stu-id="31bcc-102">RequiresCapability user defined type</span></span>

<span data-ttu-id="31bcc-103">Naam ruimte: [micro soft. Quantum. targeting](xref:Microsoft.Quantum.Targeting)</span><span class="sxs-lookup"><span data-stu-id="31bcc-103">Namespace: [Microsoft.Quantum.Targeting](xref:Microsoft.Quantum.Targeting)</span></span>

<span data-ttu-id="31bcc-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="31bcc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="31bcc-105">Compileer kenmerk dat wordt gebruikt voor het markeren van een aanroepable met de runtime-mogelijkheden die nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="31bcc-105">Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a><span data-ttu-id="31bcc-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="31bcc-106">Named Items</span></span>

### <a name="level--string"></a><span data-ttu-id="31bcc-107">Niveau: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="31bcc-107">Level : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="31bcc-108">De naam van het runtime-functionaliteits niveau dat is vereist voor de aanroepable.</span><span class="sxs-lookup"><span data-stu-id="31bcc-108">The name of the runtime capability level required by the callable.</span></span>
### <a name="reason--string"></a><span data-ttu-id="31bcc-109">Reden: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="31bcc-109">Reason : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="31bcc-110">Een beschrijving van waarom de aanroepable vereist is voor deze runtime-functie.</span><span class="sxs-lookup"><span data-stu-id="31bcc-110">A description of why the callable requires this runtime capability.</span></span>

## <a name="remarks"></a><span data-ttu-id="31bcc-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="31bcc-111">Remarks</span></span>

<span data-ttu-id="31bcc-112">Dit kenmerk wordt automatisch toegevoegd aan callables door de compiler, tenzij er al een exemplaar van dit kenmerk op de aanroepable bestaat.</span><span class="sxs-lookup"><span data-stu-id="31bcc-112">This attribute is automatically added to callables by the compiler, unless an instance of this attribute already exists on the callable.</span></span> <span data-ttu-id="31bcc-113">Het mag niet worden gebruikt, behalve in zeldzame gevallen waarbij de compiler de vereiste capaciteit niet correct afleiden.</span><span class="sxs-lookup"><span data-stu-id="31bcc-113">It should not be used except in rare cases where the compiler does not infer the required capability correctly.</span></span>

<span data-ttu-id="31bcc-114">Hieronder ziet u de lijst met namen van capabilities, in volg orde van toenemende mogelijkheden of het verminderen van de beperkingen:</span><span class="sxs-lookup"><span data-stu-id="31bcc-114">Below is the list of capability level names, in order of increasing capabilities or decreasing restrictions:</span></span>

## `"BasicQuantumFunctionality"`

<span data-ttu-id="31bcc-115">Meet resultaten kunnen niet worden vergeleken voor gelijkheid.</span><span class="sxs-lookup"><span data-stu-id="31bcc-115">Measurement results cannot be compared for equality.</span></span>

## `"BasicMeasurementFeedback"`

<span data-ttu-id="31bcc-116">Meet resultaten kunnen alleen worden vergeleken in if-instructie voorwaardelijke expressies in bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="31bcc-116">Measurement results can be compared for equality only in if-statement conditional expressions in operations.</span></span> <span data-ttu-id="31bcc-117">Het blok van een if-instructie dat afhankelijk is van een resultaat, mag geen set-instructies bevatten voor onveranderlijke variabelen die buiten de blok-of Return-instructies zijn gedeclareerd.</span><span class="sxs-lookup"><span data-stu-id="31bcc-117">The block of an if-statement that depends on a result cannot contain set statements for mutable variables declared outside the block, or return statements.</span></span>

## `"FullComputation"`

<span data-ttu-id="31bcc-118">Geen runtime-beperkingen.</span><span class="sxs-lookup"><span data-stu-id="31bcc-118">No runtime restrictions.</span></span> <span data-ttu-id="31bcc-119">Elk Q #-programma kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="31bcc-119">Any Q# program can be executed.</span></span>