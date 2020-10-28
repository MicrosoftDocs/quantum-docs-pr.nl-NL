---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Bewerking DrawRandomBool
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706716"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="c2a57-102">Bewerking DrawRandomBool</span><span class="sxs-lookup"><span data-stu-id="c2a57-102">DrawRandomBool operation</span></span>

<span data-ttu-id="c2a57-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="c2a57-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="c2a57-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2a57-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2a57-105">Als gevolg van een kans op succes, retourneert een enkele Bernoulli-proef versie die waar is met de opgegeven kans.</span><span class="sxs-lookup"><span data-stu-id="c2a57-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="c2a57-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c2a57-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="c2a57-107">successProbability: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c2a57-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c2a57-108">De kans dat `true` moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c2a57-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c2a57-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c2a57-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c2a57-110">`true` met waarschijnlijkheid `successProbability` en `false` met waarschijnlijkheid `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="c2a57-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>