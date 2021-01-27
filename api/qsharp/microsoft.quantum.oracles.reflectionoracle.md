---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Door de gebruiker gedefinieerd ReflectionOracle-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 1ef07126596b70d2c5574430656009116c34d2bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854495"
---
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="25d3c-102">Door de gebruiker gedefinieerd ReflectionOracle-type</span><span class="sxs-lookup"><span data-stu-id="25d3c-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="25d3c-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="25d3c-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="25d3c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25d3c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25d3c-105">Vertegenwoordigt een weer spiegeling van Oracle.</span><span class="sxs-lookup"><span data-stu-id="25d3c-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="25d3c-106">Een reflectie-Oracle, $O $, heeft invoer:</span><span class="sxs-lookup"><span data-stu-id="25d3c-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="25d3c-107">De fase $ \phi $ waarmee de doorgevoerde subruimte wordt gedraaid.</span><span class="sxs-lookup"><span data-stu-id="25d3c-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="25d3c-108">Het Qubit-REGI ster waarop de opgegeven reflectie moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="25d3c-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="25d3c-109">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="25d3c-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="25d3c-110">ApplyReflection: ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="25d3c-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="25d3c-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="25d3c-111">Remarks</span></span>

<span data-ttu-id="25d3c-112">Deze Oracle $O = \boldone-(1-e ^ {i \phi}) \ket{\psi}\bra{\psi} $ voert een gedeeltelijke reflectie uit op basis van een fase $ \phi $ over één zuivere status $ \ket{\psi} $.</span><span class="sxs-lookup"><span data-stu-id="25d3c-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>