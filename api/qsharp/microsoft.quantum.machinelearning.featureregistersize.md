---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: De functie FeatureRegisterSize
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 8f7c47c7547e7a0ac1672f308de445c1b46461e1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708346"
---
# <a name="featureregistersize-function"></a>De functie FeatureRegisterSize

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Retourneert het aantal qubits dat nodig is voor het coderen van een bepaalde functie Vector.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Invoer

### <a name="sample--double"></a>voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een voor beeld van een functie Vector die moet worden gecodeerd in een Qubit-REGI ster.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De grootte die is vereist om te coderen `sample` in een Qubit-REGI ster, uitgedrukt als een aantal qubits.