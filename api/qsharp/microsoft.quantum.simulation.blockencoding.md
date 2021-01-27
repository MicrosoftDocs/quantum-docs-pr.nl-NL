---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Door de gebruiker gedefinieerd BlockEncoding-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 70cd18f04cbd449f4818ba3b40580303137f84db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857637"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="996d1-102">Door de gebruiker gedefinieerd BlockEncoding-type</span><span class="sxs-lookup"><span data-stu-id="996d1-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="996d1-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="996d1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="996d1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="996d1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="996d1-105">Hiermee wordt een unitary aangeduid waarbij een wille keurige operator van belang wordt gecodeerd in het blok linksboven.</span><span class="sxs-lookup"><span data-stu-id="996d1-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="996d1-106">Dat wil zeggen, een `BlockEncoding` is een unitary $U $ waarbij een wille keurige operator $H $ of interest die op het systeem register reageert `s` , wordt gecodeerd in het blok linksboven dat overeenkomt met de hulp status $ \ket {0} _a $.</span><span class="sxs-lookup"><span data-stu-id="996d1-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="996d1-107">Dat wil zeggen,</span><span class="sxs-lookup"><span data-stu-id="996d1-107">That is,</span></span>

<span data-ttu-id="996d1-108">$ $ \begin{align} (\bra {0} _a \otimes I_s) U (\ket {0} _a \otimes I_s) = H \end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="996d1-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

