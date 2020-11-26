---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Bewerking EstimateTermExpectation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 3f0ff5037b1424abb6fb318bd49ffd89f545822d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224646"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="d61b0-102">Bewerking EstimateTermExpectation</span><span class="sxs-lookup"><span data-stu-id="d61b0-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="d61b0-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="d61b0-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="d61b0-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d61b0-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d61b0-105">Hiermee wordt de energie berekend die is gekoppeld aan een bepaalde Jordan-Wigner Hamiltonian-term</span><span class="sxs-lookup"><span data-stu-id="d61b0-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="d61b0-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d61b0-106">Description</span></span>

<span data-ttu-id="d61b0-107">Met deze bewerking wordt de verwachte waarde voor elke meet operator geschat en wordt deze vermenigvuldigd met de overeenkomstige coëfficiënt, met behulp van steek proeven.</span><span class="sxs-lookup"><span data-stu-id="d61b0-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="d61b0-108">De resultaten worden geaggregeerd in een variabele die de energie van de Jordan-Wigner term bevat.</span><span class="sxs-lookup"><span data-stu-id="d61b0-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="d61b0-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="d61b0-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="d61b0-110">inputStateUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="d61b0-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d61b0-111">De unitary die wordt gebruikt voor het voorbereiden van de status.</span><span class="sxs-lookup"><span data-stu-id="d61b0-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="d61b0-112">Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="d61b0-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="d61b0-113">De meet operatoren van de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="d61b0-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="d61b0-114">coeffs: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d61b0-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d61b0-115">De coëfficiënten van de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="d61b0-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="d61b0-116">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d61b0-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d61b0-117">Het aantal qubits dat nodig is voor het simuleren van het molecuul systeem.</span><span class="sxs-lookup"><span data-stu-id="d61b0-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="d61b0-118">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d61b0-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d61b0-119">Het aantal steek proeven dat moet worden gebruikt voor de schatting van de verwachting van de term.</span><span class="sxs-lookup"><span data-stu-id="d61b0-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="d61b0-120">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d61b0-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d61b0-121">De energie die is gekoppeld aan de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="d61b0-121">The energy associated to the Jordan-Wigner term.</span></span>