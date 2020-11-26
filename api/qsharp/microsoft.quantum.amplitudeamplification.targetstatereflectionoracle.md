---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: De functie TargetStateReflectionOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191105"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="7cb28-102">De functie TargetStateReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="7cb28-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="7cb28-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="7cb28-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="7cb28-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7cb28-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7cb28-105">Bouwt `ReflectionOracle` over de doel status die uniek is gemarkeerd door de vlag Qubit.</span><span class="sxs-lookup"><span data-stu-id="7cb28-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="7cb28-106">Voor de doel status is één Qubit ingesteld op 1 en alle andere 0: $ \ket {1} _f $.</span><span class="sxs-lookup"><span data-stu-id="7cb28-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="7cb28-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="7cb28-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="7cb28-108">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7cb28-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7cb28-109">Index om Qubit $f $ van Oracle te markeren.</span><span class="sxs-lookup"><span data-stu-id="7cb28-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="7cb28-110">Uitvoer: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="7cb28-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="7cb28-111">Een `ReflectionOracle` die overeenkomt met de status die is gemarkeerd door $ \ket {1} _f $.</span><span class="sxs-lookup"><span data-stu-id="7cb28-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cb28-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7cb28-112">See Also</span></span>

- [<span data-ttu-id="7cb28-113">Micro soft. Quantum. Canon. ReflectionOracle</span><span class="sxs-lookup"><span data-stu-id="7cb28-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)