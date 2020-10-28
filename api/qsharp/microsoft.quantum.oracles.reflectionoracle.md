---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Door de gebruiker gedefinieerd ReflectionOracle-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 8e35e7e508ea7e0c30ea2a70633f71a6c87d4be1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708742"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="7e0f1-102">Door de gebruiker gedefinieerd ReflectionOracle-type</span><span class="sxs-lookup"><span data-stu-id="7e0f1-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="7e0f1-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="7e0f1-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="7e0f1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e0f1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7e0f1-105">Vertegenwoordigt een weer spiegeling van Oracle.</span><span class="sxs-lookup"><span data-stu-id="7e0f1-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="7e0f1-106">Een reflectie-Oracle, $O $, heeft invoer:</span><span class="sxs-lookup"><span data-stu-id="7e0f1-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="7e0f1-107">De fase $ \phi $ waarmee de doorgevoerde subruimte wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="7e0f1-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="7e0f1-108">Het Qubit-REGI ster waarop de opgegeven reflectie moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7e0f1-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="7e0f1-109">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="7e0f1-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a><span data-ttu-id="7e0f1-110">ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7e0f1-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="7e0f1-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7e0f1-111">Remarks</span></span>

<span data-ttu-id="7e0f1-112">Deze Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ voert een gedeeltelijke reflectie uit op basis van een fase $ \phi $ over één zuivere status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="7e0f1-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>