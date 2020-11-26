---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: Bewerking AssertOperationsEqualInPlaceCompBasis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 826369bdf3544fb257c2bb202466426c1ca1e113
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202342"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="c78c9-102">Bewerking AssertOperationsEqualInPlaceCompBasis</span><span class="sxs-lookup"><span data-stu-id="c78c9-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="c78c9-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c78c9-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c78c9-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c78c9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c78c9-105">Hiermee wordt gecontroleerd of de bewerking `givenU` gelijk is aan de bewerking `expectedU` op de opgegeven invoer grootte door de actie van de bewerkingen alleen op de vectoren te controleren op basis van de berekening.</span><span class="sxs-lookup"><span data-stu-id="c78c9-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="c78c9-106">Dit is een vereiste, maar niet voldoende, voor waarde voor de gelijkheid van twee unitaries.</span><span class="sxs-lookup"><span data-stu-id="c78c9-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="c78c9-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c78c9-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="c78c9-108">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c78c9-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c78c9-109">Het aantal qubits-$n $ waarop de bewerkingen `givenU` zijn `expectedU` toegepast en waarop wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c78c9-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="c78c9-110">givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c78c9-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c78c9-111">Bewerking op $n $ qubits moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="c78c9-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="c78c9-112">expectedU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="c78c9-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c78c9-113">Verwijzings bewerking op $n $ qubits die moet `givenU` worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c78c9-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c78c9-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c78c9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

