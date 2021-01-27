---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: De functie DumpRegister
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: 835c7a9edb22b4be630ebfc04587c12b3ff668b2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829219"
---
# <a name="dumpregister-function"></a>De functie DumpRegister

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


De huidige status van de doel computer die aan de opgegeven qubits is gekoppeld, wordt gedumpt.

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="location--t"></a>Locatie: 'T

Bevat informatie over waar de dump van de status moet worden gegenereerd.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

De lijst met qubits die moeten worden gerapporteerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

Geen.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

Met deze methode kunt u de gegevens die zijn gekoppeld aan de status van de opgegeven qubits, in een bestand of een andere locatie dumpen.
De werkelijke gegevens die worden gegenereerd en de semantiek van `location` zijn specifiek voor elke doel computer. Het leveren van een lege tuple als locatie ( `()` ) betekent meestal dat de uitvoer naar de-console wordt gegenereerd.

Voor de lokale volledige status Simulator die is gedistribueerd als onderdeel van de Quantum Development Kit, verwacht deze methode een teken reeks met het pad naar een bestand waarin de status van de opgegeven qubits (bijvoorbeeld de functie Wave van het bijbehorende subsysteem) wordt geschreven als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitudes van de kans van het meten van de bijbehorende status vertegenwoordigt.
Als de opgegeven qubits Entangled zijn met andere Qubit en de status ervan niet kan worden gescheiden, wordt alleen gerapporteerd dat de qubits Entangled zijn.