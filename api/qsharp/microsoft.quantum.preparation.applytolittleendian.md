---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Bewerking ApplyToLittleEndian
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: a8c765d4b8f5d2f09cf68b7140e31c9114643733
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856980"
---
# <a name="applytolittleendian-operation"></a><span data-ttu-id="44411-102">Bewerking ApplyToLittleEndian</span><span class="sxs-lookup"><span data-stu-id="44411-102">ApplyToLittleEndian operation</span></span>

<span data-ttu-id="44411-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="44411-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="44411-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="44411-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="44411-105">Hiermee wordt een bewerking toegepast op de onderliggende qubits die een little-endian-registratie maakt.</span><span class="sxs-lookup"><span data-stu-id="44411-105">Applies an operation to the underlying qubits making up a little-endian register.</span></span> <span data-ttu-id="44411-106">Deze bewerking is gemarkeerd als intern, omdat een registratie van een little-endian is bedoeld als ' dekkend ', zodat dit alleen een implementatie detail is.</span><span class="sxs-lookup"><span data-stu-id="44411-106">This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.</span></span>

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="44411-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="44411-107">Input</span></span>

### <a name="bareop--qubit--unit--is-adj--ctl"></a><span data-ttu-id="44411-108">bareOp: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="44411-108">bareOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="register--littleendian"></a><span data-ttu-id="44411-109">registreren: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="44411-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="44411-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="44411-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

