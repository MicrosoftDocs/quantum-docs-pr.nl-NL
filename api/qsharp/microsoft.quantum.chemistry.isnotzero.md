---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: De functie IsNotZero
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839604"
---
# <a name="isnotzero-function"></a><span data-ttu-id="e9fdc-102">De functie IsNotZero</span><span class="sxs-lookup"><span data-stu-id="e9fdc-102">IsNotZero function</span></span>

<span data-ttu-id="e9fdc-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e9fdc-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="e9fdc-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e9fdc-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="e9fdc-105">Hiermee wordt gecontroleerd of een `Double` getal niet ongeveer nul is.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="e9fdc-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e9fdc-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="e9fdc-107">nummer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e9fdc-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e9fdc-108">Nummer dat moet worden gecontroleerd</span><span class="sxs-lookup"><span data-stu-id="e9fdc-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="e9fdc-109">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e9fdc-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e9fdc-110">Retourneert waar als `number` een absolute waarde groter is dan `1e-15` .</span><span class="sxs-lookup"><span data-stu-id="e9fdc-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>