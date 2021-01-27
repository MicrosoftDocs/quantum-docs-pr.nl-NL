---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Bewerking ApplyXControlledOnTruthTableWithCleanTarget
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: a54544cd026f26784bb0c41cb12187a8885ed9db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855537"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a><span data-ttu-id="b6894-102">Bewerking ApplyXControlledOnTruthTableWithCleanTarget</span><span class="sxs-lookup"><span data-stu-id="b6894-102">ApplyXControlledOnTruthTableWithCleanTarget operation</span></span>

<span data-ttu-id="b6894-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b6894-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b6894-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b6894-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b6894-105">De bewerking wordt toegepast @"microsoft.quantum.intrinsic.x" op `target` als de Boole-functie `func` resulteert in waar voor de klassieke toewijzing in `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="b6894-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b6894-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b6894-106">Description</span></span>

<span data-ttu-id="b6894-107">Met deze bewerking wordt een speciaal geval geïmplementeerd @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , waarbij de doel-Qubit bekend staat als de $ \ket $- {0} status.</span><span class="sxs-lookup"><span data-stu-id="b6894-107">This operation implements a special case of @"microsoft.quantum.synthesis.applyxcontrolledontruthtable", in which the target qubit is known to be in the $\ket{0}$ state.</span></span>

<span data-ttu-id="b6894-108">De implementatie maakt gebruik van @"microsoft.quantum.intrinsic.cnot" en @"microsoft.quantum.intrinsic.r1" poorten.</span><span class="sxs-lookup"><span data-stu-id="b6894-108">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>  <span data-ttu-id="b6894-109">De implementatie van de adjoint-bewerking is geoptimaliseerd en maakt gebruik van op metingen gebaseerde onreken bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="b6894-109">The implementation of the adjoint operation is optimized and uses measurement-based uncomputation.</span></span>

## <a name="input"></a><span data-ttu-id="b6894-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="b6894-110">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="b6894-111">FUNC: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b6894-111">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b6894-112">Tabel met Boole-waarheid wordt weer gegeven als Big-geheel getal</span><span class="sxs-lookup"><span data-stu-id="b6894-112">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="b6894-113">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b6894-113">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b6894-114">REGI ster van controle qubits</span><span class="sxs-lookup"><span data-stu-id="b6894-114">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b6894-115">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b6894-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b6894-116">Doel-Qubit (moet de status $ \ket {0} $ hebben)</span><span class="sxs-lookup"><span data-stu-id="b6894-116">Target qubit (must be in $\ket{0}$ state)</span></span>



## <a name="output--unit"></a><span data-ttu-id="b6894-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b6894-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="b6894-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b6894-118">See Also</span></span>

- [<span data-ttu-id="b6894-119">Micro soft. Quantum. synthese. ApplyXControlledOnTruthTable</span><span class="sxs-lookup"><span data-stu-id="b6894-119">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)