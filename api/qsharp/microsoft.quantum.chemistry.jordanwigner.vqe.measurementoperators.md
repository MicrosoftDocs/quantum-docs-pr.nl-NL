---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: De functie MeasurementOperators
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: a5ea9a776f522e927f2f4545bd417d35bda83994
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214344"
---
# <a name="measurementoperators-function"></a><span data-ttu-id="fdbe6-102">De functie MeasurementOperators</span><span class="sxs-lookup"><span data-stu-id="fdbe6-102">MeasurementOperators function</span></span>

<span data-ttu-id="fdbe6-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="fdbe6-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="fdbe6-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fdbe6-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="fdbe6-105">Berekent alle meet operatoren die vereist zijn voor het berekenen van de verwachting van een Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-105">Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.</span></span>

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="fdbe6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fdbe6-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="fdbe6-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fdbe6-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fdbe6-108">Het aantal qubits dat nodig is voor het simuleren van het molecuul systeem.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-108">The number of qubits required to simulate the molecular system.</span></span>


### <a name="indices--int"></a><span data-ttu-id="fdbe6-109">indices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fdbe6-109">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fdbe6-110">Een matrix met de indices van de Qubit waarop elke Pauli-operator wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-110">An array containing the indices of the qubit each Pauli operator is applied to.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="fdbe6-111">termType: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fdbe6-111">termType : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fdbe6-112">Het type Jordan-Wigner-term.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-112">The type of the Jordan-Wigner term.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="fdbe6-113">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="fdbe6-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="fdbe6-114">Een matrix met meet operatoren (elk een matrix van Pauli).</span><span class="sxs-lookup"><span data-stu-id="fdbe6-114">An array of measurement operators (each being an array of Pauli).</span></span>