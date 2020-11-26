---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: De functie QuantumROMQubitCount
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 0ec1e042b9f675505f73bfcdcc6706d0bc0367df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210400"
---
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="73885-102">De functie QuantumROMQubitCount</span><span class="sxs-lookup"><span data-stu-id="73885-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="73885-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="73885-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="73885-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73885-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="73885-105">QuantumROMQubitCount is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="73885-105">QuantumROMQubitCount has been deprecated.</span></span> <span data-ttu-id="73885-106">Gebruik <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="73885-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.</span></span>

<span data-ttu-id="73885-107">Retourneert het totale aantal qubits dat moet worden toegewezen aan de bewerking die wordt geretourneerd door `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="73885-107">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="73885-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="73885-108">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="73885-109">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73885-109">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73885-110">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="73885-110">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="73885-111">nCoeffs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73885-111">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73885-112">Aantal coëfficiënten opgegeven in `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="73885-112">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="73885-113">Output: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))</span><span class="sxs-lookup"><span data-stu-id="73885-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="73885-114">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="73885-114">First parameter</span></span>

<span data-ttu-id="73885-115">Een tuple `(x,(y,z))` waarbij `x = y + z` het totale aantal toegewezen qubits is, `y` het aantal qubits voor het `LittleEndian` REGI ster en `z` het aantal garbage qubits.</span><span class="sxs-lookup"><span data-stu-id="73885-115">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>