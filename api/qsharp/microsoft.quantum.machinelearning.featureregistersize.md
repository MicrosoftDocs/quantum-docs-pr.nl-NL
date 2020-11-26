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
# <a name="featureregistersize-function"></a><span data-ttu-id="83fd6-102">De functie FeatureRegisterSize</span><span class="sxs-lookup"><span data-stu-id="83fd6-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="83fd6-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="83fd6-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="83fd6-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="83fd6-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="83fd6-105">Retourneert het aantal qubits dat nodig is voor het coderen van een bepaalde functie Vector.</span><span class="sxs-lookup"><span data-stu-id="83fd6-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="83fd6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="83fd6-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="83fd6-107">voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="83fd6-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="83fd6-108">Een voor beeld van een functie Vector die moet worden gecodeerd in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="83fd6-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="83fd6-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="83fd6-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="83fd6-110">De grootte die is vereist om te coderen `sample` in een Qubit-REGI ster, uitgedrukt als een aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="83fd6-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>