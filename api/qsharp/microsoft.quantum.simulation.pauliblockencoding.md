---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: De functie PauliBlockEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: b1df6d239e6ef061cf0a4784c652e9dd126991d5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230426"
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