---
uid: Microsoft.Quantum.Canon.RAll1
title: Bewerking RAll1
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll1
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.
ms.openlocfilehash: f4159a6cc0e0b4f18f418a53a309b5ce527b2608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852267"
---
# <a name="rall1-operation"></a><span data-ttu-id="0ae3b-102">Bewerking RAll1</span><span class="sxs-lookup"><span data-stu-id="0ae3b-102">RAll1 operation</span></span>

<span data-ttu-id="0ae3b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0ae3b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0ae3b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0ae3b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0ae3b-105">Hiermee wordt een bewerking voor fase verschuiving uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="0ae3b-106">$R = \boldone-(1-e ^ {i \phi}) \ket{1\cdots 1} \bra{1\cdots 1} $.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-106">$R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.</span></span>

```qsharp
operation RAll1 (phase : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0ae3b-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="0ae3b-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="0ae3b-108">fase: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ae3b-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ae3b-109">De fase $ \phi $ toegepast op status $ \ket{1\cdots 1} \bra{1\cdots 1} $.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-109">The phase $\phi$ applied to state $\ket{1\cdots 1}\bra{1\cdots 1}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="0ae3b-110">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0ae3b-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0ae3b-111">Het REGI ster waarvan de status moet worden geroteerd door $R $.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ae3b-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ae3b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

