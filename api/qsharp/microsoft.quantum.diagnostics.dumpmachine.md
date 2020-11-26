---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: De functie DumpMachine
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: e7eb2dfce060b61e27deae31e3c1fc6dc3d7655c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202104"
---
# <a name="dumpmachine-function"></a>De functie DumpMachine

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


De huidige status van de doel computer dumpen.

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a>Invoer

### <a name="location--t"></a>Locatie: 'T

Bevat informatie over het genereren van de dump van de computer.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

Geen.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

Met deze methode kunt u informatie over de huidige status van de doel computer dumpen in een bestand of een andere locatie.
De werkelijke gegevens die worden gegenereerd en de semantiek van `location` zijn specifiek voor elke doel computer. Het leveren van een lege tuple als locatie ( `()` ) of het weglaten van de `location` para meter betekent meestal dat de uitvoer naar de-console wordt gegenereerd.

Voor de lokale volledige status Simulator die is gedistribueerd als onderdeel van de Quantum Development Kit, verwacht deze methode een teken reeks met het pad naar een bestand waarin de functie Wave wordt geschreven als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitudes vertegenwoordigt van de kans op het meten van de bijbehorende status.