---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: Bewerking ApplyToSubregister
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: be820c87ee19230713d6c3e5681bbe3678040e95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850475"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="fc51e-102">Bewerking ApplyToSubregister</span><span class="sxs-lookup"><span data-stu-id="fc51e-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="fc51e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fc51e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fc51e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc51e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc51e-105">Hiermee wordt een bewerking toegepast op een subregister van een REGI ster, waarbij qubits is opgegeven door een matrix met hun indexen.</span><span class="sxs-lookup"><span data-stu-id="fc51e-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fc51e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fc51e-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="fc51e-107">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fc51e-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="fc51e-108">Bewerking die moet worden toegepast op de subregister.</span><span class="sxs-lookup"><span data-stu-id="fc51e-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="fc51e-109">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fc51e-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fc51e-110">De matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="fc51e-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="fc51e-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fc51e-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fc51e-112">Meld u aan waarop de bewerking reageert.</span><span class="sxs-lookup"><span data-stu-id="fc51e-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fc51e-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fc51e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="fc51e-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fc51e-114">Example</span></span>

<span data-ttu-id="fc51e-115">Maak drie Qubit-status $ \frac {1} {\sqrt {2} } \ket {0} \_ 2 (\ket {0} \_ 1 \ Ket {0} _3 + \ket {1} \_ 1 \ Ket {1} _3) $:</span><span class="sxs-lookup"><span data-stu-id="fc51e-115">Create three qubit state $\frac{1}{\sqrt{2}}\ket{0}\_2(\ket{0}\_1\ket{0}_3+\ket{1}\_1\ket{1}_3)$:</span></span>

```qsharp
    using (register = Qubit[3]) {
        ApplyToSubregister(Exp([PauliX,PauliY],PI() / 4.0,_), [1,3], register);
    }
```

## <a name="see-also"></a><span data-ttu-id="fc51e-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fc51e-116">See Also</span></span>

- [<span data-ttu-id="fc51e-117">Micro soft. Quantum. Canon. ApplyToSubregisterA</span><span class="sxs-lookup"><span data-stu-id="fc51e-117">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="fc51e-118">Micro soft. Quantum. Canon. ApplyToSubregisterC</span><span class="sxs-lookup"><span data-stu-id="fc51e-118">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="fc51e-119">Micro soft. Quantum. Canon. ApplyToSubregisterCA</span><span class="sxs-lookup"><span data-stu-id="fc51e-119">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)