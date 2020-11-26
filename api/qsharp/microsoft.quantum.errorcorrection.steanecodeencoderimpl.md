---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Bewerking SteaneCodeEncoderImpl
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 3a9a1b11ed9255f18135e3717de7e9e1ec891298
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200422"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="a123f-102">Bewerking SteaneCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="a123f-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="a123f-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a123f-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a123f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a123f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a123f-105">Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel het coderings programma voor Steane code als de decoder.</span><span class="sxs-lookup"><span data-stu-id="a123f-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="a123f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a123f-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="a123f-107">gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a123f-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a123f-108">een matrix met 1 Qubit die de invoer-Qubit is.</span><span class="sxs-lookup"><span data-stu-id="a123f-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="a123f-109">kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a123f-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a123f-110">een matrix met 6 qubits waarvoor redundantie is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="a123f-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a123f-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a123f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

