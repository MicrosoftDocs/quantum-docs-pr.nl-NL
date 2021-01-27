---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: Bewerking MultiplexPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: 656b510cb19af69a9a3f0d537d54b0abfe76de4b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852455"
---
# <a name="multiplexpauli-operation"></a>Bewerking MultiplexPauli

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een Pauli-rotatie toegepast op een matrix van qubits.

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Hiermee wordt een unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $P $ wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.
Met name de actie van deze bewerking wordt vertegenwoordigd door de unitary

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.
\end{align} $ $

## <a name="input"></a>Invoer

### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $. De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.


### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Pauli-operator $P $ die de rotatieas bepaalt.


### <a name="control--littleendian"></a>besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApproximatelyMultiplexPauli](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)