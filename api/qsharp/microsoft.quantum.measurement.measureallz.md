---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Bewerking MeasureAllZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227077"
---
# <a name="measureallz-operation"></a><span data-ttu-id="f6333-102">Bewerking MeasureAllZ</span><span class="sxs-lookup"><span data-stu-id="f6333-102">MeasureAllZ operation</span></span>

<span data-ttu-id="f6333-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="f6333-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="f6333-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6333-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6333-105">Gezamenlijk meet het REGI ster van qubits in de Pauli Z-basis.</span><span class="sxs-lookup"><span data-stu-id="f6333-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="f6333-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f6333-106">Description</span></span>

<span data-ttu-id="f6333-107">Meting van een REGI ster van qubits in de $Z \otimes Z \otimes \cdots \otimes Z $ soort_jaar, waarmee de pariteit van het volledige REGI ster wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="f6333-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="f6333-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f6333-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="f6333-109">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f6333-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f6333-110">Het REGI ster dat moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="f6333-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="f6333-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f6333-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="f6333-112">Het resultaat van de meting $Z \otimes Z \otimes \cdots \otimes Z $.</span><span class="sxs-lookup"><span data-stu-id="f6333-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>