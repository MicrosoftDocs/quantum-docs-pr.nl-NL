---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Bewerking SteaneCodeEncoderImpl
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 81abe75e2a315fe9a994147242f3c8c9bde586ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824725"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="7c9c4-102">Bewerking SteaneCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="7c9c4-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="7c9c4-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="7c9c4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="7c9c4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c9c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c9c4-105">Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel het coderings programma voor Steane code als de decoder.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="7c9c4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7c9c4-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="7c9c4-107">gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7c9c4-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7c9c4-108">een matrix met 1 Qubit die de invoer-Qubit is.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="7c9c4-109">kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7c9c4-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7c9c4-110">een matrix met 6 qubits waarvoor redundantie is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7c9c4-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c9c4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

