---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Bewerking MeasureIdentity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: f8cf5975ac9407e8c532ace08455a41d3c08d6f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851814"
---
# <a name="measureidentity-operation"></a><span data-ttu-id="9feaf-102">Bewerking MeasureIdentity</span><span class="sxs-lookup"><span data-stu-id="9feaf-102">MeasureIdentity operation</span></span>

<span data-ttu-id="9feaf-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="9feaf-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="9feaf-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9feaf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9feaf-105">Hiermee wordt de identiteits operator in een REGI ster van qubits gemeten.</span><span class="sxs-lookup"><span data-stu-id="9feaf-105">Measures the identity operator on a register of qubits.</span></span>

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="9feaf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9feaf-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="9feaf-107">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9feaf-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9feaf-108">Het REGI ster dat moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="9feaf-108">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9feaf-109">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="9feaf-109">Output : __invalid<Result>__</span></span>

<span data-ttu-id="9feaf-110">De resultaat waarde `Zero` .</span><span class="sxs-lookup"><span data-stu-id="9feaf-110">The result value `Zero`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9feaf-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9feaf-111">Remarks</span></span>

<span data-ttu-id="9feaf-112">Aangezien $ \boldone $ alleen de eigenvalue $1 $ heeft en geen negatieve eigenvalue heeft, retourneert deze bewerking altijd `Zero` , die overeenkomt met de eigenvalue $ + 1 = (-1) ^ 0 $, en treedt er geen samen werking van de status van op `register` .</span><span class="sxs-lookup"><span data-stu-id="9feaf-112">Since $\boldone$ has only the eigenvalue $1$, and does not have a negative eigenvalue, this operation always returns `Zero`, corresponding to the eigenvalue $+1 = (-1)^0$, and does not cause a collapse of the state of `register`.</span></span>

<span data-ttu-id="9feaf-113">Op zichzelf is deze bewerking niet nuttig, maar is handig in de context van Process tomography, omdat deze informatie bevat over het behoud van de bewaring van een quantum proces.</span><span class="sxs-lookup"><span data-stu-id="9feaf-113">On its own, this operation is not useful, but is helpful in the context of process tomography, as it provides information about the trace preservation of a quantum process.</span></span>
<span data-ttu-id="9feaf-114">Met name een doel computer met verlies van metingen moet deze bewerking vervangen door een werkelijke meting van $ \boldone $.</span><span class="sxs-lookup"><span data-stu-id="9feaf-114">In particular, a target machine with lossy measurement should replace this operation by an actual measurement of $\boldone$.</span></span>