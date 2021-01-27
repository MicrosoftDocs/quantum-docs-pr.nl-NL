---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: De functie ArrangedQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841078"
---
# <a name="arrangedqubits-function"></a>De functie ArrangedQubits

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Besturings element, doel en helper qubits rangschikken op basis van een index

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a>Beschrijving

Retourneert een Qubit-matrix met het doel bij index 0 en Control i op index 2 ^ i.  De helper qubits worden ingevoegd op alle andere posities in de matrix.

## <a name="input"></a>Invoer

### <a name="controls--qubit"></a>Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)




### <a name="helper--qubit"></a>Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--qubit"></a>Uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

