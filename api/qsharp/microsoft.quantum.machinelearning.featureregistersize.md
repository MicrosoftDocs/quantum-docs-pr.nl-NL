---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: De functie FeatureRegisterSize
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 2754e901d74175c1841a38d795f5de02dabc9b8d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848429"
---
# <a name="featureregistersize-function"></a>De functie FeatureRegisterSize

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retourneert het aantal qubits dat nodig is voor het coderen van een bepaalde functie Vector.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Invoer

### <a name="sample--double"></a>voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een voor beeld van een functie Vector die moet worden gecodeerd in een Qubit-REGI ster.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De grootte die is vereist om te coderen `sample` in een Qubit-REGI ster, uitgedrukt als een aantal qubits.