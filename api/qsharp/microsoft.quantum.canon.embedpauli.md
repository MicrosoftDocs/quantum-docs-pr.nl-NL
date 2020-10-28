---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: De functie EmbedPauli
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: c78406aa4557834ac2bb40cf1847696d075e5135
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704188"
---
# <a name="embedpauli-function"></a>De functie EmbedPauli

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


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

