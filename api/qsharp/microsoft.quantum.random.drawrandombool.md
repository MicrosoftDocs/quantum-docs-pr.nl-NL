---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Bewerking DrawRandomBool
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192958"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="abd12-102">Bewerking DrawRandomBool</span><span class="sxs-lookup"><span data-stu-id="abd12-102">DrawRandomBool operation</span></span>

<span data-ttu-id="abd12-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="abd12-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="abd12-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="abd12-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="abd12-105">Als gevolg van een kans op succes, retourneert een enkele Bernoulli-proef versie die waar is met de opgegeven kans.</span><span class="sxs-lookup"><span data-stu-id="abd12-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="abd12-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="abd12-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="abd12-107">successProbability: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="abd12-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="abd12-108">De kans dat `true` moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="abd12-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="abd12-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="abd12-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="abd12-110">`true` met waarschijnlijkheid `successProbability` en `false` met waarschijnlijkheid `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="abd12-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>