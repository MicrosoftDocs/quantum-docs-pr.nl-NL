---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Bewerking ApplyXControlledOnTruthTableWithCleanTarget
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: b43a5351985339bcf7c1f2bbe03ae6dc6dfdd165
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709180"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a><span data-ttu-id="7c237-102">Bewerking ApplyXControlledOnTruthTableWithCleanTarget</span><span class="sxs-lookup"><span data-stu-id="7c237-102">ApplyXControlledOnTruthTableWithCleanTarget operation</span></span>

<span data-ttu-id="7c237-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7c237-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7c237-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c237-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c237-105">De bewerking wordt toegepast @"microsoft.quantum.intrinsic.x" op `target` als de Boole-functie `func` resulteert in waar voor de klassieke toewijzing in `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="7c237-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="7c237-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7c237-106">Description</span></span>

<span data-ttu-id="7c237-107">Met deze bewerking wordt een speciaal geval geïmplementeerd @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , waarbij de doel-Qubit bekend staat als de $ \ket $- {0} status.</span><span class="sxs-lookup"><span data-stu-id="7c237-107">This operation implements a special case of @"microsoft.quantum.synthesis.applyxcontrolledontruthtable", in which the target qubit is known to be in the $\ket{0}$ state.</span></span>

<span data-ttu-id="7c237-108">De implementatie maakt gebruik van @"microsoft.quantum.intrinsic.cnot" en @"microsoft.quantum.intrinsic.r1" poorten.</span><span class="sxs-lookup"><span data-stu-id="7c237-108">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>  <span data-ttu-id="7c237-109">De implementatie van de adjoint-bewerking is geoptimaliseerd en maakt gebruik van op metingen gebaseerde onreken bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="7c237-109">The implementation of the adjoint operation is optimized and uses measurement-based uncomputation.</span></span>

## <a name="input"></a><span data-ttu-id="7c237-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="7c237-110">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="7c237-111">FUNC: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7c237-111">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7c237-112">Tabel met Boole-waarheid wordt weer gegeven als Big-geheel getal</span><span class="sxs-lookup"><span data-stu-id="7c237-112">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="7c237-113">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7c237-113">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7c237-114">REGI ster van controle qubits</span><span class="sxs-lookup"><span data-stu-id="7c237-114">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="7c237-115">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7c237-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7c237-116">Doel-Qubit (moet de status $ \ket {0} $ hebben)</span><span class="sxs-lookup"><span data-stu-id="7c237-116">Target qubit (must be in $\ket{0}$ state)</span></span>



## <a name="output--unit"></a><span data-ttu-id="7c237-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c237-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="7c237-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7c237-118">See Also</span></span>

- [<span data-ttu-id="7c237-119">Micro soft. Quantum. synthese. ApplyXControlledOnTruthTable</span><span class="sxs-lookup"><span data-stu-id="7c237-119">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)