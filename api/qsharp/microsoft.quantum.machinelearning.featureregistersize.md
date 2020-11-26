---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: De functie FeatureRegisterSize
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: bc5d5a23cfb431f9506b15bc404ab6955d1c2a35
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196409"
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