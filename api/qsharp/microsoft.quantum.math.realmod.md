---
uid: Microsoft.Quantum.Math.RealMod
title: De functie RealMod
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 20916d8462288395384aa875bfae4f042ba6b6ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228250"
---
# <a name="realmod-function"></a><span data-ttu-id="8952b-102">De functie RealMod</span><span class="sxs-lookup"><span data-stu-id="8952b-102">RealMod function</span></span>

<span data-ttu-id="8952b-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8952b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8952b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8952b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8952b-105">Berekent de modulus tussen twee reële getallen.</span><span class="sxs-lookup"><span data-stu-id="8952b-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="8952b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8952b-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="8952b-107">waarde: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8952b-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8952b-108">Een reëel getal $x $ om de modulus van te maken.</span><span class="sxs-lookup"><span data-stu-id="8952b-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="8952b-109">modulo: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8952b-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8952b-110">Een reëel getal voor het nemen van de modulus van $x $ ten opzichte van.</span><span class="sxs-lookup"><span data-stu-id="8952b-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="8952b-111">minValue: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8952b-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8952b-112">De kleinste waarde die door deze functie moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8952b-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="8952b-113">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8952b-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="8952b-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8952b-114">Remarks</span></span>

<span data-ttu-id="8952b-115">Deze functie berekent de werkelijke modulus door de werkelijke lijn over de eenheids cirkel te verpakken en vervolgens de hoek op de eenheids cirkel te vinden die overeenkomt met de invoer.</span><span class="sxs-lookup"><span data-stu-id="8952b-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="8952b-116">De `minValue` invoer wordt vervolgens effectief opgegeven waar de eenheids cirkel moet worden geknipt.</span><span class="sxs-lookup"><span data-stu-id="8952b-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>