---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: De functie ExpandedCoefficients
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 92d7deb7010791e7de3d22ad4616b20110d5e84e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214378"
---
# <a name="expandedcoefficients-function"></a><span data-ttu-id="b25d1-102">De functie ExpandedCoefficients</span><span class="sxs-lookup"><span data-stu-id="b25d1-102">ExpandedCoefficients function</span></span>

<span data-ttu-id="b25d1-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="b25d1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="b25d1-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b25d1-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b25d1-105">Breidt de compacte weer gave van de Jordan-Wigner coëfficiënten uit om een een-op-een-toewijzing te verkrijgen tussen deze en Pauli-voor waarden.</span><span class="sxs-lookup"><span data-stu-id="b25d1-105">Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.</span></span>

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="b25d1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b25d1-106">Input</span></span>

### <a name="coeff--double"></a><span data-ttu-id="b25d1-107">coeff: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b25d1-107">coeff : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b25d1-108">Een matrix met coëfficiënten, zoals gelezen uit de gegevens structuur van de Jordan-Wigner Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="b25d1-108">An array of coefficients, as read from the Jordan-Wigner Hamiltonian data structure.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="b25d1-109">termType: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b25d1-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b25d1-110">Het type Jordan-Wigner-term.</span><span class="sxs-lookup"><span data-stu-id="b25d1-110">The type of the Jordan-Wigner term.</span></span>



## <a name="output--double"></a><span data-ttu-id="b25d1-111">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b25d1-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b25d1-112">Uitgebreide matrices van coëfficiënten, één per Pauli term.</span><span class="sxs-lookup"><span data-stu-id="b25d1-112">Expanded arrays of coefficients, one per Pauli term.</span></span>