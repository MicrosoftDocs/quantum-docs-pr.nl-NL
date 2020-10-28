---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: De functie QuantumROM
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 8ba5c6fab4abcfaee7233df9535f22eea5f68c28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708203"
---
# <a name="quantumrom-function"></a><span data-ttu-id="75a63-102">De functie QuantumROM</span><span class="sxs-lookup"><span data-stu-id="75a63-102">QuantumROM function</span></span>

<span data-ttu-id="75a63-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="75a63-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="75a63-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="75a63-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="75a63-105">Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven.</span><span class="sxs-lookup"><span data-stu-id="75a63-105">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="75a63-106">Op basis van een lijst met $N $ coëfficiënten $ \ alpha_j $ wordt een unitary $U $ geretourneerd die gebruikmaakt van de Quantum-ROM-techniek voor het voorbereiden van een benadering $ \tilde\rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ van de zuivering van de dichtheids matrix $ \rho = \ sum_ {j = 0} ^ {N-1} \frac{ {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $.</span><span class="sxs-lookup"><span data-stu-id="75a63-106">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="75a63-107">In deze benadering is de fout $ \epsilon $ zo dat $ | p_j-\frac{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ en $ \| \tilde\rho-\rho \| \le \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="75a63-107">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="75a63-108">Met andere woorden, $ $ \begin{align} U\ket {0} ^ {\lceil\ log_2 N\rceil} \ Ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\Text{garbage} _J}.</span><span class="sxs-lookup"><span data-stu-id="75a63-108">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="75a63-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="75a63-109">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="75a63-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="75a63-110">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="75a63-111">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="75a63-111">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="75a63-112">De doel fout $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="75a63-112">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="75a63-113">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="75a63-113">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="75a63-114">Matrix van $N $-coëfficiënten waarmee de kans op basis status wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="75a63-114">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="75a63-115">Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="75a63-115">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit-adj--ctl"></a><span data-ttu-id="75a63-116">Output: (([int](xref:microsoft.quantum.lang-ref.int); ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="75a63-116">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="75a63-117">Eerste para meter</span><span class="sxs-lookup"><span data-stu-id="75a63-117">First parameter</span></span>

<span data-ttu-id="75a63-118">Een tuple `(x,(y,z))` waarbij `x = y + z` het totale aantal toegewezen qubits is, `y` het aantal qubits voor het `LittleEndian` REGI ster en `z` het aantal garbage qubits.</span><span class="sxs-lookup"><span data-stu-id="75a63-118">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="75a63-119">Tweede para meter</span><span class="sxs-lookup"><span data-stu-id="75a63-119">Second parameter</span></span>

<span data-ttu-id="75a63-120">De One-norm $ \ sum_j | \ alpha_j | $ van de coëfficiënt matrix.</span><span class="sxs-lookup"><span data-stu-id="75a63-120">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="75a63-121">Derde para meter</span><span class="sxs-lookup"><span data-stu-id="75a63-121">Third parameter</span></span>

<span data-ttu-id="75a63-122">De unitary $U $.</span><span class="sxs-lookup"><span data-stu-id="75a63-122">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="75a63-123">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="75a63-123">References</span></span>

- <span data-ttu-id="75a63-124">Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="75a63-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>