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
# <a name="featureregistersize-function"></a><span data-ttu-id="6283f-102">De functie FeatureRegisterSize</span><span class="sxs-lookup"><span data-stu-id="6283f-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="6283f-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6283f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="6283f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6283f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6283f-105">Retourneert het aantal qubits dat nodig is voor het coderen van een bepaalde functie Vector.</span><span class="sxs-lookup"><span data-stu-id="6283f-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="6283f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6283f-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="6283f-107">voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="6283f-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="6283f-108">Een voor beeld van een functie Vector die moet worden gecodeerd in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="6283f-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="6283f-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6283f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6283f-110">De grootte die is vereist om te coderen `sample` in een Qubit-REGI ster, uitgedrukt als een aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="6283f-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>