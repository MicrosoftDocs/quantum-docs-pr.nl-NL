---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Bewerking ApplyPauli
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: ccf8e1b3dbe5d4cd916a581aeab190ab0cff2021
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705109"
---
# <a name="applypauli-operation"></a><span data-ttu-id="45906-102">Bewerking ApplyPauli</span><span class="sxs-lookup"><span data-stu-id="45906-102">ApplyPauli operation</span></span>

<span data-ttu-id="45906-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="45906-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="45906-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="45906-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="45906-105">Op basis van een multi-Qubit Pauli-operator, wordt de bijbehorende bewerking toegepast op een registratie.</span><span class="sxs-lookup"><span data-stu-id="45906-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="45906-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="45906-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="45906-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="45906-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="45906-108">Een multi-Qubit Pauli-operator wordt weer gegeven als een matrix van Pauli Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="45906-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="45906-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="45906-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="45906-110">Registreer om de opgegeven Pauli-bewerking op toe te passen.</span><span class="sxs-lookup"><span data-stu-id="45906-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="45906-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="45906-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
