---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Door de gebruiker gedefinieerd HTerm-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 504d55dc57ce92c12e6f016e9afcedfd59664aa1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204127"
---
# <a name="hterm-user-defined-type"></a><span data-ttu-id="40291-102">Door de gebruiker gedefinieerd HTerm-type</span><span class="sxs-lookup"><span data-stu-id="40291-102">HTerm user defined type</span></span>

<span data-ttu-id="40291-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="40291-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="40291-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="40291-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="40291-105">Indeling van gegevens die zijn door gegeven van C# naar Q # om een term van de Hamiltonian weer te geven.</span><span class="sxs-lookup"><span data-stu-id="40291-105">Format of data passed from C# to Q# to represent a term of the Hamiltonian.</span></span>
<span data-ttu-id="40291-106">De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="40291-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype HTerm = (Int[], Double[]);
```

