---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: De functie IsNotZero
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204059"
---
# <a name="isnotzero-function"></a><span data-ttu-id="b74fb-102">De functie IsNotZero</span><span class="sxs-lookup"><span data-stu-id="b74fb-102">IsNotZero function</span></span>

<span data-ttu-id="b74fb-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b74fb-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="b74fb-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b74fb-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b74fb-105">Hiermee wordt gecontroleerd of een `Double` getal niet ongeveer nul is.</span><span class="sxs-lookup"><span data-stu-id="b74fb-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="b74fb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b74fb-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="b74fb-107">nummer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b74fb-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b74fb-108">Nummer dat moet worden gecontroleerd</span><span class="sxs-lookup"><span data-stu-id="b74fb-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="b74fb-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b74fb-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b74fb-110">Retourneert waar als `number` een absolute waarde groter is dan `1e-15` .</span><span class="sxs-lookup"><span data-stu-id="b74fb-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>