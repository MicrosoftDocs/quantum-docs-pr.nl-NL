---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Bewerking ApplyToLittleEndian
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: d94a9969a3f827d594946ab8ca6cd4672da7ef7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708695"
---
# <a name="applytolittleendian-operation"></a><span data-ttu-id="b9675-102">Bewerking ApplyToLittleEndian</span><span class="sxs-lookup"><span data-stu-id="b9675-102">ApplyToLittleEndian operation</span></span>

<span data-ttu-id="b9675-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b9675-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b9675-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b9675-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b9675-105">Hiermee wordt een bewerking toegepast op de onderliggende qubits die een little-endian-registratie maakt.</span><span class="sxs-lookup"><span data-stu-id="b9675-105">Applies an operation to the underlying qubits making up a little-endian register.</span></span> <span data-ttu-id="b9675-106">Deze bewerking is gemarkeerd als intern, omdat een registratie van een little-endian is bedoeld als ' dekkend ', zodat dit alleen een implementatie detail is.</span><span class="sxs-lookup"><span data-stu-id="b9675-106">This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.</span></span>

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="b9675-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="b9675-107">Input</span></span>

### <a name="bareop--qubit--unit-adj--ctl"></a><span data-ttu-id="b9675-108">bareOp: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="b9675-108">bareOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="register--littleendian"></a><span data-ttu-id="b9675-109">registreren: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b9675-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="b9675-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b9675-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

