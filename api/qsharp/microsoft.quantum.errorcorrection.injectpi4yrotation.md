---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Bewerking InjectPi4YRotation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 249c347c9e9729e719eda69e4e9a21847d9a46eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825945"
---
# <a name="injectpi4yrotation-operation"></a>Bewerking InjectPi4YRotation

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee roteert u één Qubit door π/4 over de Y-as.

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a>Beschrijving

Voert een π/4-rotatie over `Y` .

De rotatie wordt uitgevoerd door een magische status te gebruiken; dat wil zeggen, een kopie van de status $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} .
\end{align} $ $

## <a name="input"></a>Invoer

### <a name="data--qubit"></a>gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een Qubit die moet worden gedraaid over $Y $ door $ \pi/$4.


### <a name="magic--qubit"></a>Magic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een Qubit in eerste instantie in de status Magic. De volgende toepassing van deze bewerking `magic` wordt geretourneerd naar de $ \ket {0} $-status.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
Ry(PI() / 4.0, data);
```

en

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

Met deze bewerking `Adjoint` wordt de functor ondersteund. in dat geval wordt dezelfde Magic-status gebruikt, maar het effect op de gegevens Qubit is $-\ Pi/4 $ $Y $-Rotation.