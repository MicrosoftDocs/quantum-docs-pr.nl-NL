---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerOptimizedBlockEncodingStatePrep
title: _JordanWignerOptimizedBlockEncodingStatePrep bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerOptimizedBlockEncodingStatePrep
qsharp.summary: ''
ms.openlocfilehash: 2853d46a576ed47e9a6b9564983226e5a2744622
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215636"
---
# <a name="_jordanwigneroptimizedblockencodingstateprep-operation"></a><span data-ttu-id="d4262-102">_JordanWignerOptimizedBlockEncodingStatePrep bewerking</span><span class="sxs-lookup"><span data-stu-id="d4262-102">_JordanWignerOptimizedBlockEncodingStatePrep operation</span></span>

<span data-ttu-id="d4262-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="d4262-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="d4262-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d4262-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>




```qsharp
operation _JordanWignerOptimizedBlockEncodingStatePrep (targetError : Double, optimizedBEGeneratorSystem : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem, qROMIdxRegister : Microsoft.Quantum.Arithmetic.LittleEndian, qROMGarbage : Qubit[], signQubit : Qubit, selectZControlRegisters : Qubit[], OptimizedBEControlRegisters : Qubit[], pauliBases : Qubit[], pauliBasesIdx : Microsoft.Quantum.Arithmetic.LittleEndian, indexRegisters : Microsoft.Quantum.Arithmetic.LittleEndian[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d4262-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="d4262-105">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="d4262-106">targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d4262-106">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="optimizedbegeneratorsystem--optimizedbegeneratorsystem"></a><span data-ttu-id="d4262-107">optimizedBEGeneratorSystem: [optimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="d4262-107">optimizedBEGeneratorSystem : [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span></span>




### <a name="qromidxregister--littleendian"></a><span data-ttu-id="d4262-108">qROMIdxRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d4262-108">qROMIdxRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="qromgarbage--qubit"></a><span data-ttu-id="d4262-109">qROMGarbage: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4262-109">qROMGarbage : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="signqubit--qubit"></a><span data-ttu-id="d4262-110">signQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d4262-110">signQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="selectzcontrolregisters--qubit"></a><span data-ttu-id="d4262-111">selectZControlRegisters: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4262-111">selectZControlRegisters : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="optimizedbecontrolregisters--qubit"></a><span data-ttu-id="d4262-112">OptimizedBEControlRegisters: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4262-112">OptimizedBEControlRegisters : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="paulibases--qubit"></a><span data-ttu-id="d4262-113">pauliBases: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4262-113">pauliBases : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="paulibasesidx--littleendian"></a><span data-ttu-id="d4262-114">pauliBasesIdx: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d4262-114">pauliBasesIdx : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="indexregisters--littleendian"></a><span data-ttu-id="d4262-115">indexRegisters: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]</span><span class="sxs-lookup"><span data-stu-id="d4262-115">indexRegisters : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="d4262-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4262-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

