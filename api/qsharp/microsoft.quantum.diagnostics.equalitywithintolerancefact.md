---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: De functie EqualityWithinToleranceFact
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: ab7e43d951bf741926b15f27f94d176e88609d4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828751"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="bd9dd-102">De functie EqualityWithinToleranceFact</span><span class="sxs-lookup"><span data-stu-id="bd9dd-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="bd9dd-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="bd9dd-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="bd9dd-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bd9dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bd9dd-105">Vertegenwoordigt de claim die een klassieke drijvende-komma waarde de verwachte waarde heeft tot een gegeven absolute tolerantie.</span><span class="sxs-lookup"><span data-stu-id="bd9dd-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="bd9dd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bd9dd-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="bd9dd-107">werkelijk: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bd9dd-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bd9dd-108">Het getal dat moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="bd9dd-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="bd9dd-109">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bd9dd-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bd9dd-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="bd9dd-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="bd9dd-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bd9dd-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bd9dd-112">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="bd9dd-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bd9dd-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bd9dd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

