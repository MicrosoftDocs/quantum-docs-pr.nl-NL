---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Bewerking FiveQubitCodeEncoderImpl
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 0a40d9674c011567b2fa9c838f31a0ee115e4268
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826084"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="50e5c-102">Bewerking FiveQubitCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="50e5c-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="50e5c-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="50e5c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="50e5c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="50e5c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="50e5c-105">Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel de 5 Qubit encoder als de decoder.</span><span class="sxs-lookup"><span data-stu-id="50e5c-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="50e5c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="50e5c-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="50e5c-107">gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="50e5c-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="50e5c-108">een matrix met 1 Qubit die de invoer-Qubit is.</span><span class="sxs-lookup"><span data-stu-id="50e5c-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="50e5c-109">kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="50e5c-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="50e5c-110">een matrix met 4 qubits waarvoor redundantie is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="50e5c-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="50e5c-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="50e5c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="50e5c-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="50e5c-112">Remarks</span></span>

<span data-ttu-id="50e5c-113">Het geselecteerde coderings programma is gemaakt op basis van het papier V. Kliuchnikov en D. Maslov, "Optima Lise ring van Clifford-circuits," fysieke. Rev. fysieke. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Afbeelding 4b) en is in totaal 11 poorten vereist.</span><span class="sxs-lookup"><span data-stu-id="50e5c-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>