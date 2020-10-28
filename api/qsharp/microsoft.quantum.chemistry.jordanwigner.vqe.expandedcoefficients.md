---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: De functie ExpandedCoefficients
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 8f5a2319b5839d0d9e47972389330dc16dffcaf0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703071"
---
# <a name="expandedcoefficients-function"></a>De functie ExpandedCoefficients

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket [](https://nuget.org/packages/)


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