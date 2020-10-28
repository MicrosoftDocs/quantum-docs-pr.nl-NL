---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Bewerking AssertOperationsEqualInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702753"
---
# <a name="assertoperationsequalinplace-operation"></a>Bewerking AssertOperationsEqualInPlace

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Als er twee bewerkingen worden uitgevoerd, worden er voor alle invoer statussen aangenomen dat ze identiek zijn.

Deze bevestiging wordt geïmplementeerd door de actie te controleren van de bewerkingen in alle provincies van het formulier $V _0 \otimes... \otimes V_ {n-1} $, waarbij $V _k $ een van de statussen $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ en $ \ket{i} $ (+ 1 Eigenstate van Pauli Y-operator) is.

Deze verklaring maakt gebruik van $n $ qubits en vereist dat meerdere aanroepen van de bewerkingen worden vergeleken.

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits-$n $ waarop de bewerkingen `givenU` zijn `expectedU` toegepast en waarop wordt uitgevoerd.


### <a name="givenu--qubit--unit"></a>givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Bewerking op $n $ qubits moet worden gecontroleerd.


### <a name="expectedu--qubit--unit-adj"></a>expectedU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Verwijzings bewerking op $n $ qubits die moet `givenU` worden vergeleken.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

De basis van de Staten $ \ket {0} $, $ \ket {1} $, $ \ket{+} $ en $ \ket{i} $ is de Chuang-Nielsen basis, zoals beschreven in [ *i. L. Chuang, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. AssertOperationsEqualReferenced](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)