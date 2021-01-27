---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: De functie ExpandedCoefficients
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835627"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="878f4-102">De functie ExpandedCoefficients</span><span class="sxs-lookup"><span data-stu-id="878f4-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="878f4-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="878f4-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="878f4-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="878f4-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="878f4-105">Breidt de compacte weer gave van de Jordan-Wigner coëfficiënten uit om een een-op-een-toewijzing te verkrijgen tussen deze en Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="878f4-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="878f4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="878f4-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="878f4-107">coeff: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="878f4-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="878f4-108">Een matrix met coëfficiënten, zoals gelezen uit de gegevens structuur van de Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="878f4-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="878f4-109">termType: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="878f4-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="878f4-110">Het type Jordan-Wigner-term.</span><span class="sxs-lookup"><span data-stu-id="878f4-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="878f4-111">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="878f4-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="878f4-112">Uitgebreide matrices van coëfficiënten, één per Pauli term.</span><span class="sxs-lookup"><span data-stu-id="878f4-112">Expanded arrays of coefficients, one per Pauli term.</span></span>