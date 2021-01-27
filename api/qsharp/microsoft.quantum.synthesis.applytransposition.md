---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Bewerking ApplyTransposition
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855570"
---
# <a name="applytransposition-operation"></a>Bewerking ApplyTransposition

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt de amplitude in de index vervangen `a` door de amplitude bij de index `b` in de opgegeven status-vector van `register` lengte $n $.  Als `a` gelijk is aan `b` , wordt de status-vector niet gewijzigd.

## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Eerste index (moet een waarde tussen 0 en $2 ^ n-$1) zijn


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

Tweede index (moet een waarde tussen 0 en $2 ^ n-$1) zijn


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een lijst met $n $ qubits waarop de omzetting wordt toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

Bereid een uniforme superpositie voor in aantal statussen $ | 1 \ rangle $, $ | 2 \ rangle $ en $ | 3 \ rangle $ op 2 qubits.

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```