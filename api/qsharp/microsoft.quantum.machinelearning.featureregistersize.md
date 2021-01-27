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
# <a name="featureregistersize-function"></a><span data-ttu-id="9beef-102">De functie FeatureRegisterSize</span><span class="sxs-lookup"><span data-stu-id="9beef-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="9beef-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9beef-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="9beef-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9beef-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="9beef-105">Retourneert het aantal qubits dat nodig is voor het coderen van een bepaalde functie Vector.</span><span class="sxs-lookup"><span data-stu-id="9beef-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="9beef-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9beef-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="9beef-107">voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9beef-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9beef-108">Een voor beeld van een functie Vector die moet worden gecodeerd in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="9beef-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="9beef-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9beef-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9beef-110">De grootte die is vereist om te coderen `sample` in een Qubit-REGI ster, uitgedrukt als een aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="9beef-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>