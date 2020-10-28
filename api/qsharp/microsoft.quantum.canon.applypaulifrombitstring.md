---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Bewerking ApplyPauliFromBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: 09754accb92c1339b781003e5722e3c8f5884e6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705108"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="3f4c2-102">Bewerking ApplyPauliFromBitString</span><span class="sxs-lookup"><span data-stu-id="3f4c2-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="3f4c2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3f4c2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3f4c2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3f4c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3f4c2-105">Past een Pauli-operator op elke qubit in een matrix toe als de overeenkomstige bit van een Boole-matrix overeenkomt met een gegeven invoer.</span><span class="sxs-lookup"><span data-stu-id="3f4c2-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3f4c2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3f4c2-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="3f4c2-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="3f4c2-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="3f4c2-108">De operator Pauli die moet worden toegepast op `qubits[idx]` WHERE `bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="3f4c2-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="3f4c2-109">bitApply: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3f4c2-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3f4c2-110">Pauli Toep assen als bit deze waarde is</span><span class="sxs-lookup"><span data-stu-id="3f4c2-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="3f4c2-111">bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="3f4c2-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="3f4c2-112">Booleaanse registratie voor het opgeven van de bijbehorende Qubit in `qubits` moet worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="3f4c2-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3f4c2-113">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3f4c2-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3f4c2-114">Quantum registratie voor selectief Toep assen van de opgegeven Pauli-operator</span><span class="sxs-lookup"><span data-stu-id="3f4c2-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="3f4c2-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3f4c2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3f4c2-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3f4c2-116">Remarks</span></span>

<span data-ttu-id="3f4c2-117">De Boole-matrix en het Quantum register moeten even lang zijn.</span><span class="sxs-lookup"><span data-stu-id="3f4c2-117">The Boolean array and the quantum register must be of equal length.</span></span>