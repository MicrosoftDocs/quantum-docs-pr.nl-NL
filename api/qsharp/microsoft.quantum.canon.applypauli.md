---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Bewerking ApplyPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: b3557c6d8b5a90019f6d4cfa7b405475a3ab39fb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844738"
---
# <a name="applypauli-operation"></a><span data-ttu-id="877bd-102">Bewerking ApplyPauli</span><span class="sxs-lookup"><span data-stu-id="877bd-102">ApplyPauli operation</span></span>

<span data-ttu-id="877bd-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="877bd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="877bd-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="877bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="877bd-105">Op basis van een multi-Qubit Pauli-operator, wordt de bijbehorende bewerking toegepast op een registratie.</span><span class="sxs-lookup"><span data-stu-id="877bd-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="877bd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="877bd-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="877bd-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="877bd-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="877bd-108">Een multi-Qubit Pauli-operator wordt weer gegeven als een matrix van Pauli Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="877bd-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="877bd-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="877bd-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="877bd-110">Registreer om de opgegeven Pauli-bewerking op toe te passen.</span><span class="sxs-lookup"><span data-stu-id="877bd-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="877bd-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="877bd-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="877bd-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="877bd-112">Example</span></span>

<span data-ttu-id="877bd-113">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="877bd-113">The following are equivalent:</span></span>

```qsharp
ApplyPauli([PauliY, PauliZ, PauliX], target);
```

<span data-ttu-id="877bd-114">en</span><span class="sxs-lookup"><span data-stu-id="877bd-114">and</span></span>

```qsharp
Y(target[0]);
Z(target[1]);
X(target[2]);
```