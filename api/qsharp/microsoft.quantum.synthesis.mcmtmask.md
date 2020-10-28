---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Door de gebruiker gedefinieerd MCMTMask-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709294"
---
# <a name="mcmtmask-user-defined-type"></a>Door de gebruiker gedefinieerd MCMTMask-type

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket [](https://nuget.org/packages/)


Een type dat een meerdere beheerde Toffoli-Gate met meerdere doelen vertegenwoordigt.

De eerste integer is een bitmasker voor regels voor besturings elementen.  Bits-indexen die zijn ingesteld, komen overeen met beheer regel indexen.

De tweede integer is een bitmasker voor doel lijnen.  Bits-indexen die zijn ingesteld, komen overeen met doel regel indexen.

De bits-indexen van beide gehele getallen moeten niet-aaneengesloten zijn.

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a>Benoemde items

### <a name="controlmask--int"></a>ControlMask: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="targetmask--int"></a>TargetMask: [int](xref:microsoft.quantum.lang-ref.int)

