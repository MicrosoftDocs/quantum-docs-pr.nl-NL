---
uid: Microsoft.Quantum.Chemistry.JordanWigner.TrotterStepOracle
title: De functie TrotterStepOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: TrotterStepOracle
qsharp.summary: Returns Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: f7659616ea39d781137c26965cbf2005c5e634b2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703095"
---
# <a name="trottersteporacle-function"></a>De functie TrotterStepOracle

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Retourneert Trotter-stap bewerking en de para meters die nodig zijn om deze uit te voeren.

```qsharp
function TrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a>Invoer

### <a name="qsharpdata--jordanwignerencodingdata"></a>qSharpData: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Hamiltonian beschreven door `JordanWignerEncodingData` Format.


### <a name="trotterstepsize--double"></a>trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Stap grootte van Trotter integrator.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Volg orde van Trotter integrator.



## <a name="output--intdoublequbit--unit-adj--ctl"></a>Output: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL))

Een tuple waarbij: `Int` het aantal toegewezen qubits, `Double` is `1.0/trotterStepSize` en de bewerking is de Trotter-stap.