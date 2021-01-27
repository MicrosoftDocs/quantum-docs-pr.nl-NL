---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Door de gebruiker gedefinieerd ReflectionPhases-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: fc3642b76c6e01f0709e78ea42c9ea7237389afa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847182"
---
# <a name="reflectionphases-user-defined-type"></a>Door de gebruiker gedefinieerd ReflectionPhases-type

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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