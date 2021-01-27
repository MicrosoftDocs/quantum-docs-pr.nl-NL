---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexZ
title: Bewerking ApproximatelyMultiplexZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: b69b4de62241a7d16c2f07449115f864defda45d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841095"
---
# <a name="approximatelymultiplexz-operation"></a>Bewerking ApproximatelyMultiplexZ

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een Pauli Z-rotatie toegepast op een matrix van qubits, waarbij kleine rotatie hoeken worden afgekapt volgens een gegeven tolerantie.

```qsharp
operation ApproximatelyMultiplexZ (tolerance : Double, coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Hiermee wordt de unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $Z $, wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.
Met name deze bewerking kan worden weer gegeven door de unitary

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.
\end{align} $ $

## <a name="input"></a>Invoer

### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een tolerantie waaronder kleine coëfficiënten worden afgekapt.


### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $. De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.


### <a name="control--littleendian"></a>besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.

## <a name="references"></a>Verwijzingen

- Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. MultiplexZ](xref:Microsoft.Quantum.Canon.MultiplexZ)