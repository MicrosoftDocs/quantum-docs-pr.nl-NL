---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Bewerking PrepareChoiState
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: ced71c4278f42f577760acd54ae53e7f5e6dae4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210570"
---
# <a name="preparechoistate-operation"></a>Bewerking PrepareChoiState

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de status van de Choi-Jamiołkowski voor een bepaalde bewerking voor de opgegeven referentie-en doel registers voor bereid.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="op--qubit--unit"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Bewerking $ \Lambda $ waarvan de Choi-Jamiołkowski-status $J (\Lambda)/2 ^ N $ moet worden voor bereid, waarbij $N $ het aantal qubits is waarop wordt `op` gehandeld.


### <a name="reference--qubit"></a>verwijzing: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van qubits, te beginnen met de status $ \ket{00\cdots 0} $ die moet worden gebruikt als referentie voor de actie van `op` .


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van qubits in eerste instantie in de $ \ket{00\cdots 0} $-status waarop moet `op` worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De Choi – Jamiłkowski State $J (\Lambda) $ van een quantum proces is gedefinieerd als $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ waarbij $ | X\rangle \! \rangle $ is de *vectorization* van een matrix $X $ in de kolom-stacking-Conventie. Het leren van een klassieke beschrijving van deze status biedt volledige informatie over het effect van $ \Lambda $ op wille keurige invoer status en vormt de basis van de tomography van het *Quantum proces*.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PrepareChoiStateA](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [Micro soft. Quantum. prepare. PrepareChoiStateC](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [Micro soft. Quantum. prepare. PrepareChoiStateCA](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)