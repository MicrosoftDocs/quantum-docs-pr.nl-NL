---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: De functie ApproximateInputEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 035c353c34362aa3486a7df9e7bb1bc95a6f63be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856167"
---
# <a name="approximateinputencoder-function"></a>De functie ApproximateInputEncoder

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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