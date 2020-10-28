---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Bewerking OptimizedBEXY
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 359d347fc57be46200a218646911a7a400b4a96d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703155"
---
# <a name="optimizedbexy-operation"></a><span data-ttu-id="51678-102">Bewerking OptimizedBEXY</span><span class="sxs-lookup"><span data-stu-id="51678-102">OptimizedBEXY operation</span></span>

<span data-ttu-id="51678-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="51678-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="51678-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51678-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51678-105">Een unitary $U $ die de teken reeks Pauli toepast op $ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 $ op qubits $0.. p $ op index $z \in \{ 0, 1 \} $ en $p $.</span><span class="sxs-lookup"><span data-stu-id="51678-105">A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$.</span></span> <span data-ttu-id="51678-106">Dat wil zeggen, $ $ \begin{align} U\ket {z} \ Ket {p} \ Ket {\ psi} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 \ket{\psi} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="51678-106">That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$</span></span>

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="51678-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="51678-107">Input</span></span>

### <a name="paulibasis--qubit"></a><span data-ttu-id="51678-108">pauliBasis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="51678-108">pauliBasis : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="51678-109">Als deze Qubit de status $ \ket {0} $ heeft, wordt $X $ toegepast.</span><span class="sxs-lookup"><span data-stu-id="51678-109">When this qubit is in state $\ket{0}$, $X$ is applied.</span></span> <span data-ttu-id="51678-110">Wanneer de status is ingesteld op $ \ket {1} $, wordt $Y $ toegepast.</span><span class="sxs-lookup"><span data-stu-id="51678-110">When it is in state $\ket{1}$, $Y$ is applied.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="51678-111">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="51678-111">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="51678-112">De status $ \ket{p} $ van dit REGI ster bepaalt de Qubit waarop $X $ of $Y $ wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="51678-112">The state $\ket{p}$ of this register determines the qubit on which $X$ or $Y$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="51678-113">targetRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="51678-113">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="51678-114">Het REGI ster van qubits waarop de Pauli-Opera tors worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="51678-114">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51678-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51678-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="51678-116">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="51678-116">References</span></span>

- <span data-ttu-id="51678-117">Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="51678-117">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>