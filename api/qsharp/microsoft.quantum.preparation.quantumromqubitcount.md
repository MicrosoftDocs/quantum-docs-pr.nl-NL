---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: De functie QuantumROMQubitCount
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 988d5efa3e27cf5e9a276ab3ab443c10f88fe1ad
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708191"
---
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="2d56e-102">De functie QuantumROMQubitCount</span><span class="sxs-lookup"><span data-stu-id="2d56e-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="2d56e-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2d56e-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2d56e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2d56e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2d56e-105">Retourneert het totale aantal qubits dat moet worden toegewezen aan de bewerking die wordt geretourneerd door `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="2d56e-105">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="2d56e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2d56e-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="2d56e-107">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2d56e-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2d56e-108">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="2d56e-108">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="2d56e-109">nCoeffs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2d56e-109">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2d56e-110">Aantal coëfficiënten opgegeven in `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="2d56e-110">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="2d56e-111">Output: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))</span><span class="sxs-lookup"><span data-stu-id="2d56e-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="2d56e-112">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="2d56e-112">First parameter</span></span>

<span data-ttu-id="2d56e-113">Een tuple `(x,(y,z))` waarbij `x = y + z` het totale aantal toegewezen qubits is, `y` het aantal qubits voor het `LittleEndian` REGI ster en `z` het aantal garbage qubits.</span><span class="sxs-lookup"><span data-stu-id="2d56e-113">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>