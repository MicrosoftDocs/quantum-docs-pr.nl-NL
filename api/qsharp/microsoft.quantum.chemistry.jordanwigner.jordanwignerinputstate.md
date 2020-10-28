---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Door de gebruiker gedefinieerd JordanWignerInputState-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 171a2999ab8c73925d4624c565bfd41a4e73c99d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703185"
---
# <a name="jordanwignerinputstate-user-defined-type"></a><span data-ttu-id="5a08c-102">Door de gebruiker gedefinieerd JordanWignerInputState-type</span><span class="sxs-lookup"><span data-stu-id="5a08c-102">JordanWignerInputState user defined type</span></span>

<span data-ttu-id="5a08c-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="5a08c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="5a08c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a08c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5a08c-105">Indeling van gegevens die zijn door gegeven van C# naar Q # voor de voor bereiding van de begin toestand, de betekenis van de gegevens die worden weer gegeven, is afhankelijk van het algoritme dat deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="5a08c-105">Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

