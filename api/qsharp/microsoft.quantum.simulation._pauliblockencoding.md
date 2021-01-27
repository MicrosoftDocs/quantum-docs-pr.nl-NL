---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: Functie _PauliBlockEncoding
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: c27ef1a6b7cd7c84defe2a783e9fb1610e52d1e7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851067"
---
# <a name="_pauliblockencoding-function"></a>Functie _PauliBlockEncoding

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee maakt u een Block-encoding-unitary voor een Hamiltonian.

De Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $ wordt beschreven door een som van Pauli-voor waarden $P _j $, elk met een real-efficient $ \ alpha_j $.

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Invoer

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een van `GeneratorSystem` $H $ als een som van de Pauli-voor waarden


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a>statePrepUnitary: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een unitary-bewerking $V $ waarmee de unitary $V _j $ wordt toegepast op index $ \ket{j} $, op basis van een functie $f: j\rightarrow V_j $.


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a>multiplexer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL)-> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL





## <a name="output--doubleblockencodingreflection"></a>Uitvoer: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Eerste para meter

De enige norm van coëfficiënten $ \alpha = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Tweede para meter

Een `BlockEncodingReflection` unitary $U $ van de Hamiltonian $U $. Omdat deze unitary voldoet aan $U ^ 2 = I $, is het ook een reflectie.

## <a name="remarks"></a>Opmerkingen

Voor beelden van bewerkingen voor het voorbereiden en onbereid maken van de status $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $, en het bouwen van een met vermenigvuldiging beheerde unitary zijn <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> en <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .