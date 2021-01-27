---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: De functie ExpandedCoefficients
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835627"
---
# <a name="expandedcoefficients-function"></a>De functie ExpandedCoefficients

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Breidt de compacte weer gave van de Jordan-Wigner coëfficiënten uit om een een-op-een-toewijzing te verkrijgen tussen deze en Pauli-voor waarden.

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a>Invoer

### <a name="coeff--double"></a>coeff: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een matrix met coëfficiënten, zoals gelezen uit de gegevens structuur van de Jordan-Wigner Hamiltonian.


### <a name="termtype--int"></a>termType: [int](xref:microsoft.quantum.lang-ref.int)

Het type Jordan-Wigner-term.



## <a name="output--double"></a>Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Uitgebreide matrices van coëfficiënten, één per Pauli term.