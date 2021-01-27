---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Bewerking SteaneCodeEncoderImpl
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 81abe75e2a315fe9a994147242f3c8c9bde586ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824725"
---
# <a name="steanecodeencoderimpl-operation"></a>Bewerking SteaneCodeEncoderImpl

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel het coderings programma voor Steane code als de decoder.

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="data--qubit"></a>gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

een matrix met 1 Qubit die de invoer-Qubit is.


### <a name="scratch--qubit"></a>kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

een matrix met 6 qubits waarvoor redundantie is toegevoegd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

