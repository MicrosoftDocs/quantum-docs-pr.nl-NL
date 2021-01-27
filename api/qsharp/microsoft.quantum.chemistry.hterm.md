---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Door de gebruiker gedefinieerd HTerm-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 744668a4fe96ee00fe2f7991f4e1f05eea19d417
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851778"
---
# <a name="hterm-user-defined-type"></a><span data-ttu-id="3b2fb-102">Door de gebruiker gedefinieerd HTerm-type</span><span class="sxs-lookup"><span data-stu-id="3b2fb-102">HTerm user defined type</span></span>

<span data-ttu-id="3b2fb-103">Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3b2fb-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="3b2fb-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3b2fb-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="3b2fb-105">Indeling van gegevens die zijn door gegeven van C# naar Q # om een term van de Hamiltonian weer te geven.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-105">Format of data passed from C# to Q# to represent a term of the Hamiltonian.</span></span>
<span data-ttu-id="3b2fb-106">De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="3b2fb-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype HTerm = (Int[], Double[]);
```

