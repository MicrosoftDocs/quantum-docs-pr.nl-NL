---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Bewerking AssertOperationsEqualReferenced
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: a3e8791321b4f2ca1885dffeb92c7b13e5491a32
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702747"
---
# <a name="assertoperationsequalreferenced-operation"></a>Bewerking AssertOperationsEqualReferenced

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Als er twee bewerkingen worden uitgevoerd, worden er voor alle invoer statussen aangenomen dat ze identiek zijn.

Deze bevestiging wordt geïmplementeerd met behulp van de Choi – Jamiołkowski isomorphism om de bewering te beperken tot een van de Qubit-status verklaringen op twee Entangled-registers.
Deze bewerking heeft dus slechts één aanroep nodig voor elke bewerking die wordt getest, maar vereist twee keer zoveel qubits die moeten worden toegewezen.
Deze bevestiging kan worden gebruikt om ervoor te zorgen dat een geoptimaliseerde versie van een bewerking identiek is aan de Naïve-implementatie, of dat een bewerking die op een bereik van niet-Quantum gegevens reageert, overeenkomt met de bekende gevallen.

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Aantal qubits dat aan elke bewerking moet worden door gegeven.


### <a name="actual--qubit--unit"></a>werkelijk: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Te testen bewerking.


### <a name="expected--qubit--unit-adj"></a>verwacht: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Bewerking die het verwachte gedrag voor de bewerking tijdens de test definieert.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Voor deze bewerking moet de bewerking worden gemodelleerd om het verwachte gedrag te adjointable, zodat de inverse alleen kan worden uitgevoerd op het doel register.
Formeel, een kan een getransponeerde-bewerking opgeven, waardoor deze vereiste wordt versoepeld, maar de getransponeerde bewerking is niet in het algemeen fysiek te realiseren voor wille keurige Quantum bewerkingen, en is hier dus niet opgenomen als een optie.