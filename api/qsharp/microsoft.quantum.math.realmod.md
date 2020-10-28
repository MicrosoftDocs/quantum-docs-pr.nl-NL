---
uid: Microsoft.Quantum.Math.RealMod
title: De functie RealMod
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706797"
---
# <a name="realmod-function"></a><span data-ttu-id="c1c49-102">De functie RealMod</span><span class="sxs-lookup"><span data-stu-id="c1c49-102">RealMod function</span></span>

<span data-ttu-id="c1c49-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="c1c49-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="c1c49-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1c49-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1c49-105">Berekent de modulus tussen twee reële getallen.</span><span class="sxs-lookup"><span data-stu-id="c1c49-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="c1c49-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c1c49-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="c1c49-107">waarde: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1c49-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c1c49-108">Een reëel getal $x $ om de modulus van te maken.</span><span class="sxs-lookup"><span data-stu-id="c1c49-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="c1c49-109">modulo: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1c49-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c1c49-110">Een reëel getal voor het nemen van de modulus van $x $ ten opzichte van.</span><span class="sxs-lookup"><span data-stu-id="c1c49-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="c1c49-111">minValue: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1c49-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c1c49-112">De kleinste waarde die door deze functie moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c1c49-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="c1c49-113">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1c49-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="c1c49-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c1c49-114">Remarks</span></span>

<span data-ttu-id="c1c49-115">Deze functie berekent de werkelijke modulus door de werkelijke lijn over de eenheids cirkel te verpakken en vervolgens de hoek op de eenheids cirkel te vinden die overeenkomt met de invoer.</span><span class="sxs-lookup"><span data-stu-id="c1c49-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="c1c49-116">De `minValue` invoer wordt vervolgens effectief opgegeven waar de eenheids cirkel moet worden geknipt.</span><span class="sxs-lookup"><span data-stu-id="c1c49-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>