---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Bewerking FiveQubitCodeEncoderImpl
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: f70d2d1352c7b2eebee7a863eba97d78d7351dab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200846"
---
# <a name="fivequbitcodeencoderimpl-operation"></a>Bewerking FiveQubitCodeEncoderImpl

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een persoonlijke bewerking die wordt gebruikt voor het implementeren van zowel de 5 Qubit encoder als de decoder.

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="data--qubit"></a>gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

een matrix met 1 Qubit die de invoer-Qubit is.


### <a name="scratch--qubit"></a>kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

een matrix met 4 qubits waarvoor redundantie is toegevoegd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Het geselecteerde coderings programma is gemaakt op basis van het papier V. Kliuchnikov en D. Maslov, "Optima Lise ring van Clifford-circuits," fysieke. Rev. fysieke. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Afbeelding 4b) en is in totaal 11 poorten vereist.