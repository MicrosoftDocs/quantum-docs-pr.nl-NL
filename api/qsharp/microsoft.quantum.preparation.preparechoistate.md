---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Bewerking PrepareChoiState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: 8b2917a7d9414539f2f7c821c4115fc4b21d0373
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708652"
---
# <a name="preparechoistate-operation"></a>Bewerking PrepareChoiState

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket [](https://nuget.org/packages/)


Hiermee wordt de status van de Choi-Jamiłkowski voor een bepaalde bewerking voor de opgegeven referentie-en doel registers voor bereid.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="op--qubit--unit"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Bewerking $ \Lambda $ waarvan de Choi-Jamiłkowski-status $J (\Lambda)/2 ^ N $ moet worden voor bereid, waarbij $N $ het aantal qubits is waarop wordt `op` gehandeld.


### <a name="reference--qubit"></a>verwijzing: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van qubits, te beginnen met de status $ \ket{00\cdots 0} $ die moet worden gebruikt als referentie voor de actie van `op` .


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van qubits in eerste instantie in de $ \ket{00\cdots 0} $-status waarop moet `op` worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De Choi – Jamiłkowski State $J (\Lambda) $ van een quantum proces is gedefinieerd als $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ waarbij $ | X\rangle \! \rangle $ is de *vectorization* van een matrix $X $ in de kolom-stacking-Conventie. Het leren van een klassieke beschrijving van deze status biedt volledige informatie over het effect van $ \Lambda $ op wille keurige invoer status en vormt de basis van de tomography van het *Quantum proces* .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PrepareChoiStateA](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [Micro soft. Quantum. prepare. PrepareChoiStateC](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [Micro soft. Quantum. prepare. PrepareChoiStateCA](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)