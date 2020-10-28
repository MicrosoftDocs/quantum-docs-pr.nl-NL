---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Bewerking EstimateTermExpectation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703077"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="1b605-102">Bewerking EstimateTermExpectation</span><span class="sxs-lookup"><span data-stu-id="1b605-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="1b605-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="1b605-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="1b605-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1b605-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1b605-105">Hiermee wordt de energie berekend die is gekoppeld aan een bepaalde Jordan-Wigner Hamiltonian-term</span><span class="sxs-lookup"><span data-stu-id="1b605-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="1b605-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1b605-106">Description</span></span>

<span data-ttu-id="1b605-107">Met deze bewerking wordt de verwachte waarde voor elke meet operator geschat en wordt deze vermenigvuldigd met de overeenkomstige coëfficiënt, met behulp van steek proeven.</span><span class="sxs-lookup"><span data-stu-id="1b605-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="1b605-108">De resultaten worden geaggregeerd in een variabele die de energie van de Jordan-Wigner term bevat.</span><span class="sxs-lookup"><span data-stu-id="1b605-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="1b605-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="1b605-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit-adj"></a><span data-ttu-id="1b605-110">inputStateUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="1b605-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="1b605-111">De unitary die wordt gebruikt voor het voorbereiden van de status.</span><span class="sxs-lookup"><span data-stu-id="1b605-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="1b605-112">Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="1b605-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="1b605-113">De meet operatoren van de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="1b605-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="1b605-114">coeffs: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="1b605-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="1b605-115">De coëfficiënten van de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="1b605-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="1b605-116">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1b605-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1b605-117">Het aantal qubits dat nodig is voor het simuleren van het molecuul systeem.</span><span class="sxs-lookup"><span data-stu-id="1b605-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="1b605-118">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1b605-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1b605-119">Het aantal steek proeven dat moet worden gebruikt voor de schatting van de verwachting van de term.</span><span class="sxs-lookup"><span data-stu-id="1b605-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="1b605-120">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1b605-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1b605-121">De energie die is gekoppeld aan de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="1b605-121">The energy associated to the Jordan-Wigner term.</span></span>