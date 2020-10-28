---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: De functie ApproximateInputEncoder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 67ef7a47a2e036f0953d946b4ace0e6673b173bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706885"
---
# <a name="approximateinputencoder-function"></a>De functie ApproximateInputEncoder

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Op basis van een set coëfficiënten en een tolerantie, wordt een status voorbereidings bewerking geretourneerd die elke coëfficiënt voorbereidt als de overeenkomstige amplitude van een reken kundige status, tot aan de opgegeven tolerantie.

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Invoer

### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De aanpassings tolerantie die moet worden gebruikt bij het coderen van de gegeven coëfficiënten in een invoer status.


### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

De coëfficiënten die moeten worden gecodeerd in een invoer status.



## <a name="output--stategenerator"></a>Uitvoer: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Een status voorbereidings bewerking waarbij de gegeven coëfficiënten als een invoer status voor een bepaald REGI ster worden voor bereid.