---
uid: Microsoft.Quantum.Characterization.ApplyHadamardTest
title: Bewerking ApplyHadamardTest
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ApplyHadamardTest
qsharp.summary: ''
ms.openlocfilehash: c36a54bf907d41c9eaa1ece01b1bd446f6b8aaa1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851930"
---
# <a name="applyhadamardtest-operation"></a><span data-ttu-id="17eab-102">Bewerking ApplyHadamardTest</span><span class="sxs-lookup"><span data-stu-id="17eab-102">ApplyHadamardTest operation</span></span>

<span data-ttu-id="17eab-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="17eab-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="17eab-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="17eab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyHadamardTest (phaseShift : Bool, commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), control : Qubit, target : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="17eab-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="17eab-105">Input</span></span>

### <a name="phaseshift--bool"></a><span data-ttu-id="17eab-106">phaseShift: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="17eab-106">phaseShift : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="17eab-107">commonPreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="17eab-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="17eab-108">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="17eab-108">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="17eab-109">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="17eab-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="control--qubit"></a><span data-ttu-id="17eab-110">besturings element: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="17eab-110">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="target--qubit"></a><span data-ttu-id="17eab-111">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="17eab-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="17eab-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="17eab-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

