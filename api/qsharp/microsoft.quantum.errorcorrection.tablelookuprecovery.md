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
# <a name="tablelookuprecovery-function"></a>De functie TableLookupRecovery

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voor een gegeven tabel met Pauli-bewerkingen op een bepaald REGI ster van qubits retourneert deze functie een object van het type `RecoveryFn` dat alle informatie bevat die nodig is voor het uitvoeren van een tabel-lookup-code ring met betrekking tot de opgegeven matrix van Pauli-bewerkingen.

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a>Invoer

### <a name="table--pauli"></a>tabel: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Tabel met Pauli-bewerkingen die worden uitgevoerd op een bepaald Qubit-REGI ster



## <a name="output--recoveryfn"></a>Uitvoer: [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Een object van het type `RecoveryFn` , dat wil zeggen een kaart `Syndrome -> Pauli[]` die is gekoppeld aan een bepaalde Syndrome-matrix een bijbehorende Pauli-correctie bewerking.