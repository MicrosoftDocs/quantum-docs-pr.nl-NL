---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Door de gebruiker gedefinieerd ReflectionPhases-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707716"
---
# <a name="reflectionphases-user-defined-type"></a>Door de gebruiker gedefinieerd ReflectionPhases-type

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Fasen voor een reeks van gedeeltelijke reflecties in amplitude versterking.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Benoemde items

### <a name="aboutstart--double"></a>AboutStart: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een matrix met fasen voor reflectie over de begin status.
### <a name="abouttarget--double"></a>AboutTarget: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een matrix met fasen voor reflectie over de doel status.

## <a name="remarks"></a>Opmerkingen

Beide matrices moeten dezelfde lengte hebben. Houd er rekening mee dat in veel gevallen de eerste fase van de begin status en laatste fase over de doel status een globale fase verschuiving introduceert en kan worden ingesteld op $0 $.