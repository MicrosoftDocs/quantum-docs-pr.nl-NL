---
uid: Microsoft.Quantum.Canon.RAll0
title: Bewerking RAll0
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll0
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.
ms.openlocfilehash: 6185e66e08d2af3aa0b35791638820b4dcc5af35
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703893"
---
# <a name="rall0-operation"></a><span data-ttu-id="05a95-102">Bewerking RAll0</span><span class="sxs-lookup"><span data-stu-id="05a95-102">RAll0 operation</span></span>

<span data-ttu-id="05a95-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="05a95-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="05a95-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="05a95-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="05a95-105">Hiermee wordt een bewerking voor fase verschuiving uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="05a95-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="05a95-106">$R = \boldone-(1-e ^ {i \phi}) \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="05a95-106">$R=\boldone-(1-e^{i \phi})\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>

```qsharp
operation RAll0 (phase : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="05a95-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="05a95-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="05a95-108">fase: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="05a95-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="05a95-109">De fase $ \phi $ toegepast op status $ \ket{0\cdots 0} \bra{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="05a95-109">The phase $\phi$ applied to state $\ket{0\cdots 0}\bra{0\cdots 0}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="05a95-110">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="05a95-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="05a95-111">Het REGI ster waarvan de status moet worden geroteerd door $R $.</span><span class="sxs-lookup"><span data-stu-id="05a95-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="05a95-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="05a95-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="05a95-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="05a95-113">See Also</span></span>

- [<span data-ttu-id="05a95-114">Micro soft. Quantum. Canon. RAll1</span><span class="sxs-lookup"><span data-stu-id="05a95-114">Microsoft.Quantum.Canon.RAll1</span></span>](xref:Microsoft.Quantum.Canon.RAll1)