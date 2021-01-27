---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: De functie PauliBlockEncoding
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848009"
---
# <a name="pauliblockencoding-function"></a>De functie PauliBlockEncoding

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee maakt u een Block-encoding-unitary voor een Hamiltonian.

De Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ wordt beschreven door een som van Pauli-voor waarden $P _j $, elk met een real-efficient $ \ alpha_j $.

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Invoer

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een van `GeneratorSystem` $H $ als een som van de Pauli-voor waarden



## <a name="output--doubleblockencodingreflection"></a>Uitvoer: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Eerste para meter

De enige norm van coëfficiënten $ \alpha = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Tweede para meter

Een `BlockEncodingReflection` unitary $U $ van de Hamiltonian $H $. Omdat deze unitary voldoet aan $U ^ 2 = I $, is het ook een reflectie.

## <a name="remarks"></a>Opmerkingen

Dit wordt verkregen door de status van $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ voor te bereiden en te ontbouwen en een unitary met vermenigvuldiging <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> te maken <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .