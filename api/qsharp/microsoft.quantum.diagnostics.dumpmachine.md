---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: De functie DumpMachine
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: c85cf6764bdc913a71448c525318f45743bf1df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702711"
---
# <a name="dumpmachine-function"></a>De functie DumpMachine

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


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