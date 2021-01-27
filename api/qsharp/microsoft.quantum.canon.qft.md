---
uid: Microsoft.Quantum.Canon.QFT
title: Bewerking QFT
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 30f475c3850c248b5af58db1e4aac3638c4c0471
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852296"
---
# <a name="qft-operation"></a>Bewerking QFT

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert de Quantum Fourier-trans formatie uit op een Quantum register dat een geheel getal in de weer gave big endian bevat.

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="qs--bigendian"></a>qs: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Quantum registratie waarop de Quantum Fourier-trans formatie wordt toegepast



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De invoer en uitvoer worden gezien als big endian-code ring.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyQuantumFourierTransformBE](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)