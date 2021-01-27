---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Door de gebruiker gedefinieerd JordanWignerInputState-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 18adf28b4e99c825f14e9271791ded069e687901
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837699"
---
# <a name="jordanwignerinputstate-user-defined-type"></a><span data-ttu-id="0606c-102">Door de gebruiker gedefinieerd JordanWignerInputState-type</span><span class="sxs-lookup"><span data-stu-id="0606c-102">JordanWignerInputState user defined type</span></span>

<span data-ttu-id="0606c-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="0606c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="0606c-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="0606c-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="0606c-105">Indeling van gegevens die zijn door gegeven van C# naar Q # voor de voor bereiding van de begin toestand, de betekenis van de gegevens die worden weer gegeven, is afhankelijk van het algoritme dat deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="0606c-105">Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

