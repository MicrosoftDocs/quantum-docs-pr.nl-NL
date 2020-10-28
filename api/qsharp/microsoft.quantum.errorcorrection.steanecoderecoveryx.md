---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: De functie SteaneCodeRecoveryX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 0f6b987ca23bd9ff2076080d60f1ca756b36848e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702393"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="5bccd-102">De functie SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="5bccd-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="5bccd-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="5bccd-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="5bccd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5bccd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5bccd-105">Decoder voor het X-deel van de stabilisatorer groep van de ⟦ ⟧ Steane Quantum code.</span><span class="sxs-lookup"><span data-stu-id="5bccd-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="5bccd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5bccd-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="5bccd-107">syndrome: [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="5bccd-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="5bccd-108">Een Syndrome-matrix die is verkregen van het meten van de X-deel van de stabilisator.</span><span class="sxs-lookup"><span data-stu-id="5bccd-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="5bccd-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="5bccd-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="5bccd-110">Een matrix met Pauli-bewerkingen die, wanneer toegepast op het gecodeerde Quantum systeem, de fout corrigeert die overeenkomt met `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="5bccd-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bccd-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5bccd-111">Remarks</span></span>

<span data-ttu-id="5bccd-112">De gekozen decoder maakt gebruik van de CSS-code-eigenschap van de ⟦-code van de 7, 1, 3 ⟧ Steane, dat wil zeggen, het corrigeert X fouten en Z-fouten afzonderlijk.</span><span class="sxs-lookup"><span data-stu-id="5bccd-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="5bccd-113">Een eigenschap van de code is dat de locatie van de X, respectievelijk de Z-correctie die moet worden toegepast, de 3-bits code ring van de X, respectievelijk Z Syndrome is als een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="5bccd-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="5bccd-114">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="5bccd-114">References</span></span>

- <span data-ttu-id="5bccd-115">D.</span><span class="sxs-lookup"><span data-stu-id="5bccd-115">D.</span></span> <span data-ttu-id="5bccd-116">Gottesman, "stabilisators codes en Quantum fout correctie," Ph.D. thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="5bccd-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="5bccd-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5bccd-117">See Also</span></span>

- [<span data-ttu-id="5bccd-118">Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="5bccd-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="5bccd-119">Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryFns</span><span class="sxs-lookup"><span data-stu-id="5bccd-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)