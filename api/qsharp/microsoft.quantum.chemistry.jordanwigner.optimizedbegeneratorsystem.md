---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
title: Door de gebruiker gedefinieerd OptimizedBEGeneratorSystem-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEGeneratorSystem
qsharp.summary: Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.
ms.openlocfilehash: 06d13a8a64a3c572821ec97f8776d6f1dbe4a4ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703167"
---
# <a name="optimizedbegeneratorsystem-user-defined-type"></a><span data-ttu-id="6ca59-102">Door de gebruiker gedefinieerd OptimizedBEGeneratorSystem-type</span><span class="sxs-lookup"><span data-stu-id="6ca59-102">OptimizedBEGeneratorSystem user defined type</span></span>

<span data-ttu-id="6ca59-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="6ca59-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="6ca59-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6ca59-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6ca59-105">Functie die `OptimizedBETermIndex` gegevens retourneert voor `n` een term met een geheel getal `n` , samen met het aantal voor waarden in de eerste `Int` en de som van absolute waarden van alle termen coëfficiënten in de `Double` .</span><span class="sxs-lookup"><span data-stu-id="6ca59-105">Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.</span></span>

```qsharp

newtype OptimizedBEGeneratorSystem = (Int, Double, (Int -> Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex));
```
