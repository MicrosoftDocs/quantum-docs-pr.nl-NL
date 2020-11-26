---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: De functie SteaneCodeRecoveryX
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 5fac832ef5b7d7be2d85675a32f45e66312f66c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200367"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="52f05-102">De functie SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="52f05-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="52f05-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="52f05-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="52f05-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="52f05-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="52f05-105">Decoder voor het X-deel van de stabilisatorer groep van de ⟦ ⟧ Steane Quantum code.</span><span class="sxs-lookup"><span data-stu-id="52f05-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="52f05-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="52f05-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="52f05-107">syndrome: [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="52f05-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="52f05-108">Een Syndrome-matrix die is verkregen van het meten van de X-deel van de stabilisator.</span><span class="sxs-lookup"><span data-stu-id="52f05-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="52f05-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="52f05-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="52f05-110">Een matrix met Pauli-bewerkingen die, wanneer toegepast op het gecodeerde Quantum systeem, de fout corrigeert die overeenkomt met `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="52f05-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f05-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="52f05-111">Remarks</span></span>

<span data-ttu-id="52f05-112">De gekozen decoder maakt gebruik van de CSS-code-eigenschap van de ⟦-code van de 7, 1, 3 ⟧ Steane, dat wil zeggen, het corrigeert X fouten en Z-fouten afzonderlijk.</span><span class="sxs-lookup"><span data-stu-id="52f05-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="52f05-113">Een eigenschap van de code is dat de locatie van de X, respectievelijk de Z-correctie die moet worden toegepast, de 3-bits code ring van de X, respectievelijk Z Syndrome is als een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="52f05-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="52f05-114">Referenties</span><span class="sxs-lookup"><span data-stu-id="52f05-114">References</span></span>

- <span data-ttu-id="52f05-115">D.</span><span class="sxs-lookup"><span data-stu-id="52f05-115">D.</span></span> <span data-ttu-id="52f05-116">Gottesman, "stabilisators codes en Quantum fout correctie," Ph.D. thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="52f05-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="52f05-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="52f05-117">See Also</span></span>

- [<span data-ttu-id="52f05-118">Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryX</span><span class="sxs-lookup"><span data-stu-id="52f05-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="52f05-119">Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryFns</span><span class="sxs-lookup"><span data-stu-id="52f05-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)