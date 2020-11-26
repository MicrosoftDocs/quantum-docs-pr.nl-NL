---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Door de gebruiker gedefinieerd BlockEncoding-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 75fdbf13cf07d906982d4a611d1d25b3e29db2cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225428"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="5e0cd-102">Door de gebruiker gedefinieerd BlockEncoding-type</span><span class="sxs-lookup"><span data-stu-id="5e0cd-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="5e0cd-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5e0cd-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5e0cd-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5e0cd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5e0cd-105">Hiermee wordt een unitary aangeduid waarbij een wille keurige operator van belang wordt gecodeerd in het blok linksboven.</span><span class="sxs-lookup"><span data-stu-id="5e0cd-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="5e0cd-106">Dat wil zeggen, een `BlockEncoding` is een unitary $U $ waarbij een wille keurige operator $H $ of interest die op het systeem register reageert `s` , wordt gecodeerd in het blok linksboven dat overeenkomt met de hulp status $ \ket {0} _a $.</span><span class="sxs-lookup"><span data-stu-id="5e0cd-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="5e0cd-107">Dat wil zeggen,</span><span class="sxs-lookup"><span data-stu-id="5e0cd-107">That is,</span></span>

<span data-ttu-id="5e0cd-108">$ $ \begin{align} (\bra {0} _a \otimes I_s) U (\ket {0} _a \otimes I_s) = H \end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="5e0cd-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

