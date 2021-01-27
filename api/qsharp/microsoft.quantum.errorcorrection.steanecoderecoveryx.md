---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: De functie SteaneCodeRecoveryX
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: c90eac291ebe718d10377399184ad705bb51673e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824706"
---
# <a name="steanecoderecoveryx-function"></a>De functie SteaneCodeRecoveryX

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Decoder voor het X-deel van de stabilisatorer groep van de ⟦ ⟧ Steane Quantum code.

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a>Invoer

### <a name="syndrome--syndrome"></a>syndrome: [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Een Syndrome-matrix die is verkregen van het meten van de X-deel van de stabilisator.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een matrix met Pauli-bewerkingen die, wanneer toegepast op het gecodeerde Quantum systeem, de fout corrigeert die overeenkomt met `syndrome` .

## <a name="remarks"></a>Opmerkingen

De gekozen decoder maakt gebruik van de CSS-code-eigenschap van de ⟦-code van de 7, 1, 3 ⟧ Steane, dat wil zeggen, het corrigeert X fouten en Z-fouten afzonderlijk. Een eigenschap van de code is dat de locatie van de X, respectievelijk de Z-correctie die moet worden toegepast, de 3-bits code ring van de X, respectievelijk Z Syndrome is als een geheel getal.

## <a name="references"></a>Verwijzingen

- D. Gottesman, "stabilisators codes en Quantum fout correctie," Ph.D. thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryX](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Micro soft. Quantum. ErrorCorrection. SteaneCodeRecoveryFns](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)