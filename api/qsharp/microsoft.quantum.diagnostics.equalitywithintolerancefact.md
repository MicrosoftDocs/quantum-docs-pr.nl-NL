---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: De functie EqualityWithinToleranceFact
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: 6ada2632974fddd6dd0fd8e4e6ab0866e4f29524
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201713"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="6fb36-102">De functie EqualityWithinToleranceFact</span><span class="sxs-lookup"><span data-stu-id="6fb36-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="6fb36-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6fb36-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6fb36-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6fb36-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6fb36-105">Vertegenwoordigt de claim die een klassieke drijvende-komma waarde de verwachte waarde heeft tot een gegeven absolute tolerantie.</span><span class="sxs-lookup"><span data-stu-id="6fb36-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="6fb36-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6fb36-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="6fb36-107">werkelijk: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6fb36-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6fb36-108">Het getal dat moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="6fb36-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="6fb36-109">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6fb36-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6fb36-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="6fb36-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="6fb36-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6fb36-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6fb36-112">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="6fb36-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6fb36-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6fb36-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

