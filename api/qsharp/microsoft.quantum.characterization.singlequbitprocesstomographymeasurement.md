---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Bewerking SingleQubitProcessTomographyMeasurement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 3756040df8e34ecee1e968428b08387e0096ab7b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204195"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a>Bewerking SingleQubitProcessTomographyMeasurement

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een Qubit-proces tomography meting uitgevoerd in de Pauli, op basis van een bepaald kanaal van belang.

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a>Invoer

### <a name="preparation--pauli"></a>voor bereiding: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Het Pauli basis element $P $ waarin een Qubit moet worden voor bereid.


### <a name="measurement--pauli"></a>meting: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Het Pauli basis element $Q $ waarin een Qubit moet worden gemeten.


### <a name="channel--qubit--unit"></a>kanaal: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Eén Qubit-kanaal $ \Lambda $ waarvan het gedrag wordt geschat met Process tomography.



## <a name="output--__invalidresult__"></a>Uitvoer: __ongeldig <Result>__

Het resultaat `Zero` met kans $ $ \Begin{align} \Pr (\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).
\end{align} $ $

## <a name="remarks"></a>Opmerkingen

De verdeling over de resultaten die door deze bewerking worden geretourneerd, is een speciaal geval van een tomography-status van twee Qubit. Laat $ \rho = J (\Lambda)/$2 de status Choi-Jamiłkowski voor $ \Lambda $ zijn. De bovenstaande distributie is dan identiek aan $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{align} $ $ waarbij $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 de daad werkelijke meting is die overeenkomt met $P $ en $Q $.