---
uid: Microsoft.Quantum.Canon.ApplyToSubregisterC
title: Bewerking ApplyToSubregisterC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregisterC
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 52564e64d8cc9cdbeb2626ed8694168b8ed48c22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850466"
---
# <a name="applytosubregisterc-operation"></a>Bewerking ApplyToSubregisterC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking toegepast op een subregister van een REGI ster, waarbij qubits is opgegeven door een matrix met hun indexen.
De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.

```qsharp
operation ApplyToSubregisterC (op : (Qubit[] => Unit is Ctl), idxs : Int[], target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Invoer

### <a name="op--qubit--unit--is-ctl"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Bewerking die moet worden toegepast op de subregister.


### <a name="idxs--int"></a>idxs: [int](xref:microsoft.quantum.lang-ref.int)[]

De matrix van indices, waarmee wordt aangegeven op welke qubits de bewerking wordt toegepast.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Meld u aan waarop de bewerking reageert.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToSubregister](xref:Microsoft.Quantum.Canon.ApplyToSubregister)