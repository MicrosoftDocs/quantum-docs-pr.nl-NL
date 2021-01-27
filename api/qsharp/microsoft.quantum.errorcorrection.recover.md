---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Herstel bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: 3e2ce404ae3a6b4097897b859388fea3f915232c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825529"
---
# <a name="recover-operation"></a><span data-ttu-id="bc25f-102">Herstel bewerking</span><span class="sxs-lookup"><span data-stu-id="bc25f-102">Recover operation</span></span>

<span data-ttu-id="bc25f-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="bc25f-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="bc25f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bc25f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bc25f-105">Voert één afronding van de fout correctie uit op basis van een Quantum code die wordt beschreven door een `QECC` type.</span><span class="sxs-lookup"><span data-stu-id="bc25f-105">Performs a single round of error correction by a quantum code described by a `QECC` type.</span></span>

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="bc25f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bc25f-106">Input</span></span>

### <a name="code--qecc"></a><span data-ttu-id="bc25f-107">code: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="bc25f-107">code : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="bc25f-108">Een Quantum fout: een code die is verpakt als `QECC` type, beschrijft de code ring en de code ring van Quantum gegevens en hoe fout-Syndromes worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="bc25f-108">A quantum error-correcting code packaged as a `QECC` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fn--recoveryfn"></a><span data-ttu-id="bc25f-109">FN: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="bc25f-109">fn : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="bc25f-110">Een `RecoveryFn` waarmee elke fout Syndrome wordt toegewezen aan de `Pauli[]` bewerkingen die de gedetecteerde fout corrigeren.</span><span class="sxs-lookup"><span data-stu-id="bc25f-110">A `RecoveryFn` that maps each error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="bc25f-111">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="bc25f-111">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="bc25f-112">Een matrix met qubits waarvan de stabilisatorer code is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="bc25f-112">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc25f-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc25f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bc25f-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bc25f-114">See Also</span></span>

- [<span data-ttu-id="bc25f-115">Micro soft. Quantum. ErrorCorrection. QECC</span><span class="sxs-lookup"><span data-stu-id="bc25f-115">Microsoft.Quantum.ErrorCorrection.QECC</span></span>](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [<span data-ttu-id="bc25f-116">Micro soft. Quantum. ErrorCorrection. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="bc25f-116">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="bc25f-117">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="bc25f-117">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)