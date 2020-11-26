---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Door de gebruiker gedefinieerd RequiresCapability-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 0d9e4eb294b3ce91058c204d5dba37ea29b4ac28
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231004"
---
# <a name="requirescapability-user-defined-type"></a>Door de gebruiker gedefinieerd RequiresCapability-type

Naam ruimte: [micro soft. Quantum. targeting](xref:Microsoft.Quantum.Targeting)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Compileer kenmerk dat wordt gebruikt voor het markeren van een aanroepable met de runtime-mogelijkheden die nodig zijn.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a>Benoemde items

### <a name="level--string"></a>Niveau: [teken reeks](xref:microsoft.quantum.lang-ref.string)

De naam van het runtime-functionaliteits niveau dat is vereist voor de aanroepable.
### <a name="reason--string"></a>Reden: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een beschrijving van waarom de aanroepable vereist is voor deze runtime-functie.

## <a name="remarks"></a>Opmerkingen

Dit kenmerk wordt automatisch toegevoegd aan callables door de compiler, tenzij er al een exemplaar van dit kenmerk op de aanroepable bestaat. Het mag niet worden gebruikt, behalve in zeldzame gevallen waarbij de compiler de vereiste capaciteit niet correct afleiden.

Hieronder ziet u de lijst met namen van capabilities, in volg orde van toenemende mogelijkheden of het verminderen van de beperkingen:

## `"BasicQuantumFunctionality"`

Meet resultaten kunnen niet worden vergeleken voor gelijkheid.

## `"BasicMeasurementFeedback"`

Meet resultaten kunnen alleen worden vergeleken in if-instructie voorwaardelijke expressies in bewerkingen. Het blok van een if-instructie dat afhankelijk is van een resultaat, mag geen set-instructies bevatten voor onveranderlijke variabelen die buiten de blok-of Return-instructies zijn gedeclareerd.

## `"FullComputation"`

Geen runtime-beperkingen. Elk Q #-programma kan worden uitgevoerd.