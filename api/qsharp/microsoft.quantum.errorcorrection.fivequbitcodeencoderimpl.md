---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Bewerking FiveQubitCodeEncoderImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 29b0f47ddffeae3ed4dfda4084304427418e02fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702482"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="333cb-102">Bewerking FiveQubitCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="333cb-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="333cb-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="333cb-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="333cb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="333cb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="333cb-105">Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel de 5 Qubit encoder als de decoder.</span><span class="sxs-lookup"><span data-stu-id="333cb-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="333cb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="333cb-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="333cb-107">gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="333cb-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="333cb-108">een matrix met 1 Qubit die de invoer-Qubit is.</span><span class="sxs-lookup"><span data-stu-id="333cb-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="333cb-109">kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="333cb-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="333cb-110">een matrix met 4 qubits waarvoor redundantie is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="333cb-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="333cb-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="333cb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="333cb-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="333cb-112">Remarks</span></span>

<span data-ttu-id="333cb-113">Het geselecteerde coderings programma is gemaakt op basis van het papier V. Kliuchnikov en D. Maslov, "Optima Lise ring van Clifford-circuits," fysieke. Rev. fysieke. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Afbeelding 4b) en is in totaal 11 poorten vereist.</span><span class="sxs-lookup"><span data-stu-id="333cb-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>