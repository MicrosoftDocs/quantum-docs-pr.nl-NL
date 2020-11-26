---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Bewerking RecoverCSS
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: eb01b1b9fccc19f0e3f1fd5ee596b95d0d61563f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200540"
---
# <a name="recovercss-operation"></a><span data-ttu-id="85cd2-102">Bewerking RecoverCSS</span><span class="sxs-lookup"><span data-stu-id="85cd2-102">RecoverCSS operation</span></span>

<span data-ttu-id="85cd2-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="85cd2-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="85cd2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85cd2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85cd2-105">Voert één afronding van de fout correctie uit op basis van een Quantum code die wordt beschreven door een `CSS` type.</span><span class="sxs-lookup"><span data-stu-id="85cd2-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="85cd2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="85cd2-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="85cd2-107">code: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="85cd2-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="85cd2-108">Een Quantum CSS-fout: de code die is verpakt als een `CSS` type wordt beschreven in een beschrijving van de code ring en het decoderen van Quantum gegevens en hoe fout-Syndromes worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="85cd2-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="85cd2-109">fnX: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="85cd2-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="85cd2-110">Een `RecoveryFn` waarmee elke $X $ error Syndrome wordt toegewezen aan de `Pauli[]` bewerkingen die de gedetecteerde fout corrigeren.</span><span class="sxs-lookup"><span data-stu-id="85cd2-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="85cd2-111">fnZ: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="85cd2-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="85cd2-112">Een `RecoveryFn` waarmee elke $Z $ error Syndrome wordt toegewezen aan de `Pauli[]` bewerkingen die de gedetecteerde fout corrigeren.</span><span class="sxs-lookup"><span data-stu-id="85cd2-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="85cd2-113">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="85cd2-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="85cd2-114">Een matrix met qubits waarvan de stabilisatorer code is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="85cd2-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85cd2-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85cd2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="85cd2-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="85cd2-116">See Also</span></span>

- [<span data-ttu-id="85cd2-117">Micro soft. Quantum. ErrorCorrection. CSS</span><span class="sxs-lookup"><span data-stu-id="85cd2-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="85cd2-118">Micro soft. Quantum. ErrorCorrection. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="85cd2-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="85cd2-119">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="85cd2-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)