---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Bewerking ApproximateQFT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 31fd87c0f61292142c7493cc29cad1082a9a2d67
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850326"
---
# <a name="approximateqft-operation"></a><span data-ttu-id="c7497-102">Bewerking ApproximateQFT</span><span class="sxs-lookup"><span data-stu-id="c7497-102">ApproximateQFT operation</span></span>

<span data-ttu-id="c7497-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7497-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7497-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7497-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7497-105">De benadering van de Quantum Fourier-trans formatie (AQFT) Toep assen op een Quantum register.</span><span class="sxs-lookup"><span data-stu-id="c7497-105">Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.</span></span>

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c7497-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c7497-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="c7497-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7497-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7497-108">een benaderingen-para meter waarmee wordt bepaald op welk niveau de bewaakte Z-rotaties die zich in het QFT-circuit bevinden, worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c7497-108">approximation parameter which determines at which level the controlled Z-rotations that occur in the QFT circuit are pruned.</span></span>

<span data-ttu-id="c7497-109">Met de benaderings parameter a wordt het Pruning-niveau van de Z-rotaties bepaald, d.w.z. een ∈ {0.. n} en alle Z-rotaties 2π/2.000 waarbij k>a worden verwijderd uit het QFT-circuit.</span><span class="sxs-lookup"><span data-stu-id="c7497-109">The approximation parameter a determines the pruning level of the Z-rotations, i.e., a ∈ {0..n} and all Z-rotations 2π/2ᵏ where k>a are removed from the QFT circuit.</span></span> <span data-ttu-id="c7497-110">Het is bekend dat voor k >= log ₂ (n) en log ₂ (1/ε) + 3 een kan worden gebonden | | QFT-AQFT | |<ε.</span><span class="sxs-lookup"><span data-stu-id="c7497-110">It is known that for k >= log₂(n)+log₂(1/ε)+3 one can bound ||QFT-AQFT||<ε.</span></span>


### <a name="qs--bigendian"></a><span data-ttu-id="c7497-111">qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="c7497-111">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="c7497-112">Quantum register van n qubits waarmee de benadering van de Quantum Fourier-trans formatie wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c7497-112">quantum register of n qubits to which the Approximate Quantum Fourier Transform is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c7497-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7497-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c7497-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c7497-114">Remarks</span></span>

<span data-ttu-id="c7497-115">AQFT vereist Z-rotatie poorten van de vorm 2π/2.000 en Hadamard-Gates.</span><span class="sxs-lookup"><span data-stu-id="c7497-115">AQFT requires Z-rotation gates of the form 2π/2ᵏ and Hadamard gates.</span></span>

<span data-ttu-id="c7497-116">Er wordt van uitgegaan dat de invoer en uitvoer worden gecodeerd in big endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="c7497-116">The input and output are assumed to be encoded in big endian encoding.</span></span>

## <a name="references"></a><span data-ttu-id="c7497-117">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="c7497-117">References</span></span>

- [<span data-ttu-id="c7497-118">*M. Roetteler, th. Beth*, Vereffeningsnr. algebra eng. commun. Comput. 19 (3): 177-193 (2008)</span><span class="sxs-lookup"><span data-stu-id="c7497-118"> *M. Roetteler, Th. Beth*, Appl. Algebra Eng. Commun. Comput. 19(3): 177-193 (2008) </span></span>](http://doi.org/10.1007/s00200-008-0072-2)
- [<span data-ttu-id="c7497-119">*D. Coppersmith* arXiv: Quant-pH/0201067v1</span><span class="sxs-lookup"><span data-stu-id="c7497-119"> *D. Coppersmith* arXiv:quant-ph/0201067v1 </span></span>](https://arxiv.org/abs/quant-ph/0201067)