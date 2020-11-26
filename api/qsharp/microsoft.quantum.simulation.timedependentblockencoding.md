---
uid: Microsoft.Quantum.Simulation.TimeDependentBlockEncoding
title: Door de gebruiker gedefinieerd TimeDependentBlockEncoding-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentBlockEncoding
qsharp.summary: >-
  Represents a `BlockEncoding` that is controlled by a clock register.

  That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k. \end{align} $$.
ms.openlocfilehash: 8fade22dca7af16a567a88f4413c8e9dcc1604b2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203498"
---
# <a name="timedependentblockencoding-user-defined-type"></a><span data-ttu-id="ada31-102">Door de gebruiker gedefinieerd TimeDependentBlockEncoding-type</span><span class="sxs-lookup"><span data-stu-id="ada31-102">TimeDependentBlockEncoding user defined type</span></span>

<span data-ttu-id="ada31-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ada31-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ada31-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ada31-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ada31-105">Vertegenwoordigt een `BlockEncoding` die wordt beheerd door een klok registratie.</span><span class="sxs-lookup"><span data-stu-id="ada31-105">Represents a `BlockEncoding` that is controlled by a clock register.</span></span>

<span data-ttu-id="ada31-106">Dat wil zeggen, a `TimeDependentBlockEncoding` is een unitary-$U $, beheerd door een status $ \ket{k} _d $ in een klok registratie, `d` zodat een wille keurige operator $H _k $ van belang dat er op het systeem register `s` wordt gedecodeerd in het blok linksboven dat overeenkomt met de hulp status $ \ket {0} _a $.</span><span class="sxs-lookup"><span data-stu-id="ada31-106">That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="ada31-107">Dat wil zeggen,</span><span class="sxs-lookup"><span data-stu-id="ada31-107">That is,</span></span>

<span data-ttu-id="ada31-108">$ $ \begin{align} (\bra {0} \_ a\otimes i_ {DS}) U (\ket {0} \_ a\otimes i_ {DS}) = \ sum_ {k} \ket{k}\bra{k} \_ d\otimes H_k.</span><span class="sxs-lookup"><span data-stu-id="ada31-108">$$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k.</span></span>
<span data-ttu-id="ada31-109">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="ada31-109">\end{align} $$.</span></span>

```qsharp

newtype TimeDependentBlockEncoding = (((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

