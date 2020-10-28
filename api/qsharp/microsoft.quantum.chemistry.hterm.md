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
# <a name="hterm-user-defined-type"></a><span data-ttu-id="89449-102">Door de gebruiker gedefinieerd HTerm-type</span><span class="sxs-lookup"><span data-stu-id="89449-102">HTerm user defined type</span></span>

<span data-ttu-id="89449-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="89449-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="89449-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89449-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89449-105">Indeling van gegevens die zijn door gegeven van C# naar Q # om een term van de Hamiltonian weer te geven.</span><span class="sxs-lookup"><span data-stu-id="89449-105">Format of data passed from C# to Q# to represent a term of the Hamiltonian.</span></span>
<span data-ttu-id="89449-106">De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="89449-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype HTerm = (Int[], Double[]);
```

