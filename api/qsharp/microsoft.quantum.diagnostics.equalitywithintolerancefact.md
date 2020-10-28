---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: De functie EqualityWithinToleranceFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702657"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="b19c1-102">De functie EqualityWithinToleranceFact</span><span class="sxs-lookup"><span data-stu-id="b19c1-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="b19c1-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b19c1-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b19c1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b19c1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b19c1-105">Vertegenwoordigt de claim die een klassieke drijvende-komma waarde de verwachte waarde heeft tot een gegeven absolute tolerantie.</span><span class="sxs-lookup"><span data-stu-id="b19c1-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="b19c1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b19c1-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="b19c1-107">werkelijk: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b19c1-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b19c1-108">Het getal dat moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="b19c1-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="b19c1-109">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b19c1-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b19c1-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="b19c1-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="b19c1-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b19c1-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b19c1-112">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="b19c1-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b19c1-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b19c1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

