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
# <a name="jordanwignerinputstate-user-defined-type"></a>Door de gebruiker gedefinieerd JordanWignerInputState-type

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Indeling van gegevens die zijn door gegeven van C# naar Q # voor de voor bereiding van de begin toestand, de betekenis van de gegevens die worden weer gegeven, is afhankelijk van het algoritme dat deze ontvangt.

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

