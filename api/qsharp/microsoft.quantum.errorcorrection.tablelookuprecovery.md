---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: De functie TableLookupRecovery
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: 9f957155e42bb6b5163521171fcba5897f290335
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824402"
---
# <a name="tablelookuprecovery-function"></a><span data-ttu-id="63f2f-102">De functie TableLookupRecovery</span><span class="sxs-lookup"><span data-stu-id="63f2f-102">TableLookupRecovery function</span></span>

<span data-ttu-id="63f2f-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="63f2f-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="63f2f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63f2f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63f2f-105">Voor een gegeven tabel met Pauli-bewerkingen op een bepaald REGI ster van qubits retourneert deze functie een object van het type `RecoveryFn` dat alle informatie bevat die nodig is voor het uitvoeren van een tabel-lookup-code ring met betrekking tot de opgegeven matrix van Pauli-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="63f2f-105">For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.</span></span>

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a><span data-ttu-id="63f2f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="63f2f-106">Input</span></span>

### <a name="table--pauli"></a><span data-ttu-id="63f2f-107">tabel: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="63f2f-107">table : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="63f2f-108">Tabel met Pauli-bewerkingen die worden uitgevoerd op een bepaald Qubit-REGI ster</span><span class="sxs-lookup"><span data-stu-id="63f2f-108">Table of Pauli operations that operate on a given qubit register</span></span>



## <a name="output--recoveryfn"></a><span data-ttu-id="63f2f-109">Uitvoer: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="63f2f-109">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="63f2f-110">Een object van het type `RecoveryFn` , dat wil zeggen een kaart `Syndrome -> Pauli[]` die is gekoppeld aan een bepaalde Syndrome-matrix een bijbehorende Pauli-correctie bewerking.</span><span class="sxs-lookup"><span data-stu-id="63f2f-110">An object of type `RecoveryFn`, i.e., a map `Syndrome -> Pauli[]` that associates with a given syndrome array a corresponding Pauli correction operation.</span></span>