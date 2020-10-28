---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Bewerking MultiplexZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: f7b1973e18ad396ebe892ad63ae47374a7cafbd5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703958"
---
# <a name="multiplexz-operation"></a>Bewerking MultiplexZ

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een Pauli Z-rotatie toegepast op een matrix van qubits.

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a>Beschrijving

Hiermee wordt de unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $Z $, wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.
Met name deze bewerking kan worden weer gegeven door de unitary

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.
\end{align} $ $

## <a name="input"></a>Invoer

### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $. De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.


### <a name="control--littleendian"></a>besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.

## <a name="references"></a>Naslaginformatie

- Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApproximatelyMultiplexZ](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)