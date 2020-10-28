---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Bewerking DecodeFromSteaneCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e6831a8630c0a80c2abe7c4a720263f0de03edc4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702518"
---
# <a name="decodefromsteanecode-operation"></a><span data-ttu-id="67168-102">Bewerking DecodeFromSteaneCode</span><span class="sxs-lookup"><span data-stu-id="67168-102">DecodeFromSteaneCode operation</span></span>

<span data-ttu-id="67168-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="67168-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="67168-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67168-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67168-105">Een inverse coderings bewerking waarbij een niet-versleutelde Quantum-REGI ster wordt toegewezen aan een gecodeerd Quantum REGI ster onder de Quantum code ⟦, 1, 3 ⟧ Steane.</span><span class="sxs-lookup"><span data-stu-id="67168-105">An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="67168-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="67168-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="67168-107">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="67168-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="67168-108">Een matrix met qubits die de code ring logische status van 5 Qubit vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="67168-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="67168-109">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="67168-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="67168-110">Een Qubit-matrix van lengte 1 die de niet-versleutelde status in de eerste para meter weergeeft, samen met de hulp qubits in de tweede para meter.</span><span class="sxs-lookup"><span data-stu-id="67168-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="67168-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="67168-111">Remarks</span></span>

<span data-ttu-id="67168-112">De gekozen decoder maakt gebruik van de CSS-code-eigenschap van de ⟦-code van de 7, 1, 3 ⟧ Steane, dat wil zeggen, het corrigeert X fouten en Z-fouten afzonderlijk.</span><span class="sxs-lookup"><span data-stu-id="67168-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="67168-113">Een eigenschap van de code is dat de locatie van de X, respectievelijk de Z-correctie die moet worden toegepast, de 3-bits code ring van de X, respectievelijk Z Syndrome is als een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="67168-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="67168-114">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="67168-114">References</span></span>

- <span data-ttu-id="67168-115">D.</span><span class="sxs-lookup"><span data-stu-id="67168-115">D.</span></span> <span data-ttu-id="67168-116">Gottesman, "stabilisators codes en Quantum fout correctie," Ph.D. thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="67168-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="67168-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="67168-117">See Also</span></span>

- [<span data-ttu-id="67168-118">Micro soft. Quantum. ErrorCorrection. SteaneCodeEncoder</span><span class="sxs-lookup"><span data-stu-id="67168-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [<span data-ttu-id="67168-119">Micro soft. Quantum. ErrorCorrection. SteaneCodeDecoder</span><span class="sxs-lookup"><span data-stu-id="67168-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [<span data-ttu-id="67168-120">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="67168-120">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)