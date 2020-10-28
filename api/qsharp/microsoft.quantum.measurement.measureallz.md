---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Bewerking MeasureAllZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701942"
---
# <a name="measureallz-operation"></a><span data-ttu-id="189b7-102">Bewerking MeasureAllZ</span><span class="sxs-lookup"><span data-stu-id="189b7-102">MeasureAllZ operation</span></span>

<span data-ttu-id="189b7-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="189b7-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="189b7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="189b7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="189b7-105">Gezamenlijk meet het REGI ster van qubits in de Pauli Z-basis.</span><span class="sxs-lookup"><span data-stu-id="189b7-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="189b7-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="189b7-106">Description</span></span>

<span data-ttu-id="189b7-107">Meting van een REGI ster van qubits in de $Z \otimes Z \otimes \cdots \otimes Z $ soort_jaar, waarmee de pariteit van het volledige REGI ster wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="189b7-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="189b7-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="189b7-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="189b7-109">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="189b7-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="189b7-110">Het REGI ster dat moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="189b7-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="189b7-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="189b7-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="189b7-112">Het resultaat van de meting $Z \otimes Z \otimes \cdots \otimes Z $.</span><span class="sxs-lookup"><span data-stu-id="189b7-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>