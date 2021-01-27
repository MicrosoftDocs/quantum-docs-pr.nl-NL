---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Bewerking DrawRandomBool
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853692"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="9e6a2-102">Bewerking DrawRandomBool</span><span class="sxs-lookup"><span data-stu-id="9e6a2-102">DrawRandomBool operation</span></span>

<span data-ttu-id="9e6a2-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="9e6a2-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9e6a2-105">Als gevolg van een kans op succes, retourneert een enkele Bernoulli-proef versie die waar is met de opgegeven kans.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="9e6a2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9e6a2-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="9e6a2-107">successProbability: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9e6a2-108">De kans dat `true` moet worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9e6a2-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9e6a2-110">`true` met waarschijnlijkheid `successProbability` en `false` met waarschijnlijkheid `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="9e6a2-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>

## <a name="example"></a><span data-ttu-id="9e6a2-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9e6a2-111">Example</span></span>

<span data-ttu-id="9e6a2-112">De volgende Q # fragment voorbeelden worden gespiegeld van een verte kende munten:</span><span class="sxs-lookup"><span data-stu-id="9e6a2-112">The following Q# snippet samples flips from a biased coin:</span></span>

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```