---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 273692efa629cb8cc20069ef500c4e0902fbc3ff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201339"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a><span data-ttu-id="f7621-102">_ExtractLogicalQubitFromSteaneCode bewerking</span><span class="sxs-lookup"><span data-stu-id="f7621-102">_ExtractLogicalQubitFromSteaneCode operation</span></span>

<span data-ttu-id="f7621-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f7621-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f7621-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7621-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f7621-105">Syndrome-meting en de inverse van het insluiten.</span><span class="sxs-lookup"><span data-stu-id="f7621-105">Syndrome measurement and the inverse of embedding.</span></span>

<span data-ttu-id="f7621-106">$X $-en $Z $-stabilisatoren worden niet gelijk behandeld, wat het gevolg is van de specifieke keuze van het coderings circuit.</span><span class="sxs-lookup"><span data-stu-id="f7621-106">$X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit.</span></span>
<span data-ttu-id="f7621-107">Deze asymmetrie leidt naar een andere Syndrome-extractie routine.</span><span class="sxs-lookup"><span data-stu-id="f7621-107">This asymmetry leads to a different syndrome extraction routine.</span></span>
<span data-ttu-id="f7621-108">Eén kan de Syndrome meten door de multi-Qubit Pauli-operator rechtstreeks op de code status te meten, maar voor het doel van de distillatie wordt de logische Qubit geretourneerd in één Qubit, in de periode dat de Syndrome metingen zonder verdere ancillas kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f7621-108">One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.</span></span>

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a><span data-ttu-id="f7621-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="f7621-109">Input</span></span>

### <a name="code--logicalregister"></a><span data-ttu-id="f7621-110">code: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="f7621-110">code : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>





## <a name="output--qubitintint"></a><span data-ttu-id="f7621-111">Uitvoer: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="f7621-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="f7621-112">De logische Qubit en een paar gehele getallen voor $X $-Syndrome en $Z $-Syndrome.</span><span class="sxs-lookup"><span data-stu-id="f7621-112">The logical qubit and a pair of integers for $X$-syndrome and $Z$-syndrome.</span></span>
<span data-ttu-id="f7621-113">Ze vertegenwoordigen de index van de code Qubit waarop een enkele $X $-of $Z $-error de gemeten Syndrome heeft veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="f7621-113">They represent the index of the code qubit on which a single $X$- or $Z$-error would have caused the measured syndrome.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7621-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f7621-114">Remarks</span></span>

<span data-ttu-id="f7621-115">Houd er rekening mee dat deze bewerking niet is gemarkeerd als `internal` , omdat eenheids tests rechtstreeks afhankelijk zijn van deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="f7621-115">Note that this operation is not marked as `internal`, as unit tests directly depend on this operation.</span></span> <span data-ttu-id="f7621-116">Als toekomstige verbetering moeten eenheids testen worden herstructureeerd om alleen rechtstreeks op open bare callables te zijn.</span><span class="sxs-lookup"><span data-stu-id="f7621-116">As a future improvement, unit tests should be refactored to depend only on public callables directly.</span></span>

> [!WARNING]
> <span data-ttu-id="f7621-117">Deze routine is afgestemd op een bepaald coderings circuit voor de 7 Qubit-code van Steane. Als het coderings circuit is gewijzigd, moet het Syndrome-resultaat mogelijk anders worden geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="f7621-117">This routine is tailored to a particular encoding circuit for Steane's 7 qubit code; if the encoding circuit is modified then the syndrome outcome might have to be interpreted differently.</span></span>