---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData
title: Door de gebruiker gedefinieerd JordanWignerEncodingData-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerEncodingData
qsharp.summary: Format of data passed from C# to Q# to represent all information for Hamiltonian simulation. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 62988eefa57d8a9e4ed9dcfbdbc6c3b630c6faa2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703215"
---
# <a name="jordanwignerencodingdata-user-defined-type"></a>Door de gebruiker gedefinieerd JordanWignerEncodingData-type

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Indeling van gegevens die zijn door gegeven van C# naar Q # om alle informatie voor Hamiltonian simulatie weer te geven.
De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.

```qsharp

newtype JordanWignerEncodingData = (Int, Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms, (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), Double);
```

