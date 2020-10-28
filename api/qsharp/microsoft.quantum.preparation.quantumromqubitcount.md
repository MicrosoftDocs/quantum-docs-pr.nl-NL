---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: De functie QuantumROMQubitCount
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 988d5efa3e27cf5e9a276ab3ab443c10f88fe1ad
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708191"
---
# <a name="quantumromqubitcount-function"></a>De functie QuantumROMQubitCount

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket [](https://nuget.org/packages/)


Retourneert het totale aantal qubits dat moet worden toegewezen aan de bewerking die wordt geretourneerd door `QuantumROM` .

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a>Invoer

### <a name="targeterror--double"></a>targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)

De doel fout $ \epsilon $.


### <a name="ncoeffs--int"></a>nCoeffs: [int](xref:microsoft.quantum.lang-ref.int)

Aantal coëfficiënten opgegeven in `QuantumROM` .



## <a name="output--intintint"></a>Output: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))

## <a name="first-parameter"></a>Eerste para meter

Een tuple `(x,(y,z))` waarbij `x = y + z` het totale aantal toegewezen qubits is, `y` het aantal qubits voor het `LittleEndian` REGI ster en `z` het aantal garbage qubits.