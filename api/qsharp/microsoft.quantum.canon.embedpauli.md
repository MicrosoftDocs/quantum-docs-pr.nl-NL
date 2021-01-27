---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: De functie EmbedPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: 0e6a93e22ee495abcc44bdf522e7c72c0981308b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840536"
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



## <a name="example"></a>Voorbeeld

De matrix verkrijgen `[PauliI, PauliI, PauliX, PauliI]` :

```qsharp
EmbedPauli(PauliX, 2, 3);
```