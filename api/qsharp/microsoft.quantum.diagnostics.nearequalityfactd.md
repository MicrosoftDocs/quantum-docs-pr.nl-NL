---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: De functie NearEqualityFactD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702615"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="f896e-102">De functie NearEqualityFactD</span><span class="sxs-lookup"><span data-stu-id="f896e-102">NearEqualityFactD function</span></span>

<span data-ttu-id="f896e-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f896e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f896e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f896e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f896e-105">Hierbij wordt bevestigd dat een klassieke drijvende-komma waarde de verwachte waarde heeft tot een kleine tolerantie van 1e-10.</span><span class="sxs-lookup"><span data-stu-id="f896e-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="f896e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f896e-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="f896e-107">werkelijk: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f896e-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f896e-108">Het getal dat moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="f896e-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="f896e-109">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f896e-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f896e-110">De verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="f896e-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f896e-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f896e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f896e-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f896e-112">Remarks</span></span>

<span data-ttu-id="f896e-113">Dit komt overeen <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> met een hardcoded tolerantie van $10 ^ {-10} $.</span><span class="sxs-lookup"><span data-stu-id="f896e-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>