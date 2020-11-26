---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData
title: Door de gebruiker gedefinieerd JordanWignerEncodingData-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerEncodingData
qsharp.summary: Format of data passed from C# to Q# to represent all information for Hamiltonian simulation. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 2acb33c8dab229264273ff23606c47322df740a4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214786"
---
# <a name="jordanwignerencodingdata-user-defined-type"></a><span data-ttu-id="87e61-102">Door de gebruiker gedefinieerd JordanWignerEncodingData-type</span><span class="sxs-lookup"><span data-stu-id="87e61-102">JordanWignerEncodingData user defined type</span></span>

<span data-ttu-id="87e61-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="87e61-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="87e61-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="87e61-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="87e61-105">Indeling van gegevens die zijn door gegeven van C# naar Q # om alle informatie voor Hamiltonian simulatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="87e61-105">Format of data passed from C# to Q# to represent all information for Hamiltonian simulation.</span></span>
<span data-ttu-id="87e61-106">De betekenis van de gegevens die worden weer gegeven, is afhankelijk van de algoritme die deze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="87e61-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerEncodingData = (Int, Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms, (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), Double);
```

