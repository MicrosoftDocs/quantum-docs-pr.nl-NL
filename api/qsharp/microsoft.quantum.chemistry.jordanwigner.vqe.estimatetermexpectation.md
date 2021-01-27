---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Bewerking EstimateTermExpectation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835676"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="cbdab-102">Bewerking EstimateTermExpectation</span><span class="sxs-lookup"><span data-stu-id="cbdab-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="cbdab-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="cbdab-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="cbdab-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="cbdab-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="cbdab-105">Hiermee wordt de energie berekend die is gekoppeld aan een bepaalde Jordan-Wigner Hamiltonian-term</span><span class="sxs-lookup"><span data-stu-id="cbdab-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="cbdab-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="cbdab-106">Description</span></span>

<span data-ttu-id="cbdab-107">Met deze bewerking wordt de verwachte waarde voor elke meet operator geschat en wordt deze vermenigvuldigd met de overeenkomstige coëfficiënt, met behulp van steek proeven.</span><span class="sxs-lookup"><span data-stu-id="cbdab-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="cbdab-108">De resultaten worden geaggregeerd in een variabele die de energie van de Jordan-Wigner term bevat.</span><span class="sxs-lookup"><span data-stu-id="cbdab-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="cbdab-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="cbdab-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="cbdab-110">inputStateUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="cbdab-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="cbdab-111">De unitary die wordt gebruikt voor het voorbereiden van de status.</span><span class="sxs-lookup"><span data-stu-id="cbdab-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="cbdab-112">Ops: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="cbdab-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="cbdab-113">De meet operatoren van de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="cbdab-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="cbdab-114">coeffs: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="cbdab-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="cbdab-115">De coëfficiënten van de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="cbdab-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="cbdab-116">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbdab-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cbdab-117">Het aantal qubits dat nodig is voor het simuleren van het molecuul systeem.</span><span class="sxs-lookup"><span data-stu-id="cbdab-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="cbdab-118">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cbdab-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cbdab-119">Het aantal steek proeven dat moet worden gebruikt voor de schatting van de verwachting van de term.</span><span class="sxs-lookup"><span data-stu-id="cbdab-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="cbdab-120">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cbdab-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cbdab-121">De energie die is gekoppeld aan de Jordan-Wigner term.</span><span class="sxs-lookup"><span data-stu-id="cbdab-121">The energy associated to the Jordan-Wigner term.</span></span>