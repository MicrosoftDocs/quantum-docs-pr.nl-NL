---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms
title: Door de gebruiker gedefinieerd JWOptimizedHTerms-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JWOptimizedHTerms
qsharp.summary: Format of data passed from C# to Q# to represent terms of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: d75737f23db84f2a21daff7a0ebcb8ae51feb642
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703179"
---
# <a name="jwoptimizedhterms-user-defined-type"></a>Door de gebruiker gedefinieerd JWOptimizedHTerms-type

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


De indeling van gegevens die zijn door gegeven van C# naar Q # om de voor waarden van de Hamiltonian weer te geven.
De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.

```qsharp

newtype JWOptimizedHTerms = (Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[]);
```

