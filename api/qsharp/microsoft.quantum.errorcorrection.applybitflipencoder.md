---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Bewerking ApplyBitFlipEncoder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: cc70cc409cb472a747899838d3a9ad2d78f6b5ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827695"
---
# <a name="applybitflipencoder-operation"></a>Bewerking ApplyBitFlipEncoder

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een persoonlijke bewerking die wordt gebruikt voor het implementeren van de bit Flip encoder en de decoder.

Houd er rekening mee dat dit coderings programma gebruik kan maken van in-place samenhangende herstel bewerking. in dat geval wordt de fout ' Oorzaak ' die wordt beschreven door de begin status van `auxQubits` .
Met name als u in `auxQubits` eerste instantie de status $ \ket {10} $ hebt, leidt dit tot een $X _1 $-fout op de gecodeerde Qubit.

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="coherentrecovery--bool"></a>coherentRecovery: [BOOL](xref:microsoft.quantum.lang-ref.bool)




### <a name="data--qubit"></a>gegevens: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="scratch--qubit"></a>kras: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Verwijzingen

- doi:10.1103/PhysRevA.85.044302