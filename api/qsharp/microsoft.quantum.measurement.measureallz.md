---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Bewerking MeasureAllZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854673"
---
# <a name="measureallz-operation"></a><span data-ttu-id="fde93-102">Bewerking MeasureAllZ</span><span class="sxs-lookup"><span data-stu-id="fde93-102">MeasureAllZ operation</span></span>

<span data-ttu-id="fde93-103">Naam ruimte: [micro soft. Quantum. meet](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="fde93-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="fde93-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fde93-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fde93-105">Gezamenlijk meet het REGI ster van qubits in de Pauli Z-basis.</span><span class="sxs-lookup"><span data-stu-id="fde93-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="fde93-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fde93-106">Description</span></span>

<span data-ttu-id="fde93-107">Meting van een REGI ster van qubits in de $Z \otimes Z \otimes \cdots \otimes Z $ soort_jaar, waarmee de pariteit van het volledige REGI ster wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="fde93-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="fde93-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="fde93-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="fde93-109">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fde93-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fde93-110">Het REGI ster dat moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="fde93-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="fde93-111">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="fde93-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="fde93-112">Het resultaat van de meting $Z \otimes Z \otimes \cdots \otimes Z $.</span><span class="sxs-lookup"><span data-stu-id="fde93-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>