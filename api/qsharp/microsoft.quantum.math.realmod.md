---
uid: Microsoft.Quantum.Math.RealMod
title: De functie RealMod
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848348"
---
# <a name="realmod-function"></a><span data-ttu-id="59ae0-102">De functie RealMod</span><span class="sxs-lookup"><span data-stu-id="59ae0-102">RealMod function</span></span>

<span data-ttu-id="59ae0-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="59ae0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="59ae0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59ae0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59ae0-105">Berekent de modulus tussen twee reële getallen.</span><span class="sxs-lookup"><span data-stu-id="59ae0-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="59ae0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="59ae0-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="59ae0-107">waarde: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59ae0-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="59ae0-108">Een reëel getal $x $ om de modulus van te maken.</span><span class="sxs-lookup"><span data-stu-id="59ae0-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="59ae0-109">modulo: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59ae0-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="59ae0-110">Een reëel getal voor het nemen van de modulus van $x $ ten opzichte van.</span><span class="sxs-lookup"><span data-stu-id="59ae0-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="59ae0-111">minValue: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59ae0-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="59ae0-112">De kleinste waarde die door deze functie moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="59ae0-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="59ae0-113">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59ae0-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="example"></a><span data-ttu-id="59ae0-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="59ae0-114">Example</span></span>

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a><span data-ttu-id="59ae0-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="59ae0-115">Remarks</span></span>

<span data-ttu-id="59ae0-116">Deze functie berekent de werkelijke modulus door de werkelijke lijn over de eenheids cirkel te verpakken en vervolgens de hoek op de eenheids cirkel te vinden die overeenkomt met de invoer.</span><span class="sxs-lookup"><span data-stu-id="59ae0-116">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="59ae0-117">De `minValue` invoer wordt vervolgens effectief opgegeven waar de eenheids cirkel moet worden geknipt.</span><span class="sxs-lookup"><span data-stu-id="59ae0-117">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>