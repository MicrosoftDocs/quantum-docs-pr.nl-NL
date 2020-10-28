---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Bewerking LogicalANDMeasAndFix
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704029"
---
# <a name="logicalandmeasandfix-operation"></a>Bewerking LogicalANDMeasAndFix

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee worden de logische en van meerdere qubits berekend.

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="ctrlregister--qubit"></a>ctrlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits invoer naar de meervoudige invoer en poort.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit waarop de uitvoer van en wordt geschreven. Hierbij wordt ervan uitgegaan dat deze altijd begint in de $ \ket {0} $-status.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Wanneer `ctrlRegister` heeft precies $2 $ qubits, is dit gelijk aan de `CCNOT` bewerking, maar met een fase $e ^ {i \ pi/2} $ op $ \ket {001} $ en $-e ^ {i \ pi/2} $ op $ \ket {101} $ en $ \ket {011} $.
De adjoint is ook een aanpak-en reparatie methode die de inverse van de oorspronkelijke bewerking alleen in speciale gevallen (zie verwijzingen) is, maar die minder T-poorten gebruikt.

## <a name="references"></a>Naslaginformatie

- [*Craig Gidney* , 1709,06648](https://arxiv.org/abs/1709.06648)