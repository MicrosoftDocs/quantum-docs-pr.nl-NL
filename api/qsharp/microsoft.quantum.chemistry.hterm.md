---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Door de gebruiker gedefinieerd HTerm-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 7a18db539e55e4c1086b3d83725e3d4ba87f0117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703568"
---
# <a name="hterm-user-defined-type"></a>Door de gebruiker gedefinieerd HTerm-type

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket [](https://nuget.org/packages/)


Indeling van gegevens die zijn door gegeven van C# naar Q # om een term van de Hamiltonian weer te geven.
De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.

```qsharp

newtype HTerm = (Int[], Double[]);
```

