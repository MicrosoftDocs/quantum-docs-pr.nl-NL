---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Door de gebruiker gedefinieerd ReflectionOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226652"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="5896d-102">Door de gebruiker gedefinieerd ReflectionOracle-type</span><span class="sxs-lookup"><span data-stu-id="5896d-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="5896d-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="5896d-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="5896d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5896d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5896d-105">Vertegenwoordigt een weer spiegeling van Oracle.</span><span class="sxs-lookup"><span data-stu-id="5896d-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="5896d-106">Een reflectie-Oracle, $O $, heeft invoer:</span><span class="sxs-lookup"><span data-stu-id="5896d-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="5896d-107">De fase $ \phi $ waarmee de doorgevoerde subruimte wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="5896d-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="5896d-108">Het Qubit-REGI ster waarop de opgegeven reflectie moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5896d-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="5896d-109">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="5896d-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="5896d-110">ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="5896d-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="5896d-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5896d-111">Remarks</span></span>

<span data-ttu-id="5896d-112">Deze Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ voert een gedeeltelijke reflectie uit op basis van een fase $ \phi $ over één zuivere status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="5896d-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>