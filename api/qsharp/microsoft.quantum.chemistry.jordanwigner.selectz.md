---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Bewerking SelectZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 171bbe28ce8f10ca4b213a94b23f8c049546e3bf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703106"
---
# <a name="selectz-operation"></a><span data-ttu-id="4455c-102">Bewerking SelectZ</span><span class="sxs-lookup"><span data-stu-id="4455c-102">SelectZ operation</span></span>

<span data-ttu-id="4455c-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="4455c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="4455c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4455c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4455c-105">Een unitary $U $ waarmee de Pauli $Z $-Gate wordt toegepast op een qubits $p $, voorwaarded op een index status $ \ket{p} $.</span><span class="sxs-lookup"><span data-stu-id="4455c-105">A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$.</span></span> <span data-ttu-id="4455c-106">Dat wil zeggen, $ $ \begin{align} U\ket {p} \ Ket {\ psi} = \ket{p}Z \_ p\ket {\ psi} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="4455c-106">That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$</span></span>

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4455c-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="4455c-107">Input</span></span>

### <a name="indexregister--littleendian"></a><span data-ttu-id="4455c-108">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4455c-108">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4455c-109">De status $ \ket{p} $ van dit REGI ster bepaalt de Qubit waarop $Z $ wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="4455c-109">The state $\ket{p}$ of this register determines the qubit on which $Z$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="4455c-110">targetRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4455c-110">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4455c-111">Het REGI ster van qubits waarop de Pauli-Opera tors worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4455c-111">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4455c-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4455c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

