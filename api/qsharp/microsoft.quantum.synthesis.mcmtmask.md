---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Door de gebruiker gedefinieerd MCMTMask-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709294"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="ea8cb-102">Door de gebruiker gedefinieerd MCMTMask-type</span><span class="sxs-lookup"><span data-stu-id="ea8cb-102">MCMTMask user defined type</span></span>

<span data-ttu-id="ea8cb-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ea8cb-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ea8cb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ea8cb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ea8cb-105">Een type dat een meerdere beheerde Toffoli-Gate met meerdere doelen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="ea8cb-106">De eerste integer is een bitmasker voor regels voor besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="ea8cb-107">Bits-indexen die zijn ingesteld, komen overeen met beheer regel indexen.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="ea8cb-108">De tweede integer is een bitmasker voor doel lijnen.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="ea8cb-109">Bits-indexen die zijn ingesteld, komen overeen met doel regel indexen.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="ea8cb-110">De bits-indexen van beide gehele getallen moeten niet-aaneengesloten zijn.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="ea8cb-111">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="ea8cb-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="ea8cb-112">ControlMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea8cb-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="ea8cb-113">TargetMask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea8cb-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

