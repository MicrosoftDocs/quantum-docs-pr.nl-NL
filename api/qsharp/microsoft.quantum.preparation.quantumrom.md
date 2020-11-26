---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: De functie QuantumROM
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229882"
---
# <a name="quantumrom-function"></a><span data-ttu-id="27e59-102">De functie QuantumROM</span><span class="sxs-lookup"><span data-stu-id="27e59-102">QuantumROM function</span></span>

<span data-ttu-id="27e59-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="27e59-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="27e59-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="27e59-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="27e59-105">QuantumROM is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="27e59-105">QuantumROM has been deprecated.</span></span> <span data-ttu-id="27e59-106">Gebruik <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="27e59-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.</span></span>

<span data-ttu-id="27e59-107">Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven.</span><span class="sxs-lookup"><span data-stu-id="27e59-107">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="27e59-108">Op basis van een lijst met $N $ coëfficiënten $ \ alpha_j $ wordt een unitary $U $ geretourneerd die gebruikmaakt van de Quantum-ROM-techniek voor het voorbereiden van een benadering $ \tilde\rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ van de zuivering van de dichtheids matrix $ \rho = \ sum_ {j = 0} ^ {N-1} \frac{ {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $.</span><span class="sxs-lookup"><span data-stu-id="27e59-108">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="27e59-109">In deze benadering is de fout $ \epsilon $ zo dat $ | p_j-\frac{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ en $ \| \tilde\rho-\rho \| \le \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="27e59-109">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="27e59-110">Met andere woorden, $ $ \begin{align} U\ket {0} ^ {\lceil\ log_2 N\rceil} \ Ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\Text{garbage} _J}.</span><span class="sxs-lookup"><span data-stu-id="27e59-110">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="27e59-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="27e59-111">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="27e59-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="27e59-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="27e59-113">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="27e59-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="27e59-114">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="27e59-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="27e59-115">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="27e59-115">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="27e59-116">Matrix van $N $-coëfficiënten waarmee de kans op basis status wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="27e59-116">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="27e59-117">Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="27e59-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="27e59-118">Output: (([int](xref:microsoft.quantum.lang-ref.int)[, int)](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit) is ADJ en CTL)</span><span class="sxs-lookup"><span data-stu-id="27e59-118">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="27e59-119">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="27e59-119">First parameter</span></span>

<span data-ttu-id="27e59-120">Een tuple `(x,(y,z))` waarbij `x = y + z` het totale aantal toegewezen qubits is, `y` het aantal qubits voor het `LittleEndian` REGI ster en `z` het aantal garbage qubits.</span><span class="sxs-lookup"><span data-stu-id="27e59-120">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="27e59-121">Tweede para meter</span><span class="sxs-lookup"><span data-stu-id="27e59-121">Second parameter</span></span>

<span data-ttu-id="27e59-122">De One-norm $ \ sum_j | \ alpha_j | $ van de coëfficiënt matrix.</span><span class="sxs-lookup"><span data-stu-id="27e59-122">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="27e59-123">Derde para meter</span><span class="sxs-lookup"><span data-stu-id="27e59-123">Third parameter</span></span>

<span data-ttu-id="27e59-124">De unitary $U $.</span><span class="sxs-lookup"><span data-stu-id="27e59-124">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="27e59-125">Referenties</span><span class="sxs-lookup"><span data-stu-id="27e59-125">References</span></span>

- <span data-ttu-id="27e59-126">Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="27e59-126">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>