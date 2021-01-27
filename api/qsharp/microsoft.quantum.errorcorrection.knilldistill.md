---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Bewerking KnillDistill
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 4eff99eebb1e271d240513f827c6e93973ef79a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853106"
---
# <a name="knilldistill-operation"></a><span data-ttu-id="71501-102">Bewerking KnillDistill</span><span class="sxs-lookup"><span data-stu-id="71501-102">KnillDistill operation</span></span>

<span data-ttu-id="71501-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="71501-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="71501-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71501-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71501-105">Implementeert het distillatie algoritme Knill Magic State.</span><span class="sxs-lookup"><span data-stu-id="71501-105">Implements the Knill magic state distillation algorithm.</span></span>

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a><span data-ttu-id="71501-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71501-106">Description</span></span>

<span data-ttu-id="71501-107">Gegeven op 15 geschatte kopieën van een magische status $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} \end{align}, $ $ levert een kopie van een hogere kwaliteit.</span><span class="sxs-lookup"><span data-stu-id="71501-107">Given 15 approximate copies of a magic state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1} \end{align}, $$ yields one higher-quality copy.</span></span>

## <a name="input"></a><span data-ttu-id="71501-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="71501-108">Input</span></span>

### <a name="roughmagic--qubit"></a><span data-ttu-id="71501-109">roughMagic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="71501-109">roughMagic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="71501-110">Een REGI ster van vijf tien qubits die geschatte kopieën van een magische status bevatten.</span><span class="sxs-lookup"><span data-stu-id="71501-110">A register of fifteen qubits containing approximate copies of a magic state.</span></span> <span data-ttu-id="71501-111">De volgende toepassing van deze destillatie procedure `roughMagic[0]` bevat één kopie van een hogere kwaliteit en de rest van het REGI ster wordt opnieuw ingesteld op de status $ \ket{00\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="71501-111">Following application of this distillation procedure, `roughMagic[0]` will contain one higher-quality copy, and the rest of the register will be reset to the $\ket{00\cdots 0}$ state.</span></span>



## <a name="output--bool"></a><span data-ttu-id="71501-112">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="71501-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="71501-113">Als `true` de procedure is geslaagd en de kopie van de hogere kwaliteit moet worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="71501-113">If `true`, then the procedure succeeded and the higher-quality copy should be accepted.</span></span> <span data-ttu-id="71501-114">Als `false` de procedure is mislukt en de status van het REGI ster moet worden beschouwd als niet-gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="71501-114">If `false`, the procedure failed, and the state of the register should be considered undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="71501-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="71501-115">Remarks</span></span>

<span data-ttu-id="71501-116">We volgen het algoritme van Knill.</span><span class="sxs-lookup"><span data-stu-id="71501-116">We follow the algorithm of Knill.</span></span>
<span data-ttu-id="71501-117">De huidige implementatie is echter veel van optimaal, omdat er te veel qubits worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71501-117">However, the present implementation is far from being optimal, as it uses too many qubits.</span></span>
<span data-ttu-id="71501-118">De magische statussen worden in deze routine geïnjecteerd, in welk geval er betere protocollen zijn.</span><span class="sxs-lookup"><span data-stu-id="71501-118">The magic states are injected in this routine, in which case there are better protocols.</span></span>

## <a name="references"></a><span data-ttu-id="71501-119">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="71501-119">References</span></span>

- [<span data-ttu-id="71501-120">Knill</span><span class="sxs-lookup"><span data-stu-id="71501-120">Knill</span></span>](https://arxiv.org/abs/quant-ph/0402171)