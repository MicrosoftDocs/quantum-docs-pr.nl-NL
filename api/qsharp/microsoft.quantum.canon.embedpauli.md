---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: De functie EmbedPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: e9042ca9eac4b8791057037dc5698eb14deadd31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207034"
---
# <a name="embedpauli-function"></a>De functie EmbedPauli

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een Qubit Pauli-operator en de index van een Qubit retourneert een multi-Qubit Pauli-operator met de opgegeven single-Qubit-operator in die index en `PauliI` op elke andere index.

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a>Invoer

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Een Pauli-operator met één Qubit die op de opgegeven locatie moet worden geplaatst.


### <a name="location--int"></a>Locatie: [int](xref:microsoft.quantum.lang-ref.int)

Een dergelijke index `output[location] == pauli` , waarbij `output` de uitvoer van deze functie is.


### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Lengte van de matrix die moet worden geretourneerd.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

