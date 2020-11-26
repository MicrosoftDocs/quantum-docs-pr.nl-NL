---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Door de gebruiker gedefinieerd JordanWignerInputState-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 81993a7449098c03639cf090fb36ed39c6ba17c0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214684"
---
# <a name="jordanwignerinputstate-user-defined-type"></a><span data-ttu-id="8bf03-102">Door de gebruiker gedefinieerd JordanWignerInputState-type</span><span class="sxs-lookup"><span data-stu-id="8bf03-102">JordanWignerInputState user defined type</span></span>

<span data-ttu-id="8bf03-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="8bf03-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="8bf03-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8bf03-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="8bf03-105">Indeling van gegevens die zijn door gegeven van C# naar Q # voor de voor bereiding van de begin toestand, de betekenis van de gegevens die worden weer gegeven, is afhankelijk van het algoritme dat deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="8bf03-105">Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

