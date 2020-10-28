---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Door de gebruiker gedefinieerd BlockEncoding-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 1b769c58fd23b4ebc9d779cec3c47d8275822e5a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708089"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="d8b4f-102">Door de gebruiker gedefinieerd BlockEncoding-type</span><span class="sxs-lookup"><span data-stu-id="d8b4f-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="d8b4f-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d8b4f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d8b4f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d8b4f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d8b4f-105">Hiermee wordt een unitary aangeduid waarbij een wille keurige operator van belang wordt gecodeerd in het blok linksboven.</span><span class="sxs-lookup"><span data-stu-id="d8b4f-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="d8b4f-106">Dat wil zeggen, een `BlockEncoding` is een unitary $U $ waarbij een wille keurige operator $H $ of interest die op het systeem register reageert `s` , wordt gecodeerd in het blok linksboven dat overeenkomt met de hulp status $ \ket {0} _a $.</span><span class="sxs-lookup"><span data-stu-id="d8b4f-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="d8b4f-107">Dat wil zeggen,</span><span class="sxs-lookup"><span data-stu-id="d8b4f-107">That is,</span></span>

<span data-ttu-id="d8b4f-108">$ $ \begin{align} (\bra {0} _a \otimes I_s) U (\ket {0} _a \otimes I_s) = H \end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="d8b4f-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

