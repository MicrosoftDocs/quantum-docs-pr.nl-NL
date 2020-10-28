---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Bewerking SteaneCodeEncoderImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: b843422a6007d01de9b57ec659c229b8ab0ad2e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702417"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="4782d-102">Bewerking SteaneCodeEncoderImpl</span><span class="sxs-lookup"><span data-stu-id="4782d-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="4782d-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="4782d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="4782d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4782d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4782d-105">Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel het coderings programma voor Steane code als de decoder.</span><span class="sxs-lookup"><span data-stu-id="4782d-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4782d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4782d-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="4782d-107">gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4782d-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4782d-108">een matrix met 1 Qubit die de invoer-Qubit is.</span><span class="sxs-lookup"><span data-stu-id="4782d-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="4782d-109">kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4782d-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4782d-110">een matrix met 6 qubits waarvoor redundantie is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4782d-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4782d-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4782d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

