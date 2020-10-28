---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: De functie ExpandedCoefficients
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 8f5a2319b5839d0d9e47972389330dc16dffcaf0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703071"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="85d1e-102">De functie ExpandedCoefficients</span><span class="sxs-lookup"><span data-stu-id="85d1e-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="85d1e-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="85d1e-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="85d1e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="85d1e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="85d1e-105">Breidt de compacte weer gave van de Jordan-Wigner coëfficiënten uit om een een-op-een-toewijzing te verkrijgen tussen deze en Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="85d1e-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="85d1e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="85d1e-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="85d1e-107">coeff: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="85d1e-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="85d1e-108">Een matrix met coëfficiënten, zoals gelezen uit de gegevens structuur van de Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="85d1e-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="85d1e-109">termType: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="85d1e-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="85d1e-110">Het type Jordan-Wigner-term.</span><span class="sxs-lookup"><span data-stu-id="85d1e-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="85d1e-111">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="85d1e-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="85d1e-112">Uitgebreide matrices van coëfficiënten, één per Pauli term.</span><span class="sxs-lookup"><span data-stu-id="85d1e-112">Expanded arrays of coefficients, one per Pauli term.</span></span>